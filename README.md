# Akıllı Müşteri Yönetim ve Analiz Sistemi (Telco Senaryosu)

## Proje Hakkında

Bu proje, Python Programlama dersi kapsamında hazırlanmış bir dönem ödevidir. Amaç, Python'ın temel veri yapıları, fonksiyonlar, döngüler ve kütüphane kullanımını gerçek hayata yakın bir telekomünikasyon (Telco) senaryosu üzerinde uygulamaktır.

Sistem, müşteri bilgilerini saklamakta, fatura hesaplamaları yapmakta, müşteri analizleri gerçekleştirmekte ve ayrılma (Churn) riski taşıyan müşterileri tespit etmektedir.

---

## Kullanılan Konular

### 1. Veri Yapıları

* Değişkenler
* Liste (List)
* Sözlük (Dictionary)
* Küme (Set)

### 2. Karar Yapıları

* If
* Else
* Mantıksal Operatörler (and, or, not)

### 3. Fonksiyonlar

* Parametre kullanımı
* Return kullanımı

### 4. Döngüler

* For Döngüsü

### 5. Kütüphaneler

* random
* math
* datetime

---

## Sistem Özellikleri

### Müşteri Yönetimi

Her müşteri için aşağıdaki bilgiler tutulmaktadır:

* Ad Soyad
* Aylık Ücret
* Sadakat Süresi (Ay)
* Aktiflik Durumu

### VIP Müşteri Tespiti

Aşağıdaki koşullardan biri sağlanıyorsa müşteri VIP olarak değerlendirilir:

* Aylık ücret 500 TL'den büyükse
* Sadakat süresi 24 aydan fazlaysa

Çıktı:

```python
VIP Müşteri: İndirim Tanımla
```

Aksi durumda:

```python
Standart Müşteri
```

### Customer ID Üretimi

Her müşteri için rastgele bir müşteri numarası oluşturulur.

Örnek:

```text
IST-2026-5832
```

---

## Fatura Hesaplama Sistemi

Sistem aylık ücret üzerine %20 KDV ekleyerek toplam faturayı hesaplar.

Formül:

```text
Toplam Tutar = Aylık Ücret x 1.20
```

Daha sonra math.ceil() fonksiyonu kullanılarak sonuç yukarı yuvarlanır.

---

## Churn (Müşteri Kaybı) Analizi

Sistemde müşterilerin ayrılma riski analiz edilmektedir.

Bir müşteri aşağıdaki koşullardan herhangi birini sağlıyorsa riskli kabul edilir:

* Sadakat süresi 6 aydan az ise
* Aktif müşteri değilse

Örnek çıktı:

```text
Durum: Churn Riski
```

---

## Set Kullanımı

Şirket hizmetleri içerisinde tekrar eden kayıtlar bulunabilir.

Örnek:

```python
["Internet","TV","Internet","Telefon","TV"]
```

Set yapısı kullanılarak tekrar eden veriler kaldırılır:

```python
{"Internet","TV","Telefon"}
```

---

## Kullanılan Dosyalar

```text
main.py
README.md
```

---

## Proje Çıktıları

Program çalıştırıldığında:

* Müşteri bilgileri görüntülenir.
* VIP müşteri kontrolü yapılır.
* Customer ID oluşturulur.
* KDV'li faturalar hesaplanır.
* Churn riski taşıyan müşteriler belirlenir.
* Benzersiz hizmet listesi oluşturulur.
* Güncel tarih rapora eklenir.

---

## Kritik Soruların Cevapları

### Neden Liste Yerine Sözlük Kullanıldı?

Sözlükler verileri anahtar-değer mantığıyla saklar.

Örnek:

```python
musteri["aylik_ucret"]
```

Bu yöntem, liste indeksleri kullanmaya göre daha okunabilir ve daha az hata üretir.

---

### Churn Riski Nasıl Belirlendi?

Sistemde basit bir kural tabanlı yaklaşım kullanılmıştır.

Aşağıdaki müşteriler riskli kabul edilmiştir:

* Sadakat süresi 6 aydan az olanlar
* Aktif olmayan müşteriler

Bu yöntem sayesinde müşteri kaybı yaşanmadan önce gerekli aksiyonların alınması amaçlanmıştır.

---

## Hazırlayan

Sami Yusuf Korkmaz

Akıllı Müşteri Yönetim ve Analiz Sistemi (Telco Senaryosu)
