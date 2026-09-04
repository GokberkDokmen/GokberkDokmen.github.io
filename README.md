# gokberkdokmen.github.io

Kişisel portfolyo sitem. Canlı: **https://gokberkdokmen.github.io**

Tasarım [Strata — HTML5 UP](https://html5up.net/strata) (CCA 3.0) üzerine kurulu;
içerik, iki dillilik ve proje kartları tarafımdan eklendi.

## Yapı

```
index.html               tek sayfa — tüm içerik burada
assets/css/main.css      şablonun kendi stili (elle düzenlenmiyor)
assets/css/custom.css    benim eklediğim stiller (dil, etiketler, kartlar)
assets/js/lang.js        TR/EN dil değiştirici
images/avatar.jpg        profil görseli
images/work/             proje görselleri (*-thumb.jpg ızgarada, diğeri lightbox'ta)
.nojekyll                GitHub Pages'in Jekyll işlemesini atlaması için
```

## İki dillilik nasıl çalışıyor

Her metnin HTML içinde iki kopyası var:

```html
<h2 lang="tr">Projeler</h2>
<h2 lang="en">Selected Work</h2>
```

`assets/js/lang.js` `<html>` etiketine `data-lang="tr"` ya da `data-lang="en"` koyuyor,
`custom.css` de diğer dildeki kopyaları gizliyor. Seçim `localStorage`'da saklanıyor;
ilk ziyarette tarayıcı diline göre karar veriliyor.

**Yeni metin eklerken iki dili de yazmayı unutma** — tek dilli bir etiket her iki
görünümde de aynı kalır.

## Yeni proje ekleme

1. Görseli `images/work/` altına koy: `proje-thumb.jpg` (800×600) ve `proje.jpg` (en fazla 1400px genişlik).
2. `index.html` içinde `id="two"` bölümündeki bir `<article>` bloğunu kopyalayıp düzenle.

## Yerelde çalıştırma

```bash
python -m http.server 8000
# http://localhost:8000
```

`index.html` dosyasını doğrudan çift tıklayarak da açabilirsin.
