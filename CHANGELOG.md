# Release notes

## [Alpha 3](https://github.com/xikiu/ebok-releases/releases/tag/v0.1.0-alpha.3)

Updated to the current project reader codebase.

- Refreshed AI explanations with a rounded card, sparkle icon, clearer setup and retry buttons, and improved loading states.
- Added trackpad and mouse-wheel page navigation.
- Improved translation language validation and error messages, including Malay results.
- Improved selection menu animations and scrolling for long definitions.
- Retained the alpha Settings sidebar and desktop packaging fixes.

Validated with the desktop build, unit tests, browser tests, and packaged installer checks on all four platforms.

## [Alpha](https://github.com/xikiu/ebok-releases/releases/tag/v0.1.0-alpha.2)

AI-assisted reading with on-device word explanations, a cleaner library sidebar, and a refreshed public download page.

### AI reading highlight

The alpha includes **Meta’s Llama 3.2 1B Instruct**, running locally through **WebLLM + WebGPU** with 4-bit weights. Select a word and choose **Define** for an optional explanation of its meaning in the surrounding passage. Enable AI once with an initial ~700 MB model download; a compatible GPU is required. Word and passage text stay on-device for AI inference. [AI guide](docs/AI.md).

### Release updates

- Removed the Profile / Plan subscription card and the unused Billing and Log out screens.
- Added a direct **Settings** shortcut for interface appearance and reading preferences.
- Refreshed the public repository with app screenshots, direct installer links, installation and format guides, and focused feedback forms.
- Retained the public-domain Alice sample, original attribution, and download checksums.

Installers are available for macOS Apple Silicon and Intel, Windows x64, and Linux x64. Mac builds are not notarized; Windows installers are unsigned. [Installation guide](docs/INSTALLATION.md).


## Initial public alpha

The first public alpha of Ebok, a local-first desktop ebook reader.

### Included

- Multi-format reading: EPUB, PDF, MOBI/AZW/AZW3/KF8/PRC, FB2, CBZ, TXT, Markdown, HTML, and DOCX.
- A local library with collections, favorites, reading progress, and drag-and-drop imports.
- Bookmarks, highlights, notes, themes, and reader appearance controls.
- On-device AI word explanations using Meta’s Llama 3.2 1B Instruct via WebLLM + WebGPU, alongside a bundled English dictionary and optional online translation.
- Optional legacy-format conversion through a separately installed Calibre.

### Downloads

Installers are provided for macOS Apple Silicon, macOS Intel, Windows x64, and Linux x64. Choose the file matching your computer from **Assets**. `alice-in-wonderland.epub` is an optional public-domain sample from [Project Gutenberg](https://www.gutenberg.org/ebooks/11), with its attribution and original license retained. `SHA256SUMS.txt` contains the checksums of the installers and sample ebook.

Windows installers are unsigned and macOS apps are not notarized. See the [installation instructions](docs/INSTALLATION.md).

### Known limitations

This is an early testing release. Keep your original ebooks as a backup. There is no cloud sync, automatic library migration, or automatic updater. DRM-protected files are unsupported; Calibre is required for legacy conversion. PDF/comic text search and OCR are unavailable. Imports are limited to 100 MB. Online features and the initial optional AI-model download require internet; AI also requires a compatible GPU.

Please [report problems](https://github.com/xikiu/ebok-releases/issues) with your app version, operating system, book format, and reproduction steps.
