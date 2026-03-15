---
name: video-processing
description: Professional video editing and processing using FFmpeg. Use when user asks to trim, cut, merge, concatenate, transcode, watermark, subtitle, color grade, convert, compress, extract audio, create GIFs, or batch process videos. Handles platform-specific exports for YouTube, Instagram, TikTok, LinkedIn, Twitter/X.
license: MIT
metadata:
  version: 1.0.0
  author: Sam
  category: video
  domain: video-editing
  updated: 2026-02-25
  tech-stack: FFmpeg, Node.js
---

# Video Processing & Editing

Professional FFmpeg-powered video editing and processing skill. Transforms Claude into a specialized video engineer.

---

## Keywords

video editing, ffmpeg, trim video, cut video, merge videos, concatenate, transcode, watermark, subtitle, color grading, video compression, extract audio, gif creation, batch processing, video conversion, hdr to sdr, audio mixing, video export, instagram reels, youtube shorts, tiktok video

---

## Prerequisites

Ensure FFmpeg is installed:
```bash
# Check if installed
ffmpeg -version

# Install on macOS
brew install ffmpeg
```

---

## Core Workflows

### Workflow 1: Trim/Cut Video

**Step 1: Identify timestamps**
- Get video info: `ffprobe -v quiet -print_format json -show_format -show_streams input.mp4`
- Note duration, codec, resolution

**Step 2: Cut with precision**
```bash
# Fast seek (keyframe-accurate)
ffmpeg -ss 00:01:30 -to 00:02:45 -i input.mp4 -c copy output.mp4

# Frame-accurate (re-encode)
ffmpeg -i input.mp4 -ss 00:01:30 -to 00:02:45 -c:v libx264 -c:a aac output.mp4
```

### Workflow 2: Merge/Concatenate Videos

**Step 1: Create file list**
```bash
echo "file 'video1.mp4'" > filelist.txt
echo "file 'video2.mp4'" >> filelist.txt
echo "file 'video3.mp4'" >> filelist.txt
```

**Step 2: Concatenate**
```bash
# Same codec (fast)
ffmpeg -f concat -safe 0 -i filelist.txt -c copy output.mp4

# Different codecs (re-encode)
ffmpeg -f concat -safe 0 -i filelist.txt -c:v libx264 -c:a aac output.mp4
```

### Workflow 3: Add Watermark

```bash
# Image watermark (bottom-right corner)
ffmpeg -i input.mp4 -i watermark.png -filter_complex "overlay=W-w-10:H-h-10" output.mp4

# Text watermark
ffmpeg -i input.mp4 -vf "drawtext=text='Your Brand':fontsize=24:fontcolor=white@0.7:x=W-tw-10:y=H-th-10" output.mp4
```

### Workflow 4: Add Subtitles

```bash
# Burn subtitles (hardcoded)
ffmpeg -i input.mp4 -vf "subtitles=subs.srt:force_style='FontSize=22,PrimaryColour=&HFFFFFF&'" output.mp4

# Soft subtitles (selectable)
ffmpeg -i input.mp4 -i subs.srt -c copy -c:s mov_text output.mp4
```

### Workflow 5: Color Grading

```bash
# Brightness, contrast, saturation
ffmpeg -i input.mp4 -vf "eq=brightness=0.06:contrast=1.2:saturation=1.3" output.mp4

# Cinematic look (warm tones)
ffmpeg -i input.mp4 -vf "curves=r='0/0 0.25/0.28 0.5/0.55 0.75/0.8 1/1':g='0/0 0.25/0.22 0.5/0.5 0.75/0.78 1/1':b='0/0 0.25/0.18 0.5/0.45 0.75/0.7 1/0.9'" output.mp4

# HDR to SDR tone mapping
ffmpeg -i hdr_input.mp4 -vf "zscale=t=linear:npl=100,format=gbrpf32le,zscale=p=bt709,tonemap=tonemap=hable:desat=0,zscale=t=bt709:m=bt709:r=tv,format=yuv420p" output.mp4
```

### Workflow 6: Extract Audio

```bash
# Extract as MP3
ffmpeg -i input.mp4 -q:a 0 -map a output.mp3

# Extract as WAV (lossless)
ffmpeg -i input.mp4 -vn -acodec pcm_s16le output.wav

# Replace audio
ffmpeg -i input.mp4 -i new_audio.mp3 -c:v copy -map 0:v:0 -map 1:a:0 output.mp4
```

