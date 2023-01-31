# Natural_Language_Processing

![image](https://user-images.githubusercontent.com/115104812/215753040-7e0e1cf7-ee55-4530-a8e6-4b9930c0aa41.png)

![image](https://user-images.githubusercontent.com/115104812/215753246-47915e20-c0eb-47e9-9262-7a0d42707317.png)
 <p>
 Unutma Kapısı(Forget Gate): Hangi bilgilerin unutulacağı veya tutulacağı kararına varan kapıdır. Önceki hücreden gelen bilgi(ht) ve mevcut bilgi(xt) sigmoid aktivasyon fonksiyonuna sokulur ve sonucuna göre karar verilir. 0 olan bilgiler unutulur ve 1 olan bilgiler Cell State ile taşınmaya devam eder.
 <p>
 Giriş Kapısı(Input Gate): Cell State güncellemesi yapar. Önceki ve mevcut bilginin sigmoid işlemi sonucuna göre güncelleme yapıp yapılmayacağı kararına varılır. 0 olan bilgi önemsiz ve 1 olan bilgi önemli olarak kabul edilir. Ayrıca ağı düzenleme(regulate) işlemi için veriyi -1 ve 1 aralığına sıkıştıran tanh aktivasyon fonksiyonu da kullanılır. Daha sonrasında sigmoid ve tanh fonksiyonu çıkışları çarpılır ve hangi bilginin güncelleneceği kararına varılır.
 <p>
 Çıkış Kapısı(Output Gate): Çıkış kapısı ise bir sonraki hücrenin girişini(ht+1) belirler. Ayrıca tahmin yapmak için de kullanılır. Öncelikle önceki bilgiyi ve mevcut girişin bilgisini sigmoid fonksiyondan geçiririz. Daha sonra Cell State üzerinde var olan bilgiyi tanh fonksiyonundan geçiririz. Son olarak iki sonucu çarparak hangi bilgilerin bir sonraki hücre için giriş(ht+1) olacağına karar veririz. Mevcut hücre için kapı işlemleri tamamlandığında bir sonraki hücreye gidecek olan Cell State ve hücrenin giriş bilgisi olarak tanımladığım Hidden State(ht) bilgilerine karar verilmiş olur.
 <p>
