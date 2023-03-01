# SNAP Yazılımı ile Sentinel-2 Verisi İşleme
Bu repoda ESA SNAP yazılımı ile temel Sentinel-2 görüntü işleme süreci özetlenecektir. Bu repo Eskişehir Teknik Üniversitesi, Yer ve Uzay Bilimleri Enstitüsü, Uzaktan Algılama ve Coğrafi Bilgi Sistemleri Doktora Programı UCS635 Uydu Görüntü İşleme dersi kapsamında ve diğer eğitimlerimde ortam kullanmak için hazırlanmıştır. Rahatlıkla kullanabilirsiniz. İyi görüntü işlemeler :)

1. Copernicus portaline ücretsiz üyelik yapıyoruz. https://scihub.copernicus.eu/
2. Open Hub adresi üzerinden görüntü indirme aracına ulaşıyoruz. https://scihub.copernicus.eu/dhus/#/home
3. Altlık harita bölümünden Sentinel-2 Cloudless'ı seçebiliriz daha net alan seçebilmek için.

![image](https://user-images.githubusercontent.com/3392893/222094237-b111355b-ecfd-4d0c-8657-9da5a518f62e.png)

4. Scroll Butonu ile Ceylanpınar'da aşağıdaki gibi bir alan çiziyoruz.

![image](https://user-images.githubusercontent.com/3392893/222094591-685369ea-a021-4f06-9acd-b675958311e3.png)

5. Sol tarafdaki filtreleme bölümünde 
* Sentinel-2
* Sensing Period: 02.07.2022-01.09.2022 seçip arama yapıyoruz.

![image](https://user-images.githubusercontent.com/3392893/222095320-2dedd08c-b96b-4e8b-8b59-b103d6ca4c88.png)

6. Arama sonucu ilk çıkan veriyi indirme butonu ile indiriyoruz. 
* S2A_MSIL1C_20220827T075621_N0400_R035_T37SEB_20220827T085529

![image](https://user-images.githubusercontent.com/3392893/222095534-88b795bf-73f8-46f6-83ae-3f4a50395f5f.png)
 
Bu aşamada veriyi indirdikten sonra Copernicus portali ile işimiz kalmadı. Şimdi SNAP yazılımını indireceğiz.

7. SNAP yazılımını https://step.esa.int/main/download/snap-download/ adresinden indirip kuruyoruz.

![image](https://user-images.githubusercontent.com/3392893/222097296-f1b7a7e4-8bb4-409a-b63e-87c4346b7190.png)

8. Programı kurduğunuzda ilk olarak Tools > Options menüsünden programın kullandığı cache boyutunu bilgisayar kapasitinize göre arttırmanızı kesinlikle öneriririm. 

![image](https://user-images.githubusercontent.com/3392893/222098279-bf4277ff-15e2-4858-a8d2-60d2a821c6fe.png)

9. İndirdiğimiz zip dosyasını sürükle bırak yöntemi ile SNAP yazılımında açabiliriz.

10. Veri açıldıktan sonra metadata bölümünden metaverileri, bands listesinden de Sentinel-2'nin sahip olduğu bantları görebilir ve tek tek çift tıklayarak açabilirsiniz.

![image](https://user-images.githubusercontent.com/3392893/222108022-30650492-dd2a-4a56-9e15-0d439ac9c992.png)

11. Sentinel-2 Bantları

| Bant   Numarası | Bant Adı            | Dalga boyu | Çözünürlük (m) |
|-----------------|---------------------|------------|------------|
| ﻿Band 1          | Coastal aerosol     | 0.443      | 60         |
| Band 2          | Blue                | 0.490      | 10         |
| Band 3          | Green               | 0.560      | 10         |
| Band 4          | Red                 | 0.665      | 10         |
| Band 5          | Vegetation Red-edge | 0.705      | 20         |
| Band 6          | Vegetation Red-edge | 0.740      | 20         |
| Band 7          | Vegetation Red-edge | 0.783      | 20         |
| Band 8          | NIR                 | 0.842      | 10         |
| Band 9          | Water vapour        | 0.945      | 60         |
| Band 10         | SWIR                | 1.375      | 60         |
| Band 11         | SWIR                | 1.610      | 20         |
| Band 12         | SWIR                | 2.190      | 20         |

12. Görüntü dosyamıza sağ tıkladıktan sonra "Open RGB Image Window" seçeneği ile ilgili bantları Red-Green-Blue sıralaması ile görselleştiriyoruz. Burada Natural Colour ifadesi bunu ifade etmiş oluyor. 

![image](https://user-images.githubusercontent.com/3392893/222120435-21bd6c98-7257-4916-a583-47d7f46ee088.png)

![image](https://user-images.githubusercontent.com/3392893/222120585-2e9bc8b6-14a8-4351-94fa-626fa92d267b.png)

13. Görüntümüz açıldı. Sol alttaki Navigation penceresinden veya ana pencereden scroll ile zoom in-out yaparak görüntüyü inceleyebiliriz.

![image](https://user-images.githubusercontent.com/3392893/222120908-0dff7340-712b-4d32-a4df-48255affe881.png)



* SNAP Nedir, SNAP İndirme
* Copernicus Nedir, Sentinel-2 Nedir?
* Görüntü indirme
* Sentinel-2 Bantları
* Sentinel-2 İndeksleri
* Görüntü Açma, RGB, Subset
* NDVI
* Band Math
* Vector Manipulation
* Supervised and Unsupervised Classifiation
