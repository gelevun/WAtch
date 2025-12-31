# GitHub Pages Kurulum Adımları

## Hata: "Not Found" veya "Pages site failed"

Bu hata, GitHub Pages'in henüz aktif edilmediğini gösterir. Aşağıdaki adımları takip edin:

## Adım 1: GitHub Repository Ayarları

1. https://github.com/gelevun/WAtch repository'sine gidin
2. **Settings** sekmesine tıklayın (sağ üstte, Code sekmesinin yanında)
3. Sol menüden **Pages** seçeneğine tıklayın

## Adım 2: Pages Source Seçimi

**ÖNEMLİ**: İki seçenek var, **GitHub Actions** seçin:

### Seçenek A: GitHub Actions (Önerilen - Otomatik)

1. **Source** dropdown'ından **GitHub Actions** seçin
2. **Save** butonuna tıklayın
3. Artık her push'ta otomatik deploy olacak

### Seçenek B: Deploy from a branch (Manuel - Eski Yöntem)

Eğer GitHub Actions çalışmazsa:

1. **Source** dropdown'ından **Deploy from a branch** seçin
2. **Branch**: `main` seçin
3. **Folder**: `/ (root)` seçin
4. **Save** butonuna tıklayın

## Adım 3: İlk Deploy'u Tetikleme

### GitHub Actions Kullanıyorsanız:

1. **Actions** sekmesine gidin
2. Sol menüden **Deploy to GitHub Pages** workflow'unu seçin
3. Sağ üstte **Run workflow** butonuna tıklayın
4. Branch: `main` seçin
5. **Run workflow** butonuna tıklayın

### Manuel Deploy Kullanıyorsanız:

1. Herhangi bir dosyada küçük bir değişiklik yapın (örn: README.md'ye boşluk ekleyin)
2. Commit ve push edin:
   ```bash
   git add .
   git commit -m "Trigger Pages deploy"
   git push
   ```

## Adım 4: Site URL'si

Deploy tamamlandıktan sonra (1-2 dakika):

**Site URL**: https://gelevun.github.io/WAtch/

## Sorun Giderme

### "Not Found" hatası devam ediyor
- Settings > Pages'de doğru branch seçildiğinden emin olun
- 5-10 dakika bekleyin (CDN cache)
- Tarayıcı cache'ini temizleyin

### Actions sekmesinde hata görüyorsanız
- Actions sekmesine gidin
- Failed workflow'u tıklayın
- Hata mesajını kontrol edin
- Genellikle "Pages not enabled" hatası, Settings'den Pages'i aktif etmeniz gerektiğini gösterir

### Site açılıyor ama boş görünüyor
- `index.html` dosyasının root'ta olduğundan emin olun
- Browser console'da hataları kontrol edin
- Manifest.json'daki `start_url`'in doğru olduğundan emin olun

## Kontrol Listesi

- [ ] Settings > Pages'e gittim
- [ ] Source olarak "GitHub Actions" veya "Deploy from a branch" seçtim
- [ ] Save butonuna tıkladım
- [ ] Actions sekmesinde deploy başladı
- [ ] Deploy tamamlandı (yeşil tik)
- [ ] Site açılıyor: https://gelevun.github.io/WAtch/

