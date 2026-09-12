# Pastry Pipeline — Destek & Gizlilik Sitesi

`sites.google.com/view/pastrypipeline` sayfasının GitHub Pages'te yayınlanabilir
statik (HTML/CSS) sürümü.

## Dosyalar

- `index.html` — Ana sayfa / Support (hero, iletişim, SSS)
- `privacy-policy.html` — Gizlilik Politikası
- `styles.css` — Ortak stil dosyası
- `.nojekyll` — GitHub Pages'in dosyaları olduğu gibi sunması için

## GitHub'da yayınlama (GitHub Pages)

1. GitHub'da yeni bir repo oluştur (örn. `pastry-pipeline`), public olsun.
2. Bu klasördeki tüm dosyaları reponun köküne yükle:
   - Ya web arayüzünden **Add file → Upload files** ile sürükle-bırak,
   - Ya da komut satırından:
     ```bash
     git init
     git add .
     git commit -m "İlk yayın"
     git branch -M main
     git remote add origin https://github.com/KULLANICI_ADIN/pastry-pipeline.git
     git push -u origin main
     ```
3. Repo → **Settings → Pages** bölümüne git.
4. **Source** olarak **Deploy from a branch** seç; branch `main`, klasör `/ (root)` olsun. **Save**.
5. Birkaç dakika içinde site şu adreste yayınlanır:
   `https://KULLANICI_ADIN.github.io/pastry-pipeline/`

> Not: `main` branch'e her push yaptığında, ekteki GitHub Actions iş akışı
> (`.github/workflows/deploy.yml`) siteyi otomatik yayına alır. Bu yöntemi
> kullanmak istersen Settings → Pages → Source = **GitHub Actions** seç.

## Kendi ekran görüntülerini eklemek

Ana sayfadaki telefon çerçevelerinde şimdilik placeholder (yer tutucu) var.
Kendi görsellerini eklemek için:

1. Görselleri repoya bir `images/` klasörüne koy (örn. `images/screen-1.png`).
2. `index.html` içinde `.phone .screen` bloklarını şununla değiştir:
   ```html
   <div class="screen"><img src="images/screen-1.png" alt="Oynanış"></div>
   ```

## E-posta / mağaza bağlantıları

- İletişim e-postası her yerde `randommobileapp@gmail.com` olarak ayarlı.
- `index.html` içindeki Google Play / App Store rozetlerinin `href="#"` değerlerini
  gerçek mağaza bağlantılarınla değiştir.
