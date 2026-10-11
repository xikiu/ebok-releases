# Release notes

## v0.1.0-alpha.1 — Alpha 1

The first public alpha of Ebok, a local-first desktop ebook reader.

### Included

- Multi-format reading: EPUB, PDF, MOBI/AZW/AZW3/KF8/PRC, FB2, CBZ, TXT, Markdown, HTML, and DOCX.
- A local library with collections, favorites, reading progress, and drag-and-drop imports.
- Bookmarks, highlights, notes, themes, and reader appearance controls.
- A bundled English dictionary, optional online translation, and optional local AI word explanations.
- Optional legacy-format conversion through a separately installed Calibre.

### Downloads

Installers are provided for macOS Apple Silicon, macOS Intel, Windows x64, and Linux x64. Choose the file matching your computer from **Assets**. `alice-in-wonderland.epub` is an optional public-domain sample from [Project Gutenberg](https://www.gutenberg.org/ebooks/11), with its attribution and original license retained. `SHA256SUMS.txt` contains the checksums of the installers and sample ebook.

Windows installers are unsigned and macOS apps are not notarized. See the [installation instructions](https://github.com/xikiu/ebok-releases#install).

### Known limitations

This is an early testing release. Keep your original ebooks as a backup. There is no cloud sync, automatic library migration, or automatic updater. DRM-protected files are unsupported; Calibre is required for legacy conversion. PDF/comic text search and OCR are unavailable. Imports are limited to 100 MB. Online features and the initial optional AI-model download require internet; AI also requires a compatible GPU.

Please [report problems](https://github.com/xikiu/ebok-releases/issues) with your app version, operating system, book format, and reproduction steps.
