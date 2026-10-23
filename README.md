# MEVEN_MODEM_OTA

[MEVEN_MODEM](https://github.com/uzunberkay/MEVEN_MODEM) firmware'i icin OTA
dagitim reposu. Dosyalar GitHub Pages ile yayinlanir.

| Dosya | Adres |
| --- | --- |
| Metadata | `https://uzunberkay.github.io/MEVEN_MODEM_OTA/ota/esp32/prod/metadata.json` |
| Firmware | `https://uzunberkay.github.io/MEVEN_MODEM_OTA/ota/esp32/prod/firmware.bin` |

`ota/esp32/prod/` icerigi elle duzenlenmez. MEVEN_MODEM reposunun `master`
dalina yapilan her push'ta CI (`ota-publish` job'u) `scripts/release.py` ile
`firmware.bin` ve `metadata.json` dosyalarini gunceller.

Metadata formati:

```json
{
  "version": "X.Y.Z",
  "url": "https://uzunberkay.github.io/MEVEN_MODEM_OTA/ota/esp32/prod/firmware.bin",
  "sha256": "<esptool image-info Validation hash>"
}
```

Cihazlar yalnizca `version` mevcut surumden buyukse guncellenir.
