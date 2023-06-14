
# Classification Problemlerinde Güvenilirliğin Tespiti: Sensitivity, Specificity

Arkadaşlar merhaba. Bu yazıda da daha önceki yazıların ana konusuna bağlı kalarak model performans metrikleri üzerine olacak. Sınıflandırma problemlerinde modelin performansını değerlendirmek için bir çok argüman olduğundan bahsetmiştik. Bunlardan bir tanesi de confusion matrix olarak bilinen karşıtlık matrisleridir.

![image](https://github.com/tr-brain-com/dss/assets/118043046/17a2a79e-9054-4b25-9923-bc07f68f99e5)

Karşıtlık matrisleri, test verilerinin gerçek değerleri biliniyorsa belirlenebilir. Öngörülen ve gerçekleşen değerlerin 4 farklı kombinasyonundan oluşan bir tablodur. Geri Çağırma (Recall), Hassasiyet (Sensitivity), Özgüllük (Specificity), Doğruluk (Accuracy) ve en önemlisi AUC-ROC eğrilerini ölçmek için son derece kullanışlıdır.

Teşhis testlerinin performansı birkaç noktada belirlenebilir. Duyarlılık ve özgüllük bunlardan ikisidir. Kısacası: %100 hassasiyetle hasta olan herkes doğru bir şekilde hasta olarak tanımlanır. %100 özgüllükte hiç kimse yanlış pozitif test sonucu almaz. Her iki alanda da %100 puan alan testler aslında çok nadirdir. Bu, her zaman yanlış bir şekilde hasta veya sağlıklı olarak tanımlanan bireylerin olacağı anlamına gelir. Pazar için bir teşhis testi geliştirirken, her zaman menfaatleri dengeleme meselesidir.

# Hassasiyet (Sensitivity) ne ifade ediyor?

Hassasiyet, gerçek pozitif oran olarak (TPR) ifade edilir ve bir testte pozitif sonuç veren gerçekten de pozitif olan örneklerin oranıdır. Bunu bir örnekle açıklayalım. Örneğin bi test de ki pozitif örnekleri %70 oranında pozitif olarak tespit eden bir modelin, aynı testi %90 oranında pozitif tespit eden bir modele göre hassasiyetinin daha düşük olduğunu söyleyebiliriz. Peki nasıl hesaplanır ? Bunu bir önceki yazı dizisinde belirtmiştik.

Bir testin hassasiyetini hesaplamak için aşağıdaki denklem kullanılır:

![image](https://github.com/tr-brain-com/dss/assets/118043046/9bac0bc6-f2c9-4260-9204-712d9f9bf6cb)

# Özgüllük (Specificity) ne ifade ediyor?

Özgüllük, gerçek negatif oran olarak (TNR) ifade edilir ve bir testte negatif sonuç veren gerçekten de negatif olan örneklerin oranıdır. Bunu da bir örnekle açıklayalım. Örneğin, tüm sağlıklı insanları belirli bir hastalık için negatif olarak tanımlayan bir test çok özgüldür. Sağlıklı insanların %30'unun hastalığa sahip olduğunu yanlış bir şekilde tanımlayan başka bir test, daha yüksek yanlış pozitif oranına (FPR) sahip olarak daha az özgül olarak kabul edilecektir.

Bir testin özgüllüğünü hesaplamak için aşağıdaki denklem kullanılır:

![image](https://github.com/tr-brain-com/dss/assets/118043046/ada1eb25-478c-451f-8827-144ca80cd1a7)


Yazı serisinin tamamını okumak için [tıklayınız](https://www.brain-tr.com/classification-problemlerinde-guvenilirligin-tespiti-sensitivity-specificity/https://www.brain-tr.com/pca-principal-component-analysis-kullanarak-boyut-azaltma-nasil-gerceklestirilir/).

Notebook dosyası için [tıklayınız](https://github.com/tr-brain-com/dss/blob/main/diabetes_sensitivity_specificity/app.ipynb).
