# SNAP Yazılımı ile Sentinel-2 Verisi İşleme
Bu repoda ESA SNAP yazılımı ile temel Sentinel-2 görüntü işleme süreci özetlenecektir. Bu repo Eskişehir Teknik Üniversitesi, Yer ve Uzay Bilimleri Enstitüsü, Uzaktan Algılama ve Coğrafi Bilgi Sistemleri Doktora Programı UCS635 Uydu Görüntü İşleme dersi kapsamında ve diğer eğitimlerimde ortam kullanmak için hazırlanmıştır. Rahatlıkla kullanabilirsiniz. İyi görüntü işlemeler :)

1. Copernicus portaline ücretsiz üyelik yapıyoruz. https://scihub.copernicus.eu/
2. Open Hub adresi üzerinden görüntü indirme aracına ulaşıyoruz. https://scihub.copernicus.eu/dhus/#/home
3. Altlık harita bölümünden Sentinel-2 Cloudless'ı seçebiliriz daha net alan seçebilmek için.

![image](https://user-images.githubusercontent.com/3392893/222094237-b111355b-ecfd-4d0c-8657-9da5a518f62e.png)

4. Scroll Butonu ile Ceylanpınar'da aşağıdaki gibi bir alan çiziyoruz.

![image](https://user-images.githubusercontent.com/3392893/222129341-9c29ebe0-09d8-419c-b37f-e1127aab8b7e.png)

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
| Band 1          | Coastal aerosol     | 0.443      | 60         |
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

14. Bir sonraki aşamada görüntüyü aşağıdaki görseldeki şekilde zoomlayalım pivot tarlalar, alt ve üst tarafta tarım alanları olacak şekilde.

![image](https://user-images.githubusercontent.com/3392893/222121248-3381a4ad-f66b-4a60-ad12-49520d933d23.png)

15. Sırada görüntü kesme var. Görüntüye sağ tıklayarak "Spatial Subset fron View" seçeneği ile kesim işlemini başlatıyoruz.

![image](https://user-images.githubusercontent.com/3392893/222126050-d515dcc6-e64e-43f8-8232-3444c83d7527.png)

Band Subset alanında sadece B3-B4-B8 seçerek veri boyutunu azaltmayı amaçlıyoruz. 

![image](https://user-images.githubusercontent.com/3392893/222122732-f6a3d273-4177-4a67-8839-50a1184c9a56.png)

Kesilen veri sol tarafa yeni bir veri olarak eklendi.

![image](https://user-images.githubusercontent.com/3392893/222124300-02ce00f2-2a5e-4544-840d-77f2adbba0da.png)

16. Şimdi kestiğimiz veriyi sağ tıklayarak kaydedelim. 

Sağ tıklayarak "Save Product" diyoruz. İsim değiştirmeden .dim formatında kaydediyoruz. 

![image](https://user-images.githubusercontent.com/3392893/222124541-62f9d007-cb5f-4232-83f0-2ce5000a5c4e.png)

![image](https://user-images.githubusercontent.com/3392893/222124675-5ba31cc4-bb76-4d05-8666-a94a56edc664.png)

17. Şimdi subset ile kestiğimiz veriyi Load RGB Image Window seçeneği ile tekrar gösterelim. Aşağıdaki gibi güzel bir görüntü gelmiş olmalı.

![image](https://user-images.githubusercontent.com/3392893/222126477-e6f856e9-016d-45c7-a496-65bc5d9c48e8.png)

18. Bu iki veri açıkken ekranı Window > Tile Horizontally seçeneği ile ikiye bölebiliriz. Sonrasında View > Syncronize Image Views ile iki ekranı senkronize etmeyi unutmayın ve veriyi inceleyin. 

![image](https://user-images.githubusercontent.com/3392893/222133103-be31f4a4-18ac-41e4-9f50-6b651f15c259.png)

![image](https://user-images.githubusercontent.com/3392893/222132937-7cccec99-4f8e-496d-84cf-e89f2da2fa37.png)

19. Şimdi bu görüntüdeki bitki örtüsü alanlarını bulmak için bir indeks hesabı yapacağız. Bunun için "Band Math" özelliği kullanılıyor. SNAP içinde birçok tanımlı indeks olmasına rağmen biz bu uygulamada bunu elle yapacağız. Simple Ratio NIR/RED ile hesaplanan basit bir bitki örtüsü indeksidir. Sentinel-2 için B8/B4 ile hesaplanabilir. 

* Sentinel-2 ile hesaplanabilecek indekslerin listesi için: https://custom-scripts.sentinel-hub.com/custom-scripts/sentinel-2/indexdb/
* Bizim hesaplayacağımız Simple Ratio ile ilgili bilgi için. http://gsp.humboldt.edu/olm/Courses/GSP_216/lessons/Spectral-Enhancements/NDVI.html#:~:text=Simple%20Ratio%20Index%20(SR)%3A,indicate%20soil%2C%20water%20or%20ice.

* Öncelikle Raster > Bant Math seçiyoruz. Bir isim yazabilirsiniz. "Edit Expression" seçeneği ile formülü yazacağız.

![image](https://user-images.githubusercontent.com/3392893/222135201-30d517ce-66e3-423c-bc96-081f1d0817f0.png)

* B8/B4 yazdıktan sonra OK dediğimizde hesaplama yapılıyor. 

![image](https://user-images.githubusercontent.com/3392893/222135398-fe440344-aa02-43d6-b4c8-5b927b117b1e.png)

Burada bitki örtüsü alanların daha yüksek değer aldığını görebilirsiniz. 

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
