# BlackBox

BlackBox, PS5 konsollar için geliştirilmiş bir evde geliştirme (homebrew) vitrin ve indirme yöneticisidir.

---

## Sorumluluk Reddi ve Kullanım Koşulları

**Bu proje "olduğu gibi" sunulmaktadır.**

- Bu proje **hiçbir oyun dosyası, telif hakkı korumalı içerik veya üçüncü taraf yazılım barındırmaz**. `catalog/` altında yalnızca oyun meta verileri (başlık, kapak görseli bağlantıları, biçim bilgileri) tutulur; `updates/` altında yalnızca uygulamanın kendi güncelleme akış dosyaları bulunur.
- **Tüm dosya indirme ve yükleme işlemleri kullanıcının kendi sorumluluğundadır.** Bu araç yalnızca kullanıcının **yasal erişim hakkına sahip olduğu** içerikler için tasarlanmıştır.
- Bu proje **ticari bir hizmet değildir**. Herhangi bir ücret talep edilmez, abonelik gerektirmez.
- Hiçbir garanti verilmez. Yazılım, donanım, veri kaybı, hukuki sonuçlar veya herhangi bir zarardan dolayı projenin geliştiricileri, katkıda bulunanları ve ilişkili taraflar **hiçbir sorumluluk kabul etmez**.
- Bu proje **üçüncü taraf kaynaklardan (Archive.org, Vikingfile vb.) erişilen dosyaların güvenliğini, yasallığını veya telif hakkı uygunluğunu garanti etmez**; bu sorumluluk tamamen kullanıcıya aittir.
- Kullanıcı, bu aracı kullanarak tüm geçerli yasalara, hizmet koşullarına ve telif hakkı düzenlemelerine uymayı kabul eder.
- Bu proje, yetkisiz erişim, korsan kullanım veya yasa dışı faaliyetler için **tasarlanmamıştır ve bu amaçla kullanılmamalıdır**.

**Bu projeyi kullanan herkes, yukarıdaki koşulları kabul etmiş sayılır.**

---

## İçerik ve Sorumluluk Sınırları

| Konum | İçerik | Sorumluluk |
|---|---|---|
| `updates/payloads.json` | Uygulamanın kendi güncelleme bilgisi (sürüm, SHA-256) | Geliştirici |
| `updates/tv-app.json` | TV uygulaması güncelleme bilgisi | Geliştirici |
| `catalog/` dizini | Oyun meta verileri (başlık, kapak, biçim, boyut) | Üçüncü taraf kaynaklardan derlenmiştir |
| **Release asset'leri** | `blackbox.elf`, `PPSA01453.ffpkg` (kendi derlemesi) | Geliştirici |

- Kullanıcılar **hiçbir dosyayı bu repodan indirerek doğrudan kullanmamalıdır**; uygulama kendi güncelleme mekanizmasıyla çalışır.
- Oyun dosyaları (FFPFSC, PKG vb.) **bu repoda hiçbir zaman yayınlanmaz veya barındırılmaz**.

---

## Bu Proje Ne Değildir

- Bir oyun mağazası veya içerik dağıtıcısı değildir.
- Kırma (jailbreak), izinsiz erişim veya yasal olmayan herhangi bir işlem için tasarlanmamıştır.
- Üçüncü tarafların dosyalarını otomatik olarak dağıtmaz; kullanıcı manuel olarak içerik ekler.

---

## Lisans

Bu proje **GPL-3.0 veya daha sonrası** lisansı altında lisanslanmıştır. Detaylı lisans bilgisi için bkz. [LICENSE](LICENSE).

Üçüncü taraf bileşenler ve lisansları için bkz. [catalog/README.md](catalog/README.md) ve ilgili `THIRD-PARTY-NOTICES` dosyaları (release asset'leri ile birlikte gönderilir).

---

## İletişim

Teknik sorular veya hata raporları için [Issues](https://github.com/D3ATHLY/blackbox/issues) bölümünü kullanın.
