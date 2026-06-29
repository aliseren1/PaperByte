# PaperByte - HD Document Scanner & PDF Creator

PaperByte, Android cihazların kamera donanımını asenkron olarak kullanarak belgeleri yüksek kalitede tarayan, gelişmiş imaj işleme algoritmalarıyla gri tonlamaya (Grayscale) dönüştüren ve nihai çıktıyı dinamik zaman damgalı PDF olarak kurumsal yerel dizine kaydeden bir mobil döküman yönetim uygulamasıdır.

## 🚀 Özellikler
- **Asenkron Kamera Yönetimi:** `Camera2` API mimarisi ve `TextureView` kullanılarak arka planda donanım optimizasyonlu canlı önizleme ve anlık matris yakalama.
- **Gelişmiş İmaj İşleme:** `ColorMatrix` ve `ColorMatrixColorFilter` algoritmaları ile belgeleri gölgelerden arındırılmış, kurumsal arşive uygun gri tonlamalı (Grayscale) yüksek kontrastlı matrise dönüştürme.
- **Dinamik PDF Üretimi:** RAM bellek üzerinde `PdfDocument` ve `Canvas` yapılandırmasıyla pikselleri kayıpsız HD dökümana dönüştürme ve otomatik dosya kapama (`document.close()`) optimizasyonu.
- **Güvenli Dosya Yönetimi:** `System.currentTimeMillis()` entegrasyonu ile çakışmasız, benzersiz dosya adlandırma ve `DIRECTORY_DOWNLOADS` sandbox depolama yönetimi.
- **Runtime Kararlılık & Loglama:** `try-catch` hata blokları, asenkron UI Thread yönetimli `Toast` bildirim mekanizmaları ve Android `Logcat` üzerinden runtime hata/uyarı takibi.

## 🛠️ Kullanılan Teknolojiler & Sınıflar
- **Platform:** Android
- **Dil:** Java / Kotlin
- **Kamera Donanımı:** `android.hardware.camera2`
- **Grafik & PDF Motoru:** `android.graphics.pdf.PdfDocument`, `android.graphics.Canvas`
- **Geliştirme Ortamı:** Android Studio
- **Hata Ayıklama:** Android Logcat Window

## 📂 Proje Dizin Yapısı
```text
PaperByte/
│
├── app/
│   ├── src/
│   │   └── main/
│   │       ├── java/com/example/paperbyte/
│   │       │   └── MainActivity.java (Kamera, İmaj İşleme ve PDF Kodları)
│   │       └── res/
│   │           └── layout/
│   │               └── activity_main.xml (UI Arayüz Tasarımı)
