# GitHub Pages Yayınlama Talimatları

## Adım 1: GitHub Repository Oluşturma

1. GitHub'da yeni bir repository oluşturun
   - Repository adı: `WAgörcursor` (veya istediğiniz isim)
   - Public veya Private seçebilirsiniz
   - **ÖNEMLİ**: README, .gitignore veya license eklemeyin (zaten var)

## Adım 2: Repository'yi Remote Olarak Ekleme

```bash
git remote add origin https://github.com/KULLANICI_ADINIZ/WAgörcursor.git
```

**Not**: `KULLANICI_ADINIZ` yerine kendi GitHub kullanıcı adınızı yazın.

## Adım 3: GitHub'a Push Etme

```bash
git push -u origin main
```

## Adım 4: GitHub Pages'i Aktif Etme

### Yöntem 1: GitHub Actions (Önerilen - Otomatik)

1. GitHub repository sayfasına gidin
2. **Settings** sekmesine tıklayın
3. Sol menüden **Pages** seçeneğine tıklayın
4. **Source** altında **GitHub Actions** seçin
5. Kaydedin

Artık her push'ta otomatik olarak deploy edilecek!

### Yöntem 2: Manual (Eski Yöntem)

1. GitHub repository sayfasına gidin
2. **Settings** sekmesine tıklayın
3. Sol menüden **Pages** seçeneğine tıklayın
4. **Source** altında **Deploy from a branch** seçin
5. Branch: **main**, Folder: **/ (root)** seçin
6. **Save** butonuna tıklayın

## Adım 5: Manifest.json'u Güncelleme (Opsiyonel)

Eğer repository adınız "WAgörcursor" değilse veya subdirectory'de yayınlanıyorsa, `manifest.json` dosyasındaki `start_url`'i güncelleyin:

```json
{
  "start_url": "/REPOSITORY_ADI/"
}
```

## Canlı Site

Yayınlandıktan sonra siteniz şu adreste olacak:
- `https://KULLANICI_ADINIZ.github.io/WAgörcursor/`

**Not**: İlk deploy 1-2 dakika sürebilir.

## Sorun Giderme

### Site açılmıyor
- GitHub Actions sekmesinde deploy durumunu kontrol edin
- Settings > Pages'de doğru branch seçildiğinden emin olun
- 5-10 dakika bekleyin (CDN cache)

### Service Worker çalışmıyor
- HTTPS üzerinden eriştiğinizden emin olun (GitHub Pages otomatik HTTPS kullanır)
- Tarayıcı cache'ini temizleyin

### Manifest.json hatası
- `start_url`'in doğru olduğundan emin olun
- Tarayıcı console'unda hataları kontrol edin

