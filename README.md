# ItalTech Dist

Pacchetti delle **10 applicazioni desktop freeware ItalTech** e del **launcher**. Questo repository contiene solo distribuzioni: nessun sorgente, nessun cloud, nessuna telemetria.

## Download

| Tool | Versione | Linux | Android | Windows |
|---|---:|---|---|---|
| [Password ItalTech](tools/password-italtech/) | 2.0.0 | AppImage, DEB, RPM, Arch | APK | EXE, MSI |
| [Notes ItalTech](tools/notes-italtech/) | 2.0.0 | AppImage, DEB, RPM, Arch | APK | EXE, MSI |
| [File Audit ItalTech](tools/forensic-italtech/) | 2.0.0 | AppImage, DEB, RPM, Arch | APK | EXE, MSI |
| [Anonymizer ItalTech](tools/anonymizer-italtech/) | 2.0.0 | AppImage, DEB, RPM, Arch | APK | EXE, MSI |
| [Clipboard ItalTech](tools/clipboard-italtech/) | 2.0.0 | AppImage, DEB, RPM, Arch | APK | EXE, MSI |
| [PDF ItalTech](tools/pdf-italtech/) | 2.0.0 | AppImage, DEB, RPM, Arch | APK | EXE, MSI |
| [Recorder ItalTech](tools/recorder-italtech/) | 2.0.1 | AppImage, DEB, RPM, Arch | APK | EXE, MSI |
| [Codici ItalTech](tools/codici-italtech/) | 2.0.0 | AppImage, DEB, RPM, Arch | APK | EXE, MSI |
| [Metadati ItalTech](tools/metadati-italtech/) | 2.0.0 | AppImage, DEB, RPM, Arch | APK | EXE, MSI |
| [ItalTech Utility](tools/italtech-utility/) | 1.10.1 | AppImage, DEB, RPM, Arch | APK | EXE |

## Launcher

| Versione | Piattaforme |
|---|---|
| 1.0.4 | [AppImage](launcher/latest/italtech-launcher-1.0.4.AppImage) · [DEB](launcher/latest/italtech-launcher_1.0.4_amd64.deb) · [RPM](launcher/latest/italtech-launcher-1.0.4.x86_64.rpm) · [Arch](launcher/latest/italtech-launcher-1.0.4-1-x86_64.pkg.tar.zst) · [APK](launcher/latest/italtech-launcher-1.0.4-universal.apk) · [EXE](launcher/latest/italtech-launcher-1.0.4-setup.exe) |

I link dei tool puntano a `tools/<tool>/latest/`, quello del launcher a `launcher/latest/`. Ogni tool ha il proprio README breve e la propria licenza freeware.

## Catalogo per il launcher

[`catalog.json`](catalog.json) elenca versioni, piattaforme, dimensioni, icone, repository e SHA-256 di ogni pacchetto, compreso il launcher. Gli installer Windows MSI/EXE vengono compilati dalla pipeline di release e aggiunti qui automaticamente.

URL pubblico del catalogo: `https://raw.githubusercontent.com/Anthony2000-Crypto/italtech-dist/main/catalog.json`

## Licenza

Ogni applicazione è freeware. I termini sono nella `LICENSE.md` della rispettiva cartella.
