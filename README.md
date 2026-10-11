# Ebok

A local-first ebook reader for desktop. Import your books, organize your library, and return to your last reading position.

**Ebok is in alpha.** Expect rough edges and keep copies of your original ebooks.

## Download Alpha 1

[Download v0.1.0-alpha.1](https://github.com/xikiu/ebok-releases/releases/tag/v0.1.0-alpha.1)

Choose an installer from the release’s **Assets** section:

| Computer | Download |
| --- | --- |
| Mac with Apple Silicon (M-series) | `Ebok-0.1.0-alpha.1-mac-arm64.dmg` |
| Intel Mac | `Ebok-0.1.0-alpha.1-mac-x64.dmg` |
| Windows x64 | `Ebok-0.1.0-alpha.1-win-x64.exe` |
| Linux x64 | `Ebok-0.1.0-alpha.1-linux-x64.AppImage` |

Installers are unsigned; macOS builds are not notarized. Your operating system may ask for additional confirmation before opening them.

### Install

- **macOS:** Open the DMG and drag Ebok into Applications. If macOS blocks the app, use **System Settings → Privacy & Security → Open Anyway** after attempting to open it. See [Apple’s instructions](https://support.apple.com/en-us/102445).
- **Windows:** Run the installer. An unsigned-app warning may appear.
- **Linux:** Make the AppImage executable, then open it: `chmod +x Ebok-0.1.0-alpha.1-linux-x64.AppImage`. AppImage support, including FUSE, must be available on your system.

## Try a sample book

[Download Alice’s Adventures in Wonderland (EPUB)](https://github.com/xikiu/ebok-releases/releases/download/v0.1.0-alpha.1/alice-in-wonderland.epub), by Lewis Carroll. [Project Gutenberg](https://www.gutenberg.org/ebooks/11) lists it as public domain in the USA; its original attribution and full license are retained. Import it using **Import books** or drag it into your library.

## What you can do

- Read EPUB, PDF, Kindle/Mobipocket, FictionBook, CBZ comics, TXT, Markdown, HTML, and DOCX files.
- Organize books into collections, add favorites, and track reading progress.
- Save bookmarks, highlights, and notes; adjust fonts, layout, and reading themes.
- Look up words with the built-in English dictionary and use optional translation and local AI explanations.
- Convert additional legacy formats when [Calibre](https://calibre-ebook.com/download) is installed separately.

Ordinary reading works offline. Books and reading data stay on your computer; there is no account or cloud-sync service. Online dictionary fallback and translation require internet. Optional AI explanations require a compatible GPU and an initial model download.

## Alpha limitations

- DRM-protected ebooks, KFX, ACSM, legacy DOC, and password-protected PDFs are not supported.
- Imported files are limited to 100 MB. Large books may need substantial memory.
- PDF and comic text search is not available. Scanned pages are not OCR’d.
- Desktop and browser libraries are separate; there is no automatic migration or cloud backup.
- Local library data can be lost if app data is deleted. Keep your original ebook files.
- Updates are installed manually from this repository’s releases.

## Feedback

[Report a bug](https://github.com/xikiu/ebok-releases/issues/new?template=bug_report.yml) or [suggest a feature](https://github.com/xikiu/ebok-releases/issues/new). Include the app version, operating system, book format, and steps to reproduce. Please avoid attaching copyrighted books or personal reading data; a small sample you can share is preferable.

This repository contains public downloads, release notes, and feedback. Ebok’s application source is maintained privately. Third-party component licenses are included in the application; optional AI-model weights retain their upstream terms.
