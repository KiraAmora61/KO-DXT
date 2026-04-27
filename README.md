# N3TexViewer Kullanım Kılavuzu

## 1. N3TexViewer Nedir?

N3TexViewer, **Knight Online** oyunu için özel olarak geliştirilmiş bir doku (texture) görüntüleyici ve dönüştürücü uygulamasıdır. DXT formatındaki texture dosyalarını görüntülemenize, düzenlemenize ve farklı formatlara dönüştürmenize olanak tanır.

## 2. Desteklenen Formatlar

### Açılabilen Formatlar
- **DXT1, DXT2, DXT3, DXT4, DXT5** - DirectX sıkıştırılmış texture
- **BMP** - Bitmap görüntü formatı
- **TGA** - Targa görüntü formatı
- **JPG/JPEG** - JPEG görüntü formatı
- **PNG** - PNG görüntü formatı
- **ICO** - Windows ikon formatı

### Dönüştürülebilen Formatlar
- DXT ↔ BMP
- DXT ↔ PNG
- DXT ↔ ICO
- DXT ↔ DXT (farklı sıkıştırma türleri)
- BMP/TGA/JPG → DXT1/DXT3/DXT5

## 3. Dosya Açma Yöntemleri

### Yöntem 1: Menüden Açma
`File → Open` veya `Ctrl+O`

### Yöntem 2: Sürükle-Bırak
Dosyayı uygulama penceresine sürükleyip bırakabilirsiniz.

### Yöntem 3: Dosya Gezinme
- `File → Open Next` - Sonraki dosya
- `File → Open Previous` - Önceki dosya
- `File → Open First` - İlk dosya
- `File → Open Last` - Son dosya

Aynı klasördeki .dxt dosyaları arasında gezinebilirsiniz.

## 4. Tek Dosya Dönüştürme

`File → Convert` menüsünü kullanın:

| Parametre | Açıklama |
|-----------|----------|
| Format | DXT1, DXT2, DXT3, DXT4, DXT5 ve diğerleri |
| Width | Texture genişliği (piksel) |
| Height | Texture yüksekliği (piksel) |
| MipMap | MipMap oluşturma seçeneği |

> ⚠️ **Önemli:** Genişlik ve yükseklik değerleri **2'nin katı** olmalıdır (256, 512, 1024 vb.)

## 5. Toplu Dönüştürme Yöntemleri

### A) Otomatik Dönüştürme
`Tools → Convert Files Automatically`

- BMP/TGA/JPG dosyalarını seçer
- Format otomatik belirlenir
- Tüm dosyaları .dxt olarak kaydeder

### B) Manuel Dönüştürme
`Tools → Convert Files Manually`

- DXT/BMP/TGA/JPG dosyalarını seçer
- Format, boyut ve MipMap ayarlarını siz belirlersiniz

### C) Kapsamlı Dönüştürücü
`Tools → Converter Dialog`

- Kaynak ve hedef yol seçimi
- Format seçimi (kaynak ve hedef)
- Alt klasörleri dahil etme (Recursive)
- MipMap oluşturma
- Dosya filtresi
- Progress bar ile ilerleme takibi

## 6. Görüntüleme Özellikleri

### Alpha Kanalı Görüntüleme
`View → Alpha`

Texture'ın alpha kanalını grayscale olarak görüntüler. Şeffaflık kontrolü için kullanışlıdır.

### Pencere Boyutunu Ayarlama
`View → Adjust Window Size`

Pencereyi texture boyutuna göre otomatik ayarlar.

## 7. DXT Formatları Arasındaki Farklar

| Format | Bit/Pixel | Kullanım Alanı | Sıkıştırma |
|--------|-----------|---------------|------------|
| DXT1 | 4-bit | Opaque dokular | 1:8 |
| DXT3 | 8-bit | Keskin alpha geçişleri | 1:4 |
| DXT5 | 8-bit | Yumuşak alpha gradyanı | 1:4 |

### Ne Zaman Hangi Format?
- **DXT1:** Şeffaflık içermeyen dokular için ideal
- **DXT3:** Keskin alpha geçişleri (simge, harf, desen kenarları)
- **DXT5:** Yumuşak alpha gradyanları (bulut, su, alev, gölge)

## 8. Ek Araçlar

### BMP Kes
`Tools → Cut BMP`

Büyük BMP dosyalarını belirli boyutlarda parçalara ayırır.

### DXT Yeniden Kaydet
`Tools → Save Repeat`

DXT dosyalarını yeniden kaydetme işlemi yapar.

## 9. İpuçları ve Püf Noktaları

1. **Texture boyutları** her zaman 2'nin katı olmalı (128, 256, 512, 1024, 2048)
2. **Opaque dokular** için DXT1 kullanın
3. **Şeffaflık içeren dokular** için DXT3 veya DXT5 kullanın
4. **Keskin alpha geçişleri** (simge, harf gibi) için DXT3 tercih edin
5. **Yumuşak alpha gradyanları** (bulut, su gibi) için DXT5 kullanın
6. **Büyük dosya toplu işlemleri** için Kapsamlı Dönüştürücü'yü kullanın

---

*İyi çalışmalar!*
