Genel anlamı ile bir veri kümesinin sıklığını değiştirmek ya da istatistiksel olarak veriden yeni örnekler üretmek için kullanılan bir tekniktir. 2 yöntemi var.

1- Zaman Serilerinde Resampling

Zaman serisi verilerinde, verinin gözlemlenme sıklığını arttırmak veya azaltmak için kullanılır. 

* Aşağı Örnekleme (Down-sampling)
	Veriyi daha düşük bir frekansa çeker. Bu işlem temelinde bir veri toplama (aggregation) işlemidir.
	Örnek: Günlük veriden yıllık ortalama alır. 
	
	Ana amaç: imbalanced datasetlerde (sınıfların dengesiz olduğu durumlarda) kullanılan bir tekniktir. 
	Majority yani baskın olan classtan veri azaltılır.
	
	* Avantajları
		1- Basit ve hızlıdır, büyük datasetlerde işe yarar.
		2- Overfitting riskini azaltabilir, majority class'ın baskınlığını engeller.
		3- Eğitim süresini azaltır çünkü veri azalır.
	* Dezavantajı
		1- En büyük problem veri kaybı
	 

* Yukarı Örnekleme (Oversampling)
	Veriyi daha yüksek bir frekansa çeker. Minority olan (az olan) sınıfın örnek sayısını yukarı arttırma işlemidir. 
	Amaç:
	* Modelin minority class'ını daha iyi öğrenmesini sağlamak.

	* Avantajları
		1- Bilgi kaybı olmaz, çünkü veri silinmez.
		2- Minority class daha iyi öğrenir.
	* Dezavantajı
		1- Aynı veriyi tekrar tekrar gösteriyoruz, model gerçek bir pattern öğrenmek yerine, mevcut veriyi ezberleyebilir.
		2- Veri çeşitliliği artmaz, sadece tekrar var.

Minority classı arttırmaya yönelik yaygın kullanılan en önemli yöntemlerden biri de [[SMOTE (Synthetic Minority Over-sampling Technique)]]'tur.
