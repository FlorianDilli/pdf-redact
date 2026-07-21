# PDF Redactor

A privacy-first, in-browser PDF redaction tool. Upload searchable PDFs, define sensitive terms, preview matches, and export a permanently redacted PDF — all without sending any data to a server.

## Features

- **100% client-side**: All processing happens in your browser using JavaScript
- **Multi-file support**: Upload and redact multiple PDFs at once
- **Smart matching**: Finds every occurrence of your specified terms across all pages
- **Interactive preview**: See exactly what will be redacted before committing
- **Selective redaction**: Toggle individual matches on/off
- **Secure output**: Generates an image-based PDF where original text is permanently destroyed
- **No installation**: Works directly in the browser, no software to install

## How It Works

1. **Upload** one or more PDF files (drag & drop or browse)
2. **Define terms** you want to remove (name, email, address, phone, etc.)
3. **Preview matches** — see every occurrence with context, select or deselect individually
4. **Export** a redacted PDF with selected information permanently removed

## Privacy

Your files **never leave your device**. This application:

- Runs entirely in your browser
- Does not upload files to any server
- Does not use cloud services or external APIs
- Does not track or store any user data
- Can be hosted on GitHub Pages or opened directly from your computer

The output PDF is an image-based document. Original text content is rasterized and destroyed, making recovery impossible.

## Deployment

### GitHub Pages

1. Push this repository to GitHub
2. Go to **Settings → Pages**
3. Set **Source** to your branch (e.g., `main`)
4. Your site will be available at `https://<username>.github.io/<repo-name>/`

### Local Use

Simply open `index.html` in any modern web browser (Chrome, Firefox, Safari, Edge).

## Browser Requirements

- Modern browser with support for:
  - ES Modules
  - Canvas API
  - Blob/URL APIs
  - File API

Tested on Chrome, Firefox, Safari, and Edge (latest versions).

## Technical Details

- **PDF rendering**: [pdf.js](https://mozilla.github.io/pdf.js/) v4
- **PDF generation**: [pdf-lib](https://pdf-lib.js.org/) v1
- **Output format**: Image-based PDF at 150 DPI
- **No build step**: Single `index.html` file, no dependencies to install

## Limitations

- Input PDFs must already contain a searchable text layer (OCR must be performed before redaction)
- Output PDFs are image-based and may be larger than the original
- Very large PDFs (100+ pages) may take longer to process

## License

MIT