### Workflow 7: Create GIF/WebP

```bash
# High-quality GIF with palette
ffmpeg -i input.mp4 -ss 00:00:05 -t 3 -vf "fps=15,scale=480:-1:flags=lanczos,split[s0][s1];[s0]palettegen[p];[s1][p]paletteuse" output.gif

# Animated WebP (smaller file size)
ffmpeg -i input.mp4 -ss 00:00:05 -t 3 -vf "fps=15,scale=480:-1" -loop 0 output.webp
```

### Workflow 8: Platform-Specific Exports

```bash
# Instagram Reels (9:16, 1080x1920, max 90s)
ffmpeg -i input.mp4 -vf "scale=1080:1920:force_original_aspect_ratio=decrease,pad=1080:1920:(ow-iw)/2:(oh-ih)/2" -c:v libx264 -preset slow -crf 18 -c:a aac -b:a 128k -t 90 instagram_reel.mp4

# YouTube Shorts (9:16, 1080x1920, max 60s)
ffmpeg -i input.mp4 -vf "scale=1080:1920:force_original_aspect_ratio=decrease,pad=1080:1920:(ow-iw)/2:(oh-ih)/2" -c:v libx264 -preset slow -crf 18 -c:a aac -b:a 128k -t 60 youtube_short.mp4

# TikTok (9:16, 1080x1920, recommended bitrate)
ffmpeg -i input.mp4 -vf "scale=1080:1920:force_original_aspect_ratio=decrease,pad=1080:1920:(ow-iw)/2:(oh-ih)/2" -c:v libx264 -b:v 6M -c:a aac -b:a 128k tiktok.mp4

# LinkedIn Video (16:9, 1920x1080, max 10min)
ffmpeg -i input.mp4 -vf "scale=1920:1080:force_original_aspect_ratio=decrease,pad=1920:1080:(ow-iw)/2:(oh-ih)/2" -c:v libx264 -preset slow -crf 20 -c:a aac -b:a 128k linkedin.mp4

# YouTube (4K, high quality)
ffmpeg -i input.mp4 -vf "scale=3840:2160:force_original_aspect_ratio=decrease" -c:v libx264 -preset slow -crf 16 -c:a aac -b:a 256k youtube_4k.mp4
```

### Workflow 9: Batch Processing

```bash
# Process all MP4 files in directory
for f in *.mp4; do
  ffmpeg -i "$f" -vf "scale=1920:1080" -c:v libx264 -crf 20 "processed_${f}"
done

# Add watermark to all videos
for f in *.mp4; do
  ffmpeg -i "$f" -i watermark.png -filter_complex "overlay=W-w-10:H-h-10" "watermarked_${f}"
done
```

### Workflow 10: Multi-Track Audio Mixing

```bash
# Mix two audio tracks
ffmpeg -i video.mp4 -i bgmusic.mp3 -filter_complex "[0:a]volume=1.0[a1];[1:a]volume=0.3[a2];[a1][a2]amix=inputs=2:duration=first[out]" -map 0:v -map "[out]" -c:v copy output.mp4

# Add background music with fade
ffmpeg -i video.mp4 -i music.mp3 -filter_complex "[1:a]volume=0.2,afade=t=in:st=0:d=2,afade=t=out:st=58:d=2[bg];[0:a][bg]amix=inputs=2:duration=first[out]" -map 0:v -map "[out]" -c:v copy output.mp4
```

---

## Video Info Cheat Sheet

```bash
# Get full info
ffprobe -v quiet -print_format json -show_format -show_streams input.mp4

# Get duration only
ffprobe -v error -show_entries format=duration -of default=noprint_wrappers=1:nokey=1 input.mp4

# Get resolution
ffprobe -v error -select_streams v:0 -show_entries stream=width,height -of csv=s=x:p=0 input.mp4

# Extract single frame as image
ffmpeg -i input.mp4 -ss 00:00:10 -frames:v 1 thumbnail.jpg
```

---

## Best Practices

1. **Always check input first** with `ffprobe` before processing
2. **Use `-c copy`** when possible for lossless, instant operations
3. **Use CRF 18-23** for good quality/size balance (lower = better quality)
4. **Use `-preset slow`** for better compression at the cost of encoding time
5. **Test with short clips** before processing long videos
6. **Keep originals** — never overwrite source files
7. **Use hardware acceleration** when available: `-hwaccel auto`
