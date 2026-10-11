# Formats and alpha limitations

[← Back to Ebok](../README.md)

## Built-in readers

| Book type | Extensions |
| :--- | :--- |
| EPUB | `.epub`, `.epub3` |
| PDF | `.pdf` |
| Kindle / Mobipocket | `.mobi`, `.azw`, `.azw3`, `.kf8`, `.prc` |
| FictionBook | `.fb2`, `.fb2.zip`, `.fbz` |
| Comic archive | `.cbz` |
| Plain text | `.txt` |
| Markdown | `.md`, `.markdown` |
| Web page | `.html`, `.htm`, `.xhtml` |
| Word document | `.docx` |

Import support depends on the file’s contents as well as its extension. The maximum import size is **100 MB per file**; large books can use substantial memory.

## Optional conversion

Additional legacy formats (`.azw4`, `.cbr`, `.cb7`, `.cbc`, `.chm`, `.djvu`, `.htmlz`, `.lit`, `.lrf`, `.odt`, `.pdb`, `.pml`, `.pmlz`, `.rb`, `.rtf`, `.snb`, `.tcr`, and `.txtz`) can be converted when [Calibre](https://calibre-ebook.com/download) is installed separately on the same computer. Restart Ebok after installation. Conversion runs locally.

## Known limitations

- DRM-protected ebooks, KFX, ACSM, Apple Books files, legacy DOC, and password-protected PDFs are unsupported. ACSM files are download licenses rather than ebooks.
- PDF and comic text search are unavailable. Scanned pages are not OCR’d. DjVu conversion extracts existing text without OCR.
- Local library data can be lost when app data is deleted. Keep copies of your original books.
- Desktop and browser libraries are separate. Cloud sync, cloud backup, and automatic library migration are unavailable.
- Updates must be downloaded and installed manually.
- Online dictionary fallback and translation require internet. [On-device AI word explanations](AI.md) use Llama 3.2 1B Instruct and require a compatible GPU and an initial ~700 MB model download.

If a supported book fails to open, [report a bug](https://github.com/xikiu/ebok-releases/issues/new?template=bug_report.yml) with the format and steps to reproduce. Use a small sample you can share.
