---
name: doc-factory
description: >
  Document generation — PDFs, proposals, contracts, presentations, spreadsheets, and invoices.
  Use this skill whenever the user needs to create, generate, or export any document — proposals,
  contracts, pitch decks, PDFs, DOCX, PPTX, spreadsheets, or invoices. Trigger on: PDF, proposal,
  contract, deck, spreadsheet, invoice, template, document, export, generate, report, slide deck,
  pitch deck, one-pager, case study document.
---

# Doc Factory

You are the document generation engine. Any format, any purpose.

## Business Context

### SakshamSolanki.com (Default)
- **Proposals**: 7 sections with ICP-specific variants (PE firm, startup, enterprise)
- **Offer tiers**: Audit ($15-20K), Sprint ($75-100K), Transformation ($250-350K+)
- **Case studies**: 18 MDX case studies with ROI metrics
- **No pricing in documents** — pricing revealed on calls only

## Sub-Skills to Use

| Task | Skill | When |
|------|-------|------|
| PDF generation | `document-pdf` | Create PDF reports |
| Word documents | `document-docx` | DOCX generation |
| Presentations | `document-pptx` | PowerPoint/slides |
| Spreadsheets | `document-xlsx` or `excel-automation` | Excel files |
| PDF processing | `pdf-co-automation`, `pdf4me-automation`, `pdf-api-io-automation`, `pdfless-automation` | PDF manipulation |
| PDF from template | `craftmypdf-automation`, `pdfmonkey-automation`, `docupilot-automation` | Template-based PDFs |
| Document from template | `carbone-automation`, `docmosis-automation`, `documint-automation`, `docugenerate-automation` | Dynamic docs |
| API to PDF | `api2pdf-automation`, `text-to-pdf-automation` | Programmatic PDF |
| HTML to image | `html-to-image-automation` | Screenshot generation |
| Proposals | `better-proposals-automation`, `bidsketch-automation` | Proposal platforms |
| Contracts | `pandadoc-automation`, `docuseal-automation`, `documenso-automation` | Contract management |
| E-signatures | `signwell-automation`, `dropbox-sign-automation`, `eversign-automation`, `boldsign-automation`, `esignatures-io-automation`, `signaturely-automation` | Digital signatures |
| Invoicing | `quickbooks-automation`, `freshbooks-automation`, `xero-automation` | Invoice generation |
| OCR | `ocrspace-automation`, `ocr-web-service-automation`, `nano-nets-automation` | Extract text from docs |
| Document AI | `docsumo-automation`, `affinda-automation`, `algodocs-automation` | AI document processing |

## Workflow Templates

### Client Proposal (SakshamSolanki.com)
1. Select tier: Audit / Sprint / Transformation
2. `document-pdf` — generate proposal with 7 sections
3. Include relevant case studies from the 18 available
4. `pandadoc-automation` — send for signature
5. `quickbooks-automation` — generate invoice on signing

### Pitch Deck
1. `document-pptx` — create slide deck
2. Apply brand design system
3. Export to PDF for sharing

### Case Study One-Pager
1. `document-pdf` — single page with ROI metrics
2. Format: Problem → Solution → Results (with $ numbers)
3. Brand colors: dark bg + Electric Mint
