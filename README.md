# SquishIt — Browser-Based Image Compressor

A fast, client-side image compression tool that runs entirely in the browser. No server uploads, no third-party processing, no data leaves your machine.

---

## Overview

SquishIt is a single-page web application that allows users to compress large batches of images directly within the browser using the HTML5 Canvas API. It supports WebP, JPEG, and PNG formats and can handle up to 500 images in a single session. Compressed images are packaged into a ZIP file for convenient bulk download.

---

## Features

- Compress up to 500 images simultaneously
- Drag-and-drop or file picker upload interface
- Adjustable quality control from 1% to 99%
- Output format selection: WebP, JPEG, PNG, or preserve original format
- Smart compression logic — output file is always equal to or smaller than the original
- Per-image download or bulk ZIP download
- Real-time compression statistics: original size, compressed size, and savings percentage
- Fully client-side — no data is transmitted to any server

---

## Tech Stack

- HTML5
- CSS3
- Vanilla JavaScript
- HTML5 Canvas API (image processing)
- JSZip (client-side ZIP generation, loaded via CDN)

---

## Usage

No installation or build process required. Open `index.html` in any modern browser and the application is ready to use.

**To compress images:**

1. Drag and drop images onto the upload area, or click to browse files
2. Adjust the quality slider to the desired compression level
3. Select an output format if conversion is needed
4. Click "Compress All"
5. Download individual images or all at once as a ZIP archive

---

## Compression Behavior

The compressor uses a progressive quality reduction strategy. If the specified quality setting produces a file larger than the original — which can occur with already-optimized WebP images — the tool automatically lowers the quality in steps until the output is smaller. If no smaller output can be achieved, the original file is returned unchanged. The output will never exceed the original file size.

---

## Browser Compatibility

| Browser | Support |
|---|---|
| Chrome 90+ | Full |
| Edge 90+ | Full |
| Firefox 89+ | Full |
| Safari 15+ | Full |

---

## Live Demo

To use the tool right now, paste this link into your browser:

```
https://ahmad-344.github.io/image-compressor/
```

To run it on your local machine, download the `index.html` file and open it directly in any browser. No server or internet connection required after that point.

---

## Deployment

If you want to publish this tool on your own GitHub Pages or Netlify account, follow the steps below.

**GitHub Pages:**

1. Upload `index.html` to a public GitHub repository (rename it `index.html` if needed)
2. Go to repository Settings > Pages
3. Set source to the `main` branch, root folder
4. Your site will be live at `https://your-username.github.io/repository-name/`

**Netlify:**

Drag and drop `index.html` onto the Netlify dashboard at netlify.com. The site goes live immediately with an auto-generated URL.

---

## Privacy

All image processing is performed locally within the user's browser. No images, metadata, or usage data are transmitted to any external server at any point during compression or download.

---

## License

MIT License. Free to use, modify, and distribute.
