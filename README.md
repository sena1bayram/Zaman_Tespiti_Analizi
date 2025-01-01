# Zaman Serisi Analizi Projesi 📊

Bu proje, zaman serisi verilerini analiz etmek, trendleri tespit etmek ve gelecekteki değerleri tahmin etmek için hem **Python** hem de **KNIME** aracılığıyla gerçekleştirilmiştir. Finansal zaman serileri üzerinde ARIMA modeli kullanılarak tahminleme yapılmış ve çıktılar detaylı bir şekilde değerlendirilmiştir.

---

## Proje Amaçları 🚀

- Zaman serisi verilerinin yapısını analiz etmek.
- Trend, mevsimsellik ve düzensizlikleri belirlemek.
- ARIMA modeliyle en uygun parametreleri seçerek tahmin yapmak.
- Python ve KNIME platformlarında çıktıları kıyaslamak.

---

## Kullanılan Veri Seti 📂

- **Veri Kaynağı:** Zaman serisi analizine uygun finansal veri seti (Tesla hissesine ait kapanış fiyatları).
- **Değişkenler:**
  - `Date`: Tarih bilgisi.
  - `Adj Close`: Ayarlanmış kapanış fiyatı.

Veri seti, eksik değerlerin doldurulması ve trend/mevsimsellik bileşenlerinin ayrıştırılması gibi ön işlemlerden geçirilmiştir.

---

## Python Uygulama Adımları 🔄

1. **Veri Hazırlık:**
   - Tarih formatı dönüştürüldü ve indeks olarak ayarlandı.
   - Eksik değerler dolduruldu.

2. **Durağanlık Testi:**
   - ADF testiyle serinin durağan olup olmadığı kontrol edildi.
   - Durağan olmayan seriler fark alınarak durağan hale getirildi.

3. **Modelleme:**
   - Grid search ile ARIMA modelinin optimal (p, d, q) parametreleri belirlendi.
   - En iyi model AIC ve RMSE skorlarına göre seçildi.

4. **Tahmin ve Performans Analizi:**
   - Test seti üzerinde RMSE ve MAE gibi metriklerle model performansı değerlendirildi.
   - Gelecekteki 30 gün için tahmin yapıldı.

---

## KNIME Uygulama Adımları 🫰

1. **Veri Hazırlık:**
   - CSV Reader düğümü ile veri seti yüklenip temizlendi.
   - Tarih formatı dönüştürüldü ve eksik değerler dolduruldu.

2. **Modelleme:**
   - ARIMA Learner düğümü ile model parametreleri optimize edildi.
   - En iyi model, test seti üzerinde çalıştırılarak tahmin yapıldı.

3. **Görsel Analiz:**
   - Line Plot ile gerçek değerler ve tahminler karşılaştırıldı.

---

## Sonuçlar ve İyileştirme Önerileri ✅

- **Python Sonuçları:**
  - Test setindeki RMSE: 12.15, MAE: 7.37.
  - Tahminler genel trendi yakalamakta başarılı, ancak bazı tahminlerde hata oranı yüksek.

- **KNIME Sonuçları:**
  - Hata metrikleri ve görseller, modelin trend tahminlerinde benzer bir başarı gösterdiğini ortaya koydu.

- **İyileştirme:**
  - Verideki uç değerlerin etkisini azaltmak için ek ön işleme adımları uygulanabilir.
  - Heteroskedastisite sorunları için daha karmaşık modeller (GARCH gibi) kullanılabilir.

---

## Nasıl Kullanılır? 🔧

### Python İçin:
1. Gerekli kütüphaneleri yükleyin:
   ```bash
   pip install pandas numpy matplotlib statsmodels scikit-learn
   ```
2. Proje kodunu çalıştırın:
   ```bash
   python zaman_serisi.py
   ```

### KNIME İçin:
1. KNIME Analytics Platform'u indirin ve kurun.
2. Proje workflow'unu açın ve düğümleri çalıştırın.

---

## Kaynaklar 📖

- [ARIMA Modelleme](https://tr.wikipedia.org/wiki/Zaman_serisi)
- [KNIME Blog](https://www.knime.com/blog/building-a-time-series-analysis-application)
- [Python ile Zaman Serisi Analizi](https://miuul.com/blog/veri-biliminde-zaman-serileri)

---

Proje ile ilgili sorularınız için lütfen benimle iletişime geçin! 😊
