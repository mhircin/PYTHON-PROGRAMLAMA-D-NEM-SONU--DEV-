# PYTHON-PROGRAMLAMA-DONEM-SONU--ODEVI-
Python Programlama Dönem Ödevini İçermektedir.
Konu: Akıllı Müşteri Yönetim ve Analiz Sistemi (Telco Senaryosu)
Ortam: Google Colab 
Dil: PYTHON
# Akıllı Müşteri Yönetim ve Analiz Sistemi (Telco Senaryosu)

# Proje Hakkında
Bu proje Python Programlama dersi kapsamında verilen dönem ödevi için geliştirilmiştir. 
Amaç, bir telekomünikasyon şirketinin müşteri verilerini yönetebileceği, fatura hesaplayabileceği ve müşteri analizleri gerçekleştirebileceği temel bir sistem oluşturmaktır.

Proje iki bölümden oluşmaktadır:
  * Veri Yapıları ve Temel Mantık
  * Fonksiyonlar, Döngüler ve Kütüphaneler

Google Colab ortamında geliştirilmiştir

# 1. Kısım: Veri Yapıları ve Temel Mantık
Bu bölümde Python'ın temel veri yapıları ve karar mekanizmaları kullanılmıştır.

## Kullanılan Konular
- Değişkenler ve Veri Tipleri
- Liste (List) Kullanımı
- Sözlük (Dictionary) Kullanımı
- Koşullu İfadeler (if-else)
- String İşlemleri
- Rastgele ID Üretimi

# Gerçekleştirilen İşlemler
- Müşteriye ait ad, soyad, aylık ücret, sadakat süresi ve aktiflik durumu tanımlanmıştır.
- Şirket tarafından sunulan hizmetler liste içerisinde saklanmıştır.
- Müşteri bilgileri sözlük yapısında tutulmuştur.
- VIP müşteri kontrolü yapılmıştır.
- Müşteri adı büyük harfe dönüştürülmüştür.
- Rastgele müşteri kimliği (Customer ID) oluşturulmuştur.

# Neden Dictionary Kullanıldı?
Müşteri bilgileri farklı türlerde veriler içerdiğinden sözlük (dictionary) yapısı tercih edilmiştir.
Örneğin:
{
    "ad": "Medine",
    "soyad": "Hırçın",
    "aylik_ucret": 470
}
Bu yapı sayesinde verilere isimleri ile erişmek mümkündür.

Avantajları:

+ Daha okunabilir kod sağlar.
+ Veri yönetimini kolaylaştırır.
+ Hata yapma olasılığını azaltır.
+ Gerçek veritabanı mantığına daha yakındır.

# 2. Kısım: Fonksiyonlar, Döngüler ve Kütüphaneler
Bu bölümde müşteri sayısı artırılarak daha kapsamlı analizler gerçekleştirilmiştir.

# Kullanılan Konular
- Fonksiyonlar
- Döngüler (For Loop)
- Listeler
- Set Yapısı
- Hata Denetimi (Try-Except)
- Math Kütüphanesi
- Datetime Kütüphanesi

# GERÇEKLEŞTİRİLEN İŞLEMLER;

# Müşteri Yönetimi
5 farklı müşteri sözlük yapıları kullanılarak bir liste içerisinde saklanmıştır.

# Fatura Hesaplama
`tutar_hesapla()` fonksiyonu kullanılmıştır.

Fonksiyon:
* Aylık ücreti parametre olarak alır.
* %20 KDV ekler.
* Sonucu geri döndürür.

# Yuvarlama İşlemi
Math kütüphanesindeki `ceil()` fonksiyonu kullanılarak faturalar bir üst tam sayıya yuvarlanmıştır.

# Tarih Bilgisi
Datetime kütüphanesi kullanılarak rapor ve fatura tarihleri oluşturulmuştur.

# Benzersiz Hizmet Analizi
Şirket tarafından sunulan hizmetler listeye eklenmiş ve `set()` fonksiyonu kullanılarak tekrar eden hizmetler temizlenmiştir.
Örnek çıktı:
{'İnternet', 'Telefon', 'Televizyon'}

# Churn (Müşteri Kaybı) Analizi
Telekomünikasyon sektöründe müşterinin hizmetten ayrılma ihtimali "Churn Riski" olarak adlandırılır.
Bu projede:

- Müşteri aktif değilse
- veya müşteri memnuniyet skoru 50'nin altındaysa

müşteri churn riskinde kabul edilmiştir.

Kod mantığı:
if not musteri["aktif"] or musteri["skor"] < 50:
    print("Müşteri Churn Riskinde")

Bu yöntem sayesinde şirketin kaybetme ihtimali yüksek müşterileri önceden belirleyebilmesi amaçlanmıştır.
# Kullanılan Python Kütüphaneleri
python
import math
import datetime

# Math
+ ceil()
- Fatura tutarlarını yukarı yuvarlamak için kullanılmıştır.

# Datetime
+ now()
+ strftime()
Tarih ve saat bilgilerini almak için kullanılmıştır.

# Örnek Çıktı
Müşteri: Ali - Fatura: 540 TL
Müşteri: Ayşe - Fatura: 720 TL

UYARI: Ayşe isimli müşteri Churn riskindedir!

Benzersiz Hizmet Listemiz:
{'İnternet', 'Telefon', 'Televizyon'}

Fatura Düzenleme Tarihi:
01.06.2026

# Sonuç

Bu proje sayesinde Python programlama dilinin temel ve orta seviye konuları kullanılarak bir telekomünikasyon şirketi senaryosu üzerinde müşteri yönetimi, fatura hesaplama ve müşteri davranış analizi gerçekleştirilmiştir. Proje; veri yapıları, fonksiyonlar, döngüler, hata yönetimi ve kütüphane kullanımının gerçek bir iş senaryosunda nasıl uygulanabileceğini göstermektedir.
