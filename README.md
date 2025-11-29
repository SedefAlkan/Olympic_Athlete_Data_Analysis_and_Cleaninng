# 🏅 Olympic Athlete Data Analysis & Cleaning

Bu proje, olimpiyat sporcularına ait büyük bir veri seti üzerinde **veri temizleme, eksik veri doldurma, tutarsız veri giderme ve temel görselleştirme** işlemlerinin uygulanmasını içerir. Ham veri, yoğun eksik değer içerdiği için analiz yapılabilir hâle getirilmiş ve temiz bir veri seti elde edilmiştir.

---

## 🎯 Projenin Amacı

Bu çalışma, gerçek dünyadan alınmış büyük bir veri seti üzerinde:

- Eksik verileri tespit etmek  
- Uygun yöntemlerle eksik değerleri doldurmak  
- Veri içindeki tutarsızlıkları gidermek  
- Sayısal değişkenlerin dağılımlarını incelemek  
- Histogram ve boxplot gibi temel grafiklerle veriyi yorumlamak  

gibi **veri temizleme (data cleaning)** odaklı bir uygulamadır.

Bu proje bir makine öğrenimi modeli veya ileri seviye analiz içermez; amacı veri ön işleme sürecini göstermektir.

---

## 📂 Proje İçeriği

Aşağıdaki işlemler uygulanmıştır:

### ✔ 1. Veri Setinin Yüklenmesi  
- `athlete_events.csv` dosyası okunmuştur  
- Sütun isimleri Türkçeleştirilmiştir  
- Kullanılmayan sütunlar (`id`, `uok`) kaldırılmıştır

### ✔ 2. Eksik Veri Analizi  
- Boy ve kilo sütunlarında çok sayıda eksik veri bulunmuştur  
- Yaş sütununda eksik değerler tespit edilmiştir  
- Madalya bilgisi olmayan 231.333 satır olduğu görülmüştür  

### ✔ 3. Eksik Verilerin Doldurulması  
Eksik değer doldurma adımları:

- Her **Etkinlik (Event)** için Boy ve Kilo ortalamaları hesaplanmış  
- Etkinliğin ortalaması yoksa genel ortalama kullanılmış  
- Yaş sütunu, tüm veri setinin ortalamasıyla doldurulmuştur

### ✔ 4. Madalya Almayan Sporcuların Çıkarılması  
- `Madalya` sütunu boş olan tüm satırlar silinmiştir  
- Veri seti **271.116 satırdan → 39.783 satıra** düşmüştür

### ✔ 5. Temizlenmiş Verinin Kaydedilmesi  
- Temiz veri `olimpiyatlar_temizlenmis.csv` olarak dışa aktarılmıştır

### ✔ 6. Temel Görselleştirme  
Sayısal değişkenler için histogram çizilmiştir:

- Yaş  
- Boy  
- Kilo  
- Yıl  

Ayrıca “Yaş” değişkeni için bir kutu grafiği (boxplot) oluşturulmuştur.

---

## 📊 Projede Kullanılan Grafikler

- Histogram  
- Boxplot  

Bu grafikler veri dağılımını ve aykırı değerleri incelemek için kullanılmıştır.

---

## 🧠 Elde Edilen Genel İçgörüler

- Boy ve Kilo sütunlarında yüksek eksik veri bulunmuştur  
- Etkinlik bazlı ortalama doldurma yöntemi veriyi daha gerçekçi hale getirmiştir  
- Madalya almayan sporcuların çıkarılması daha anlamlı bir analiz çerçevesi oluşturmuştur  
- Yaş dağılımı genel olarak 20–30 yaş arasında yoğunlaşmaktadır  
- Sayısal değişkenler büyük oranda mantıklı aralıklarda seyretmektedir  

---

## 📁 Proje Yapısı

```text
Olympic Athlete Data Analysis & Cleaning
│
├── Veri okuma
├── Sütun adlarının düzenlenmesi
├── Gereksiz sütunların kaldırılması
├── Event bazlı ortalama ile Boy/Kilo doldurma
├── Yaş değişkeninin doldurulması
├── Madalya almayan sporcuların çıkarılması
├── Temiz verinin kaydedilmesi
└── Histogram + boxplot ile görselleştirme
