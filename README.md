# BlackBox — katalog ve güncelleme akışları

Bu depo BlackBox PS5 mağazasının canlı verisini tutar. Uygulama açılışta
otomatik denetler (sonra 6 saatte bir + Ayarlar'dan elle).

## Katalog (`catalog/catalogue-v2.json`)

```json
{"schemaVersion": 1, "revision": 14, "releases": [ … ]}
```

Her seçenek: `id, title, titleId, gameId, filename, url, sizeBytes, sha256?,
sourceId?, format (FFPFSC|exFAT), browserUrl?, cover (https), hero (https),
coverFallback?, heroFallback?, genre?, tagline?, description?, publisher?,
releaseDate?, version?, addedAt?, provider, artworkLayout (wide|ambient)`.

Kurallar: revizyon monoton artar (eski akış reddedilir), kimlikler tekil,
kapak/vitrin HTTPS zorunlu, boyut pozitif tamsayı. Elle düzenlemeyin —
`manager/blackbox_manager.py` panelini kullanın.

## Sürümler (`updates/`)

`payloads.json`: `{"minimumVersion": "1.0.0-beta.1", "payloads":
[{filename, version, url, checksum}]}` — URL'ler bu deponun Releases
dosyalarını gösterir. `minimumVersion` altındaki istemciler **zorunlu**,
diğerleri **isteğe bağlı** güncelleme görür.

`tv-app.json`: `{filename: "PPSA21453.ffpkg", version, url, checksum, size,
minimumVersion}` — aynı kural TV uygulaması için.


## İndirme

- **Uygulama sürümü:** [v1.0.1](https://github.com/D3ATHLY/blackbox/releases/tag/v1.0.1)
  - `blackbox.elf` — tarayıcı/servis sürümü (payload)
  - `PPSA01453.ffpkg` — TV uygulaması paketi
  - Her ikisi için SHA-256 yayında.
- **Akışlar:** [`updates/payloads.json`](updates/payloads.json), [`updates/tv-app.json`](updates/tv-app.json)
  (uygulama açılışta ve 6 saatte bir okur)

## Dokümanlar

- [Kurulum](guides/getting-started.md) · [İndirmeler](guides/downloads.md) ·
  [Kütüphane](guides/library.md) · [Sorun giderme](guides/troubleshooting.md)
- [Sürüm notları](release-notes)
- Uygulama arayüzü 8 dilde: Türkçe, English, Deutsch, Français, Español, Русский, العربية, Magyar.
