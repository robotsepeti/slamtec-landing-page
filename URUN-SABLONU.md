# Slamtec sitesine ürün ekleme / silme

Ürünler `app.js` dosyasındaki `const products = [` listesinde durur. Her ürün `{` ile başlayıp `},` ile biten bir bloktur.

## Ürün eklemek

1. Ürün görselini `assets/images` klasörüne yükleyin (Add file → Upload files). Dosya adında Türkçe karakter ve boşluk kullanmayın, örn. `rplidar-c1.jpg`.
2. `app.js` dosyasını açın, kalem (Edit) simgesine basın.
3. `const products = [` satırının hemen altına aşağıdaki şablonu yapıştırın ve bilgileri doldurun.
4. **Commit changes** deyin. 1–2 dakika içinde site güncellenir.

```js
  {
    id: 'urun-kodu', name: 'Kısa Ürün Adı', fullName: 'Ürünün RobotSepeti\'ndeki tam adı',
    family: 'RPLIDAR', category: 'lidar', image: 'gorsel-dosya-adi.jpg',
    url: 'https://www.robotsepeti.com/urun-sayfasinin-linki',
    summary: 'Kartta görünecek tek cümlelik açıklama.',
    paragraphs: ['Ürün detay sayfasında görünecek açıklama paragrafı.'],
    features: ['Öne çıkan özellik 1', 'Öne çıkan özellik 2'],
    specs: [['Menzil', '0,15–12 m'], ['Tarama açısı', '360°']],
    chips: ['12 m', '360°']
  },
```

Kurallar:
- `id`: sadece küçük harf, rakam ve tire (`-`). Her ürün için farklı olmalı.
- `category`: `lidar` (RPLIDAR), `mapping` (Haritalama & SLAM) veya `industrial` (Endüstriyel LiDAR).
- Metinlerin içinde `'` (tek tırnak) kullanacaksanız önüne `\` koyun: `RobotSepeti\'nde`.
- Blok `},` ile bitmeli; virgülü unutmayın.

## Ürün silmek

1. `app.js` → Edit.
2. Silinecek ürünün `id: '...'` satırını bulun (Ctrl+F).
3. O ürünün `{` satırından `},` satırına kadar olan bloğu seçip silin.
4. **Commit changes**.

## Bir şey bozulursa

Repo'nun **Actions** sekmesinde kırmızı çarpı görürseniz site eski halinde kalır; bozulmaz. Hatayı düzeltmek için `app.js` dosyasının **History** sayfasından bir önceki sürümü açıp içeriğini kopyalayarak geri yapıştırabilirsiniz.
