# Sports-Analytics-Athlete-Performance-Evaluation-Sporcu-Performans-De-erlendirme-Analizi
Veri analitiği ve makine öğrenmesi algoritmaları ile sporcu performans sınıflandırması ve tahmini.
# Sporcu Performans Analizi ve Makine Öğrenmesi ile Tahminleme

Bu proje, sporcuların fiziksel özellikleri, yaşam alışkanlıkları (uyku, beslenme), antrenman rutinleri ve demografik yapıları gibi parametreleri inceleyerek **Performans Sınıflarını** ve akademik performans çıktılarını tahmin etmeyi amaçlayan uçtan uca bir veri bilimi çalışmasıdır.

# Proje Amacı
Spor endüstrisinde veri analitiği, sporcu gelişimini optimize etmek ve başarıyı öngörmek için kritik öneme sahiptir. Bu projede, sporculardan toplanan çok boyutlu veriler temizlenerek ön işleme tabi tutulmuş; ardından denetimli öğrenme (supervised learning) algoritmaları kullanılarak sınıflandırma ve regresyon modelleri geliştirilmiştir.

## Veri Seti Yapısı
Projede `Dataset3.xlsx` dosyası girdi olarak kullanılmaktadır. Veri seti 600 sporcu kaydı ve şu temel öznitelikleri (features) içerir:
- **Demografik & Genel Bilgiler:** Yaş, Cinsiyet, Şehir, Sporcu_Bütçe_TL
- **Spor & Antrenman Geçmişi:** Spor_Dalı, Deneyim_Yılı, Kulüp_Tipi, Antrenman_Sıklığı, Antrenman_Yükü_dk, Yarışma_Sayısı
- **Fiziksel & Sağlık Göstergeleri:** Boy_cm, Kilo_kg, VO2max, Dinlenim_Nabzı_bpm, Sakatlık_Gün_Yıl
- **Yaşam Tarzı:** Motivasyon_Düzeyi, Beslenme_Tipi, Uyku_Saat, Protein_Alımı_gr
- **Hedef Değişken:** Performans_Sınıfı (0, 1, 2, 3 şeklinde sınıflandırılmış performans seviyeleri)

# Kullanılan Teknolojiler ve Kütüphaneler
Proje, Python ekosistemindeki güçlü veri bilimi kütüphaneleriyle Jupyter Notebook ortamında geliştirilmiştir:
- **Veri Manipülasyonu:** `pandas`, `numpy`
- **Veri Görselleştirme:** `matplotlib`, `seaborn`
- **Makine Öğrenmesi (Scikit-Learn):**
  - *Ön İşleme:* `StandardScaler`, `train_test_split`
  - *Sınıflandırma:* `RandomForestClassifier`, `LogisticRegression`
  - *Regresyon:* `RandomForestRegressor`, `LinearRegression`
  - *Metrikler:* `accuracy_score`, `classification_report`, `confusion_matrix`, `r2_score`, `mean_squared_error`

#Uygulama Adımları
1. **Veri Keşfi (EDA):** Eksik verilerin analizi, veri tiplerinin kontrolü ve sınıf dağılımlarının incelenmesi.
2. **Veri Temizleme & Ön İşleme:** Analize katkısı olmayan veya çok yüksek oranda eksik veri içeren (`Sakatlık_Durumu`, `Sporcu_ID` vb.) sütunların kaldırılması.
3. **Özellik Mühendisliği:** Kategorik değişkenlerin kodlanması ve sayısal verilerin standartlaştırılması.
4. **Modelleme & Eğitim:** Verinin eğitim ve test seti olarak bölünmesi, sınıflandırma ve regresyon modellerinin eğitilmesi.
5. **Değerlendirme:** Modellerin doğruluk (accuracy), hata kareler ortalaması (MSE) ve R-kare (R²) skorları üzerinden başarı analizi.
