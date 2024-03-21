# yzm208_bayes_odev
##Giriş (Özet)
Bu çalışma, Naive Bayes sınıflandırma algoritmasının kullanımını ve hiperparametrelerin etkisini incelemeyi amaçlamaktadır. Naive Bayes, makine öğrenmesinde sınıflandırma problemleri için sıkça kullanılan bir olasılık tabanlı bir algoritmadır. Bu çalışmada, diyabet veri seti üzerinde Gaussian Naive Bayes algoritması kullanılarak, veri setinin özelliklerine dayanarak bir kişinin diyabet hastası olup olmadığını tahmin etmek için bir model oluşturulmuştur. Ayrıca, Randomize Search Cross Validation yöntemi kullanılarak en iyi hiperparametrelerin belirlenmesi ve veri setinin güç dönüşümü ve normalizasyonu ile modelin performansının iyileştirilmesi incelenmiştir.

##Metot
###Naive Bayes Algoritması
Naive Bayes sınıflandırma algoritması, Bayes teoremi temel alınarak çalışır. Temel varsayım, bağımsız değişkenler arasındaki ilişkisizliktir, yani değişkenler arasındaki ilişkinin yokluğu varsayılır. Diyabet veri seti için kullanılan Gaussian Naive Bayes algoritması, bağımsız değişkenlerin normal dağılıma sahip olduğunu varsayar.

Model, eğitim veri setindeki her bir sınıf için özelliklerin olasılık yoğunluk fonksiyonlarını tahmin eder. Ardından, test veri setindeki özelliklerin bu olasılık yoğunluk fonksiyonlarına göre hangi sınıfa ait olduğunu tahmin eder. En yaygın kullanılan Gaussian Naive Bayes modelinde, özelliklerin her biri için bir normal dağılım varsayar ve bu dağılımların parametreleri (ortalama ve varyans) eğitim veri setinden tahmin edilir.

###Veri Manipülasyonu ve Normalizasyon
Veri manipülasyonu ve normalizasyon adımları, veri setinin işlenmesi ve model performansının artırılması için uygulanmıştır. İlk olarak, veri seti, bağımsız değişkenlerin hedef değişkeni etkileme şeklini belirlemek amacıyla hedef değişken (Outcome) hariç alınarak bölünmüştür. Ardından, veri seti üzerinde PowerTransformer normalizasyonu uygulanmıştır. Bu normalizasyon yöntemi, veri setindeki özelliklerin normal dağılıma dönüştürülmesini sağlar. Bu dönüşüm, modelin daha iyi performans göstermesine yardımcı olur ve aykırı değerlerin etkisini azaltır.

##Sonuçlar ve Yorum
Bu çalışma, Gaussian Naive Bayes algoritmasının diyabet veri seti üzerindeki performansını incelemiştir. İlk olarak, model varsayılan hiperparametrelerle eğitilmiş ve test edilmiştir, bu durumda elde edilen doğruluk (accuracy) oranı yaklaşık olarak %76 idi. Daha sonra, Randomize Search Cross Validation yöntemi kullanılarak en iyi hiperparametreler belirlenmiş ve modelin performansı iyileştirilmiştir. Ayrıca, veri seti üzerinde güç dönüşümü ve normalizasyonu uygulanarak verinin dağılımı düzeltilmiştir. Bu optimizasyon ve veri manipülasyonu adımlarından sonra, modelin doğruluk oranı yaklaşık olarak %80'e yükselmiştir.

Sonuçlar, Gaussian Naive Bayes algoritmasının diyabet teşhisi için etkili bir yöntem olduğunu ve uygun hiperparametrelerle ve veri manipülasyonuyla modelin performansının artırılabileceğini göstermektedir. Bu çalışma, diyabet teşhisinde makine öğrenmesi tekniklerinin kullanımını ve modelin iyileştirilmesi için yapılabilecek adımları göstermektedir.
