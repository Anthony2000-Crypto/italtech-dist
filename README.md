# ItalTech Dist

Pacchetti delle **6 applicazioni desktop freeware ItalTech** e del **launcher**. Questo repository contiene solo distribuzioni: nessun sorgente, nessun cloud, nessuna telemetria.

## Download

| Tool | Versione | Linux | Android | Windows |
|---|---:|---|---|---|
| [Password ItalTech](tools/password-italtech/) | 2.1.5 | AppImage, DEB, RPM, Arch | APK | EXE |
| [Notes ItalTech](tools/notes-italtech/) | 2.1.5 | AppImage, DEB, RPM, Arch | APK | EXE |
| [Anonymizer ItalTech](tools/anonymizer-italtech/) | 2.1.5 | AppImage, DEB, RPM, Arch | APK | EXE |
| [Clipboard ItalTech](tools/clipboard-italtech/) | 2.1.5 | AppImage, DEB, RPM, Arch | APK | EXE |
| [Recorder ItalTech](tools/recorder-italtech/) | 2.1.7 | AppImage, DEB, RPM, Arch | APK | EXE |
| [The Offline Rebellion](tools/gioco-italtech/) | 1.0.5 | AppImage, DEB, RPM, Arch | APK | EXE |

## Launcher

| Versione | Piattaforme |
|---|---|
| 1.0.11 | [AppImage](launcher/latest/italtech-launcher-1.0.11.AppImage) · [DEB](launcher/latest/italtech-launcher_1.0.11_amd64.deb) · [RPM](launcher/latest/italtech-launcher-1.0.11.x86_64.rpm) · [Arch](launcher/latest/italtech-launcher-1.0.11-1-x86_64.pkg.tar.zst) · [APK](launcher/latest/italtech-launcher-1.0.11-universal.apk) · [EXE](launcher/latest/italtech-launcher-1.0.11-setup.exe) |

I link dei tool puntano a `tools/<tool>/latest/`, quello del launcher a `launcher/latest/`. Ogni tool ha il proprio README breve e la propria licenza freeware.

## Catalogo per il launcher

[`catalog.json`](catalog.json) elenca versioni, piattaforme, dimensioni, icone, repository e SHA-256 di ogni pacchetto, compreso il launcher. Gli installer Windows MSI/EXE vengono compilati dalla pipeline di release e aggiunti qui automaticamente.

URL pubblico del catalogo: `https://raw.githubusercontent.com/Anthony2000-Crypto/italtech-dist/main/catalog.json`

## Verifica i pacchetti

Il catalogo e ogni elenco `SHA256SUMS` sono firmati con la chiave Ed25519 di
release ItalTech (`keys/italtech-release-signing.asc`, impronta
`CB4AE0CF82A1DA039C70EE36E82DE487D84FD484`). Verifica prima la firma, poi l'hash:
se un passaggio fallisce, il file non è quello pubblicato.

```bash
# una volta sola
gpg --import keys/italtech-release-signing.asc

# catalogo (firma GPG legacy; il launcher usa la catena TUF)
gpg --verify catalog.json.asc catalog.json
```

Il launcher verifica la catena TUF (`metadata/root.json`, `timestamp.json`,
`snapshot.json`, `targets.json`) con la root incorporata: versioni arretrate,
metadati scaduti e hash diversi vengono rifiutati.

```bash
# pacchetto, dalla cartella del tool
cd tools/password-italtech/latest
gpg --verify SHA256SUMS.asc SHA256SUMS
sha256sum -c SHA256SUMS
```

Su Android gli APK sono firmati con il certificato di release (SHA-256
`49:0A:7B:27:1A:1E:FF:EB:C2:A1:51:F3:9B:B6:18:1B:3B:CA:07:20:10:C5:8F:97:EE:4F:C3:1E:AF:17:69:A5`):
`apksigner verify --print-certs <file>.apk` deve mostrare sempre la stessa
impronta. Gli installer Windows non hanno una firma Authenticode: per loro
valgono la firma del catalogo e l'hash.

## Licenza

Ogni applicazione è freeware. I termini sono nella `LICENSE.md` della rispettiva cartella.
