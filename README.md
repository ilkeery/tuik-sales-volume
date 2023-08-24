# tuik-sales-volume
SARIMA ile TÜİK Perakende Satış Hacim Endeksi Tahmini

# Genel Bilgiler
Perakende Satis Hacim Endeksi ve Degisim Oranlari (sabit fiyatlarla) (2015=100)
TÜİK'ten alınmıştır. https://data.tuik.gov.tr/Bulten/Index?p=Perakende-Satis-Endeksleri-Kasim-2022-49615#:~:text=T%C3%9C%C4%B0K%20Kurumsal&text=Sabit%20fiyatlarla%20perakende%20sat%C4%B1%C5%9F%20hacmi,ise%20%253%2C9%20artt%C4%B1.

Ayrıca TÜİK Ciro endeksi de yayınlamaktadır.

2015 Yılındaki hacim = 100 kabul edilerek Türkiye'deki farklı sektörlerdeki satış hacimlerini göstermektedir.

Bu sektörler ;

1. Perakende ticaret

2. Gıda, içecek ve tütün

3. Gıda dışı (otomotiv yakıtı hariç)

4. Bilgisayar, bilgisayar donanım ve yazılımları, kitap, iletişim aygıtları vb.

5. Ses ve görüntü cihazları, hırdavat, boya ve cam, elektrikli ev aletleri, mobilya vb.

6. Tekstil, giyim ve ayakkabı

7. Eczacılık ürünleri,  tıbbi ve ortopedik ürünler, kozmetik ve kişisel bakım malzemeleri

8. Posta yoluyla veya internet üzerinden

9. Otomotiv yakıtı

# Hedefler

Sektörlerin gelecekteki satış hacimlerinin tahmin edilerek, başta kobiler olmak üzere şirketlerin bulundakları sektörlerin gelecekteki satış hacimlerine bakarak aksiyon alabilmelerini sağlamak.

Birbirlerini pozitif/negatif etkileyen sektörler var mı? Varsa gelecek öngörülerek bir erken uyarı sistemi oluşturulabilir mi?

TÜİK sezonsallıktan arındırılmış ve arındırılmamış veri sunuyor. ARIMA , SARIMA ve SARIMAX gibi modellerin test edilerek hangisinin en iyi sonucu verdiğinin test edilmesi.

# Model Eğitimi

Literatür taramasında farklı tekniklerle farklı modellerin kullanıldığı görülmüştür. Bu nedenle  ARIMA , SARIMA , SARIMAX modellerinden başlanarak XGBoost, SVR modelleri eğitilecektir.

Bu bir örnek olduğu için sadece SARIMA modeli eğitilecektir.

> Rolling Origin Forecasting

SARIMA modelinin bir sonraki ayı tahmin etmesi sağlanarak her tahmin ettiği ayı eğitimde kullanarak yeni bir model eğitilecek ve her aydan sonra o ayı da eğitiminde kullanan yeni bir SARIMA modeliyle süreç devam ettirilecektir.
# Değerlendirme

Henüz karar verilmedi. Literatürde MAPE, MAE, MSE gibi farklı sebeplerle farklı değerlendirme metrikleri kullanılmış.
