# Ses Tanıma Algoritması ile Ortamdaki Kişi Sayısını Tespit Eden Gömülü Sistem

## Proje Açıklaması
Bu proje, ses tanıma algoritmaları kullanarak bir ortamda bulunan kişi sayısını tespit eden bir gömülü sistem geliştirmeyi amaçlamaktadır. Sistem, mikrofon aracılığıyla alınan ses verilerini analiz ederek konuşmacı sayısını gerçek zamanlı olarak belirleyebilmektedir.

Bu çalışma, TÜBİTAK 2209-A Araştırma Projesi kapsamında gerçekleştirilmiştir.

---

## Amaç
- Ortamdaki kişi sayısını ses verisi üzerinden tahmin etmek  
- Kamera kullanmadan, mahremiyeti koruyan bir çözüm geliştirmek  
- Gömülü sistem üzerinde gerçek zamanlı ses analizi gerçekleştirmek  

---

## Kullanılan Teknolojiler

### Donanım
- Raspberry Pi 5 (8GB)
- MAX9814 Mikrofon Modülü
- MCP3204 ADC Entegresi

## Kaynak Kodlar

- Kaynak kodlara buradan erişebilirsiniz: [src](src/)

### Kullanılan Kütüphaneler
- pyannote.audio
- Hugging Face
- noisereduce
- webrtcvad
- matplotlib

---

## Sistem Çalışma Mantığı

Sistem aşağıdaki adımlar üzerinden çalışmaktadır:

1. Mikrofon ortam sesini algılar  
2. Analog ses sinyali ADC ile dijital veriye dönüştürülür  
3. Gürültü azaltma ve ses ön işleme uygulanır  
4. Ses aktivite tespiti ile konuşma bölümleri belirlenir  
5. pyannote.audio modeli ile konuşmacı analizi yapılır  
6. Konuşmacılar gruplanarak kişi sayısı belirlenir  

---

## Dokümanlar

- 📄 Araştırma Önerisi Formu:[Görüntüle](https://raw.githubusercontent.com/sedakoroglu/Ses_Tanima_Algoritmasiyla_Kisi_Tespiti/main/arastirma_onerisi_rapor.docx)
- 📄 Proje Raporu:[Görüntüle](https://raw.githubusercontent.com/sedakoroglu/Ses_Tanima_Algoritmasiyla_Kisi_Tespiti/main/ses_ile_kisi_tespiti_rapor.pdf)

---

## Bağlantı Şeması

![Bağlantı Şeması](images/baglanti_semasi.jpeg)

---

## Test ve Sonuçlar

Yapılan testlerde sistem:

- Tek konuşmacılı ortamda %100 doğruluk sağlamıştır  
- Çoklu konuşmacı (sıralı konuşma) durumlarında doğru tespit yapmıştır  
- Gürültülü ortamlarda da başarılı sonuçlar vermiştir  

Ancak:
- Aynı anda konuşma (çakışmalı konuşma) durumlarında hata payı artmaktadır  

---

## Sonuç

Bu proje kapsamında, ses tabanlı kişi sayısı tespiti yapan bir gömülü sistem başarıyla geliştirilmiştir. Sistem, özellikle sıralı konuşmaların olduğu ortamlarda yüksek doğrulukla çalışmaktadır.

Proje, akıllı bina sistemleri, enerji verimliliği ve otomasyon uygulamaları için kullanılabilecek potansiyele sahiptir.

---

## Gelecek Çalışmalar

- Çakışmalı konuşmalar için algoritma iyileştirmesi  
- Akıllı sistemlerle entegrasyon  
- Ürünleştirme ve ticarileştirme  
- Daha gelişmiş yapay zeka modellerinin kullanımı  

---

## Not

Bu proje TÜBİTAK 2209-A Araştırma Projesi kapsamında geliştirilmiştir.







