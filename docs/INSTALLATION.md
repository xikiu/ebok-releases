# Install Ebok Alpha

[← Back to Ebok](../README.md) · [All releases](https://github.com/xikiu/ebok-releases/releases)

Choose the installer matching your operating system and processor from the [download table](../README.md#download). Alpha installers are provided for macOS Apple Silicon, macOS Intel, Windows x64, and Linux x64.

## macOS

1. Open the `.dmg` file.
2. Drag **Ebok** into **Applications**.
3. Open Ebok from Applications.

The alpha uses an ad-hoc signature and is not notarized. If macOS blocks the first launch, open **System Settings → Privacy & Security** after attempting to open the app, then choose **Open Anyway** for Ebok if you trust the download. Follow [Apple’s instructions](https://support.apple.com/en-us/102445).

## Windows

Run the `.exe` installer and follow the setup steps. The alpha installer is unsigned, so Windows may show an unrecognized-app warning. Check that you downloaded it from this repository before continuing.

## Linux

Make the AppImage executable, then launch it:

```sh
chmod +x Ebok-Alpha-linux-x64.AppImage
./Ebok-Alpha-linux-x64.AppImage
```

Your system needs AppImage support, including FUSE. Use your distribution’s package instructions if FUSE is missing.

## Your first book

Download the [Alice sample](../samples/README.md), open Ebok, and choose **Import books**. You can also drag ebook files into the library.

Open **Settings** at the bottom of the sidebar to choose Light, Dark, or System appearance. Adjust book typography and page color in **Reading preferences**, or use **Reading appearance** while a book is open.

## Enable AI word explanations

Select a word in a text-based book, choose **Define**, then **Enable AI · download ~700 MB**. Ebok uses Llama 3.2 1B Instruct on your device. A compatible GPU and internet for the initial download are required. See the [AI guide](AI.md) for setup and privacy details.

## Update from an earlier alpha

Quit Ebok, download the new installer, and replace the application using the same installation steps. On Linux, replace your old AppImage. Updates are manual; Ebok does not download or install them automatically.

The local library is stored separately from the application. Keep your original ebooks and avoid deleting app data during an update. Automatic library migration and cloud backup are not available in this alpha.

## Verify a download

Each release includes `SHA256SUMS.txt`. Download it alongside your installer and compare the installer’s SHA-256 value with the matching line.

**macOS**

```sh
shasum -a 256 Ebok-Alpha-mac-arm64.dmg
```

**Windows (PowerShell)**

```powershell
Get-FileHash .\Ebok-Alpha-win-x64.exe -Algorithm SHA256
```

**Linux**

```sh
sha256sum Ebok-Alpha-linux-x64.AppImage
```

Use your downloaded filename if it differs from the example. Matching checksums confirm that your file matches the published release asset.

## Need help?

[Report an installation problem](https://github.com/xikiu/ebok-releases/issues/new?template=bug_report.yml) with the app version, operating system, processor, and exact error message.
