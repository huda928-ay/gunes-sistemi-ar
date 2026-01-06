# Güneş Sistemi AR - Gezegen Bilgi Kartları

WebAR tabanlı eğitim uygulaması. Basılı gezegen kartlarını kameraya tutarak 3D gezegen modelleri, bilgi panelleri ve Türkçe sesli anlatım deneyimleyin.

## 🚀 Özellikler

- **10 Gezegen Kartı Desteği**: Güneş, Merkür, Venüs, Dünya, Mars, Jüpiter, Satürn, Uranüs, Neptün, Ay
- **3D Modeller**: Dönen gezegenler ve yörünge halkaları
- **Türkçe Sesli Anlatım**: Her gezegen için otomatik sesli bilgi
- **Karşılaştırma**: İki kartı arka arkaya okutarak karşılaştırma yapın
- **Mobil Uyumlu**: Tam ekran kamera deneyimi

## 📋 Gereksinimler

### 1. targets.mind Dosyası Oluşturma

MindAR image tracking için `targets.mind` dosyası gereklidir:

1. [MindAR Image Targets Compiler](https://hiukim.github.io/mind-ar-js-doc/tools/compile) sayfasına gidin
2. 10 gezegen kartının **ön yüz** görsellerini sırayla yükleyin:
   - 0: Güneş
   - 1: Merkür
   - 2: Venüs
   - 3: Dünya
   - 4: Mars
   - 5: Jüpiter
   - 6: Satürn
   - 7: Uranüs
   - 8: Neptün
   - 9: Ay
3. "Compile" butonuna tıklayın
4. İndirilen `targets.mind` dosyasını proje kök dizinine kopyalayın

### 2. Dosya Yapısı

```
staj/
├── index.html      ✅ (oluşturuldu)
├── targets.mind    ⚠️ (oluşturmanız gerekli)
└── assets/
    └── textures/   (opsiyonel)
```

## 🎮 Kullanım

### Yerel Sunucu Başlatma

```bash
# Proje klasörüne gidin
cd c:\Users\Hüda\Desktop\staj

# Basit HTTP sunucu (Node.js gerekli)
npx serve .

# veya Python ile
python -m http.server 8000
```

### Tarayıcıda Açma

1. `https://localhost:3000` adresine gidin (HTTPS gerekli!)
2. Kamera izni verin
3. Gezegen kartlarını kameraya tutun

## 📱 Mobil Test

1. Bilgisayar ve telefon aynı WiFi'da olmalı
2. Bilgisayarın IP adresini bulun
3. Telefon tarayıcısında `https://[IP]:3000` açın

## ⚙️ Kontroller

| Buton | Fonksiyon |
|-------|-----------|
| 🔊 | Ses Aç/Kapat |
| 🔄 Sıfırla | Karşılaştırmayı temizle |

## 🔧 Sorun Giderme

| Sorun | Çözüm |
|-------|-------|
| Kamera açılmıyor | HTTPS kullanın, izinleri kontrol edin |
| Kart tanınmıyor | targets.mind dosyasını doğru oluşturun |
| Ses çalışmıyor | Türkçe TTS desteği kontrol edin |

## 📄 Lisans

Eğitim amaçlı proje - Staj sunumu için geliştirilmiştir.
