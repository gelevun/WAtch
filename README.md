# WhatsApp Chat Viewer PWA

WhatsApp export dosyalarını görüntülemek için tek HTML dosyasından oluşan bir Progressive Web App (PWA).

## Özellikler

* 📱 **WhatsApp Benzeri Arayüz**: Sohbet baloncukları ve tarih ayırıcıları
* 🖼️ **Medya Görüntüleme**: Resim, video, ses ve doküman desteği
* ⚡ **Hızlı Performans**: Lazy loading, virtual scrolling
* 📦 **Tek Dosya**: Kurulum gerektirmez, direkt tarayıcıda açılabilir
* 🔒 **Offline Çalışma**: PWA desteği ile offline kullanım
* 📱 **Mobil Uyumlu**: Responsive tasarım

## Kullanım

1. WhatsApp'tan sohbeti dışa aktarın (ZIP dosyası veya klasör)
2. `whatsapp-chat-viewer.html` dosyasını tarayıcıda açın
3. ZIP dosyasını veya klasörü yükleyin (sürükle-bırak desteklenir)
4. Sohbet görüntülenir!

## Desteklenen Medya Türleri

* **Resimler**: JPG, PNG, GIF, WebP
* **Ses Dosyaları**: OPUS, MP3, WAV, M4A
* **Dokümanlar**: PDF
* **Office Dosyaları**: Excel (XLSX, XLS), Word (DOC, DOCX)
* **İletişim Kartları**: VCF
* **Diğer**: Tüm dosya türleri (indirme linki)

## Teknik Detaylar

* **Teknoloji**: Vanilla JavaScript (ES6+), HTML5, CSS3
* **Storage**: IndexedDB (medya cache için)
* **PWA**: Service Worker ve Manifest.json
* **Bağımlılık**: JSZip ve PDF.js (CDN'den yüklenir)

## Dosya Yapısı

```
whatsapp-chat-viewer.html  # Ana uygulama (tek dosya)
manifest.json              # PWA manifest
service-worker.js          # Service worker (offline desteği)
```

## GitHub Pages

Bu uygulama GitHub Pages'de yayınlanabilir. `whatsapp-chat-viewer.html` dosyasını `index.html` olarak kopyalayarak yayınlayabilirsiniz.

## Lisans

MIT License

