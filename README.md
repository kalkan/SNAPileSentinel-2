# SNAP Yazılımı ile Sentinel-2 Verisi İşleme
Bu repoda ESA SNAP yazılımı ile temel Sentinel-2 görüntü işleme süreci özetlenecektir.

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
