# neura — tanıtım ve hukuk sitesi

`https://inceilyas.github.io/aurasity/` adresinde yayımlanan, Aurasity iOS
uygulamasının statik tanıtım/gizlilik/şartlar/destek sitesi. Saf HTML +
CSS; JavaScript, derleme adımı ya da bağımlılık yok.

## Yapı

```
index.html            Türkçe tanıtım
privacy/index.html    Gizlilik Politikası (TR)
terms/index.html      Kullanım Şartları (TR)
support/index.html    Destek (TR)
en/index.html          İngilizce tanıtım
en/privacy/index.html  Privacy Policy (EN)
en/terms/index.html    Terms of Use (EN)
en/support/index.html  Support (EN)
assets/style.css       ortak stil
assets/logo.png        logo (512×512)
assets/favicon.png     favicon (128×128)
.nojekyll              GitHub Pages'in Jekyll işlemesini kapatır
```

Gizlilik ve şartlar sayfalarının içeriği, uygulama deposundaki
`docs/PRIVACY.md` ve `docs/TERMS.md` dosyalarından birebir aktarılmıştır.
Bu iki dosya güncellenince buradaki HTML'ler de elle güncellenmelidir —
otomatik bir senkronizasyon yoktur.

## Yayımlama adımları (git bilmeden, tarayıcıdan)

1. GitHub'da oturum aç, sağ üstten **+ → New repository**.
   - Repository name: `neura`
   - **Public** seçili olsun (GitHub Pages ücretsiz planda genel depo
     ister).
   - "Add a README file" kutusunu **işaretleme** (bu klasördeki README
     zaten var, çakışmasın).
   - **Create repository**'ye bas.
2. Açılan boş depo sayfasında **"uploading an existing file"**
   bağlantısına (ya da **Add file → Upload files** menüsüne) tıkla.
3. Bilgisayarında `neura-site` klasörünü aç, içindeki **her şeyi** (alt
   klasörler dahil: `privacy`, `terms`, `support`, `en`, `assets`,
   `.nojekyll`, `README.md`, `index.html`) seçip GitHub'ın açtığı yükleme
   alanına sürükle bırak.
   - `.nojekyll` gizli bir dosyadır (adı nokta ile başlıyor); Finder'da
     görünmüyorsa `Cmd+Shift+.` ile gizli dosyaları göster.
   - Klasör yapısı **birebir korunmalı**: `privacy/index.html` gibi bir
     dosya, GitHub'da da `privacy/index.html` yolunda durmalı — GitHub'ın
     sürükle-bırak yüklemesi klasör yapısını korur, tek tek dosya
     seçersen de klasörle birlikte sürüklemen yeterli.
4. Sayfanın altındaki **Commit changes** düğmesine bas (mesaj kutusunu
   olduğu gibi bırakabilirsin).
5. Üst menüden **Settings** sekmesine gir, sol menüden **Pages**'e tıkla.
6. **Build and deployment** altında **Source** olarak **Deploy from a
   branch** seçili olduğundan emin ol.
7. **Branch** altında `main` ve yanındaki klasör olarak **/ (root)**
   seç, **Save**'e bas.
8. Birkaç dakika bekle; sayfanın üstünde "Your site is live at
   `https://inceilyas.github.io/aurasity/`" yazısı çıkınca site yayındadır.
   (İlk yayında birkaç dakika sürebilir; sayfayı yenileyerek kontrol et.)

## Güncelleme

Bir dosyayı değiştirdiğinde aynı yoldan (**Add file → Upload files**)
yeni sürümü yükleyip **Commit changes**'e basman yeterli; GitHub Pages
birkaç dakika içinde yeni içeriği yayımlar.
