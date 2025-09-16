# 🩺 Semptom Verilerine Dayalı Diyabet Risk Tahmini

Diyabet, dünya genelinde milyonlarca insanın yaşam kalitesini etkileyen ve sağlık sistemleri üzerinde önemli bir yük oluşturan kronik bir hastalıktır. Erken teşhis ve etkili yönetim, komplikasyonların önlenmesinde kritik bir rol oynamaktadır. Bu çalışmada, diyabet riskinin tahminine yönelik bir makine öğrenmesi analizi gerçekleştirilmiştir. Semptom ve demografik veriler kullanılarak Logistic Regression, Random Forest ve XGBoost gibi algoritmalarla risk tahmini yapılmıştır. Analizler sonucunda, Random Forest modeli %99,36 doğruluk ve 1,00 AUC ile en yüksek performansı göstermiştir. Ayrıca, predict_proba yöntemleriyle bireysel risk yüzdeleri hesaplanmış ve sonuçlar klinik karar destek sistemlerine entegre edilebilecek değerli bilgiler sunmaktadır.

---

## 🎯 Proje Hedefleri

- Diyabet riskini erken ve doğru şekilde tahmin etmek.  
- Semptom verilerinin makine öğrenmesi modelleri üzerindeki etkisini analiz etmek.  
- Farklı algoritmaların performanslarını karşılaştırmak.  
- Sağlık verileriyle çalışan karar destek sistemleri için referans oluşturmak.  

---

## 🧩 Veri Seti

- **Kaynak:** [Early Stage Diabetes Risk Prediction Dataset - UCI](https://archive.ics.uci.edu/dataset/529/early+stage+diabetes+risk+prediction+dataset)  
- **Özellikler:**  
  - `age`: Yaş  
  - `gender`: Cinsiyet (Kadın/Erkek)  
  - Semptomlar: Bulantı, halsizlik, susuzluk, sık idrara çıkma vb.  
- **Hedef Sütun:** `class`  
  - `0` → Diyabet Değil  
  - `1` → Diyabet  

---

## 🔬 Kullanılan Yöntemler

1. **Veri Ön İşleme**  
   - Eksik değer kontrolü ve temizleme.  
   - Kategorik değişkenlerin Label Encoding ile sayısallaştırılması.  
   - Özelliklerin StandardScaler ile ölçeklendirilmesi.  

2. **Keşifsel Veri Analizi (EDA)**  
   - Özet istatistikler.  
   - Korelasyon analizi ve ısı haritaları.  
   - Yaş ve cinsiyet dağılımı.  
   - Semptom bazlı analizler.  

3. **Veri Dengesizliği Çözümü**  
   - **SMOTE** ile sınıf dengesizliği giderildi.  

4. **Makine Öğrenmesi Modelleri**  
   - Logistic Regression  
   - Random Forest  
   - K-Nearest Neighbors (KNN)  
   - Support Vector Machine (SVM)  
   - Naive Bayes  
   - XGBoost  

5. **Model Değerlendirme**  
   - Doğruluk (Accuracy)  
   - Kesinlik (Precision)  
   - Duyarlılık (Recall)  
   - F1-Score  
   - Confusion Matrix görselleştirmeleri  

6. **Özellik Önemi Analizi**  
   - Random Forest modeli ile semptomların risk üzerindeki etkileri değerlendirildi.  

7. **Bireysel Risk Analizi**  
   - `predict_proba` yöntemi ile her birey için diyabet olma olasılıkları hesaplandı.  
   - Risk yüzdeleri, klinik karar destek sistemlerinde kullanılabilecek şekilde yorumlanabilir.  

---

## 📊 Sonuçlar

- **Random Forest modeli**, %99,36 doğruluk ve **1,00 AUC** ile en iyi performansı sergiledi.  
- XGBoost ve Logistic Regression modelleri de güçlü performans gösterdi.  
- Analizler, belirli semptomların diyabet tahmininde kritik rol oynadığını ortaya koydu.  
- Bireysel risk yüzdeleri hesaplanarak klinik karar süreçlerine katkı sağlandı.  

---

## 📂 Proje Yapısı

