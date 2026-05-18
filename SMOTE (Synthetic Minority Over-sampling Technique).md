Dengesiz veri setleri için kullanılan en önemli oversampling yöntemlerinden biridir.

Amaç:
- Minority class'ı çoğaltmak. 
- Minority'i çoğaltırken yapay yani sentetik veriler üreterek yapar.

|Class|Adet|
|---|---|
|Normal|98.000|
|Fraud|2.000|
Örneğin yukarıdaki örnekte, model sürekli olarak normal olan class'ı tahmin edecek ve accuracy score'u çok yüksek çıkacaktır. Fraud örneği çok az görülür.

*** Smote'un Temel Fikri:
- Mevcut minority örneklerini kullanır
- Onların arasında yeni veri noktaları üretir. Yani gerçekçi gözlemler oluşur.
- Yani a  ile b verileri arasında bir c noktası oluşturur.

Python kullanımı

```
from imblearn.over_sampling import SMOTE

smote = SMOTE(random_state=42)

X_resampled, y_resampled = smote.fit_resample(X, y)

```

### En kritik parametre: k_neighbors

SMOTE yeni veriler üretirsen en yakın komşulara bakar. Verilen sayıya göre, örneğin 5 verilirse en yakın 5 komşuya bakar.

* Avantajları
	1- Overfitting Azalır
		Oversampling gibi kopya üretmez.
		
	2- Minority Class öğrenmesini arttırır.
		- Recall ve f1-score iyileşebilir.
	
- Dezavantajları
	1- Noise üretme riski
		Eğer minority class çok dağınıksa ve outlier içeriyor ise saçma veri noktaları oluşabilir