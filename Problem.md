# PROBLEM KARTI - Kampus Hasar-Ariza-Sikayet Raporlama Sistemi

+ *Proje Adi:* Kampus Hasar-Ariza-Sikayet Raporlama Sistemi
+ *Grup:* Mustafa Emirhan Turhan ve Mehmet Eren Yavuz
+ *Tarih:* 13 Ekim 2026
+ *Surum:* 1.0 (Taslak)

## 1. PROBLEM TANIMI
+ ### 1.1 Mevcut Durum

+ Universite kampusunde, binalar ve tesislerde olusan hasar, ariza ve kullanici sikayetleri *tamamen manuel* olarak yonetilmektedir:
+ - *Raporlama:* Sorun yasayan kisiler kagit, e-mail, telefon veya sozlu olarak bilgi verirler
+ - *Yonetim:* Bilgiler daganik sekilde tutulur (not, e-mail, Excel vb.)
+ - *Takip:* Raporun kim tarafindan yonetilecegi belli degildir
+ - *Iletisim:* Sorun cozenler ve bildirenler arasinda iletisim kopukluklari yasanir
+ - *Istatistik:* Kampus yonetiminin verileri yoktur. Kac sorun cozuldu, hangilerinde gecikme var, tekrar eden sorunlar nelerdir bilinmez

### 1.2 Sorunlarin Detayli Etkileri

+ *Kurumsal Etki:*
+-X Ayni sorunlar tekrar tekrar bildirilir (kaynaklarin israfi)
+-X Kampus yonetimi raporlanmamis sorunlardan habersiz kalir
+-X Bakim ve onarim planlamasi yapilamaz
+-X Butce ayirma kararlari veri temeline dayanmaz

+ *Kullanici Etkileri:*
+-X Kisiler sorunun cozulup cozulmedigini bilemez
+-X Cok uzun sureler sorun devam edebilir
+-X Sorun bildiricilerin motivasyonu azalir

+ *Operasyonel Etki:*
+-X Calisanlar arasinda koordinasyon sorunu
+-X Acil sorunlar goz ardi edilebilir
+-X Is yuku dagilimi yapilamaz

+ ## 2. COZUM YAKLASIMI
+ ### 2.1 Onerilen Cozum
+ **Kampus Hasar-Ariza-Sikayet Raporlama Sistemi** adiyla merkezi bir **dijital bir platform kurulacaktir. 

+ Bu platform sunlari saglayacaktir:
+ 1. *Merkezi Raporlama:* Tum sorunlar tek platformdan bildirilir
+ 2. *Otomatik Yonlendirme:* Sorunlar sorumlu birime otomatik gonderilir
+ 3. *Gercek Zamanli Takip:* Bildirici ve cozen kisiler ilerlemeyi gorebilir
- 4. *Istatistiksel Analiz:* Kampus yonetimi ozet rapor ve grafiklere erisir
+ 5. *Kategorilendirme:* Sorunlar turlerine gore (hasar/ariza/sikayet) gruplanir

+ ### 2.2 Kapsam (In Scope)
+
+-V Kullanici kaydi ve giris (Firebase Auth)
+-V Rapor olusturma/guncelleme/silme (CRUD)
+-V Rapor durumu takibi (Yeni → Kapali)
+-V Resim yukleme (hasar gorselleri)
+-V Konum secimi (Kampus lokasyonlari)
+-V Yorum yapma (iletisim)
+-V Istatistikler ve grafikler
+-V Admin paneli (kullanici yonetimi, sistem izleme)

+ ### 2.3 Disari Birakilan Konu (Out of Scope)
+ - X SMS/Push bildirimler (future)
+ - X Mobil native uygulama (web-responsive olacak)
+ - X IoT sensorleri (manuel rapor odakli)
+ - X Yapay zeka powered analiz (Ilk versiyon daha basit)
+ - X Multi-language (Turkce odakli)


## 3. HEDEF KULLANICILAR
### 3.1 Dogrudan Kullanicilar
| Kullanici | Rol | Aciklama |
| --------- | --- | -------- |
*Ogrenci* | Sorun Bildirici | Kampuste sorun bulup bildirir, durumu takip eder|
*Personel* | Sorun Bildirici / Cozen | Hasar/arizayi fark eder, sorumlu birime iletir.|
