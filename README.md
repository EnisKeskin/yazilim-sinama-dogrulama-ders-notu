# Yazılım Test Düzeyleri

- Yazılım projelerinde testler temelde dört farklı aşamada gerçekleştirilir.
- Bu testlerin ayrıntı düzeyi artıkça test edilen parçanın büyüklüğü azalır. Bu test aşamaları aşağı-daki gibidir:

1. Birim Testler
2. Yazılım Tümleştirme Testleri
3. Sistem Testleri
4. Kabul Testleridir.

ilerleyen ayrıtlarda bu aşamalar ele alınmıştir.

## 4.1. Birim Testler

- Yordam, fonksiyon veya prosedür gibi bir kod parçasının kendisinden beklenen iş-levselliği doğru olarak yerine getirdiğini ve hata içermediğini göstermek için gerçekleştirilen testlerdir [Myers-1979].
- Birim testler bazen proje takviminden, bazen yeterli tecrübe olmayışından, bazen de gereken önemin verilmesinden dolayı acele ile geçiştirilirler veya ihmal edilirler.
- Aslında birim testler başarılı ve kaliteli yazılım ürünleri ortaya çıkartmak için kullanılabilecek olan önemli bir test aşamasıdır.
- Eğer bir yazılım projesinde birim testler başarılı bir şekilde gerçekleştirilirse, diğer test aşamalarında daha başarılı sonuçlar alınacaktır [Myers-1979].

- Birim testi yapılmasının en rahat yolu bir yazılım test aracı kullanılmasıdır.
- Eğer bir test yazılım aracı kullanılmayacak ise birim test kodları yazılım geliştirmeye paralel olarak geliştirilmelidir.
- Bu nedenle birim testler yazılım geliştirmenin bir parçası olarak düşünülmeli ve planlama buna uygun olarak gerçekleştirilmelidir.
- Gereksi-nimler veya kod güncellendikçe, birim test kodları da güncellenmelidir.

- Başarıyla sonuçlanan birim testler, yazılım tümleştirme ve sistem testlerinden önce geliştirilen yazılı genel olarak istenen gereksinimleri karşıladığı bir göstergesidir.
- Ancak tam olarak ifadesi değildir.Geliştirilen yazılımdan beklenenlerin tam olarak karşılandığını ortaya koymak için entegrasyon vesistem testleri ile arayüzlerin testlerinin de gerçekleştirilmesi gerekir.

- Birim testlerin gerçekleştirilme ayrıntısı geliştirilen yazılımın kullanım alanı ile doğ-rudan ilişkilidir.
- Örneğin tam bir yol kapsama analizinin (path coverage analysis) gerektiği ve kod içerisinde çalıştırılmayan kod parçasının bulunmadığının gösterilmesi istenen emniyet kritik sistem yazılımlarında birim testler daha bir önem arz eder.
- Bu ayrıntıda gerçekleştirilen birim testler daha fazla zaman alır, daha fazla maliyet gerektirir.
- Bu ayrıntıda testlerin gerçekleştirilmesi için test kodlarının yazıl-ması yerine, mutlaka alanında iyi bir test yazılımı kullanılmalıdır.

## Birim Testler Nasıl Gerçekleştirilir?

- Birim testlerinin amacı, geliştirilen ve derlenebilen en küçük kod parçalarının (me-tot, prosedür, fonksiyon, sınıf vb) kendilerine ait görevleri doğru şekilde yerine ge-tirdiğinin doğrulanmasıdır.
- Bu amaçla, birim testler gerçekleştirilirken test edilecek olan birim diğer birimlerden izole edilir.
- Test edilen birim için gerekli olan girdileri sağlayacak diğer,birimlerin yerine o metotların koçanları (stub) kullanılır.
- Böylece diğer birimdeki olası bir hatanın test edilen birimi etkilemesi engellenir.
- Test edilen birimin icra edeceği göreve göre test durumları oluşturulur.
- Bu durumlar kullanılarak test edilecek birim çalıştırılır ve elde edilen sonuçlar beklenen sonuçlar ile karşılaştırılarak testlerin başarılı olup olmadığına karar verilir.
- Eğer test başarısızlıkla sonuçlanmış ise birimin kodu tekrar gözden geçirilir, gerekli düzeltmeler gerçekleştirilir ve tekrar test edilir.
- Bu işlem tüm birimler başarılı bir şekilde kendilerine ait birim testleri geçinceye kadar devam eder.
- Şekil-4.1 de genel birim test süreci görülmektedir.

<center><image src="./image/genelTestBirimleri.png"></image></center>

- Birim test süreci yazılım geliştirme metodolojilerine göre farklılık gösterebilir.
- Örneğin projede test güdümlü (test driven) veya çevik yazılım geliştirme metodolojisi kullanılacaksa birimler yazılmadan önce test kodları yazılır.
- Birim testler yazılım geliştiriciler tarafından gerçekleştirilir.
- Birim testlerin başarılı bir şekilde yapılmasının ilk adımı, süreçte görüldüğü gibi birim test stratejisinin net olarak belirlenmesi ve tüm geliştiricilerin belirlenen bu strateji üzerine eğitimlerinin gerçekleştirilmesidir.
- Bu eğitim sadece birim testleri, birim testlerde kullanılacak olan araçları değil projenin genel test yaklaşımını da kapsamalıdır.

**Birim Testlere Bir Örnek :**

<center><image src="./image/testOrnek.png"></image></center>

bir kapsamaya ulaşılır.

- Yani bu kodun sadece yarısı çalıştırılmış olur.
- Eğer diğer test durumu da koşturulursa kodun geri kalan kısmı da çalıştırılmış olur. Bu iki test du-rumunun koşturulmasıyla bu metot °/0100 kapsamaya ulaşmış olur.
- Yani bu metodun içerisindeki tüm satırlar bu iki test durumu ile en az bir kez çalıştırılmış olur. Kap-sama analizleri birim testlerin kalitesini gösteren bir metriktir.

**Test Durumu 2:**

<center><image src="./image/testDurum2.png"></image></center>

### Birim Testlerde Kapsama Analizi

- Birim testlerde önemli diğer bir konu da kapsamadır.
- Kapsama bir yazılım birimi içerisindeki tüm yol ve karar noktalarmm test edilmesidir.
- Bu durum özellikle emni-yet ve görev kritik sistemler için daha büyük bir önem arz eder.
- Konunun daha iyi anlaşılması için yukarıdaki örnek incelendiğinde yazılan iki test durumu sıra ile koşturulursa, ilk test durumunun koşturulmasıdan sonra bu metot üzerinde % bir kapsamaya ulaşılır.
- Yani bu kodun sadece yarısı çalıştırılmış olur.
- Eğer diğer test durumu da koşturulursa kodun geri kalan kısmı da çalıştırılmış olur.
- Bu iki test du-rumunun koşturulmasıyla bu metot °/0100 kapsamaya ulaşmış olur.
- Yani bu metodun içerisindeki tüm satırlar bu iki test durumu ile en az bir kez çalıştırılmış olur.
- Kapsama analizleri birim testlerin kalitesini gösteren bir metriktir.

### Birim Testlerde Sınır Değer Analizi

- Birim testlerde önemli diğer bir nokta da sınır değerlerin kontrol edilmelidir.
- Bir metot içerisinde belirli bir değer aralığında işlem yapılıyorsa bu değer aralığının alt ve üst smırının kontrol edilmesi gerekir.
- Yazılım testlerinde yazılımcıların en çok hataya düştükleri konuların başında sınır değerlerin yazılım içerisinde uygun bir şekilde kapalı veya açık aralık şeklinde kodlanmamasıdır.
- Yukarıda verilen örnek incelendiğinde k=0 durumunda ne gibi bir sonuçla karşılaşılır? Bu durumun kod içeri-sinde kontrol altına almması gereklidir.
- Bu durum için üçüncü bir test durumu ya-zılmalı ve yazılımcıdan da bu durumda kodun nasıl davranacağı öğrenilerek elde edilen sonuçla karşılaştırılmalıdır.
- Birim testlere genel bir yaklaşım getirmek için IEEE tarafından tanımlanmış bir test standardı vardır [ANSI/IEEE Std 1008-1987].
- Bu standart yazılım projeleri kapsamında gerçekleştirilecek olan birim test eylemlerini genel bir çerçevede tanımla-maktadır.

## 4.2. Tümleştirme Testleri

- Yazılım projelerinde birim testlerin başarılı bir şekilde sonuçlandınlmasından sonra tümleştirme (entegrasyon) testleri başlar.
- Birim testlerde amaç modüllerin ayrı ayrı kendilerinden beklenen işlevleri yerine getirdiğinin doğrulanması iken tümleştirme testlerinin amacı bir araya gelerek entegre edilmiş olan bir yazılımın içerisindeki bileşenlerin birbirleriyle uyum içerisinde doğru bir şekilde çalıştığının ve bileşenlerin kendilerine ait gereksinimleri yerine getirdiğinin doğrulanmasıdır.
- Bu testlerin gerçekleştirilmesi için kullanılacak olan test durumları yazılım gereksinimleri ile arayüz gereksinimlerinden çıkartılır.
- Tümleştirme testlerinde Bölüm 4'de anlatılan kara kutu test yöntemi kullanılır.
- Testlerde hem pozitif hem de negatif test durumları uygun parametreler kullanılarak koşturulur.
- Sonuçlar beklenen değerlerle karşılaştırılarak sistemin kendisinden beklenen davranışları gerçekleştirdiği doğrulanır.

- Tümleştirme testleri gerçekleştirilirken big bang, aşağıdan-yukarıya veya yukarıdan-aşağıya olmaz üzere farklı stratejiler kullamlabilir.

- Big bang stratejisine göre geliştirilen tüm üst ve alt düzey modüller birbirleriyle en-tegre edildikten sonra testler başlar.
- Bu stratejide sistem bir bütün olarak ele alınarak testler icra edildiğinden testlerin gerçekleştirilmesi hızlıdır ve zamandan tasarruf edilir.
- Ancak bir hata çıkması durumunda bu hatanm hangi seviye katmanda oluştuğu veya hangi modülden kaynaldandığının tespitinde zorluklar yaşanabilir twu-20o1. Şekil-4.2 de big bang test yaklaşımı örneklendirilmiştir.

<center><image src="./image/bigBangTest.png"></image></center>

**Aşağıdan-yukarıya** tümleştirme test stratejisi öncelikle birim testlerin yapılmasıyla başlar.

- Birim testleri başarıyla tamamlanan alt düzey modüller birbirleriyle entegre edilir.
- Bu entegrasyondan sonra alt düzey modüller ile ilgili entegrasyon testleri icra edilir.
- Bu testlerin başarılı bir şekilde sonlandırılmasından sonra bir üst katman mo-dülleri sisteme entegre edilir ve gerekli entegrasyon testleri icra edilir.
- Bu entegrasyon tüm sistem inşa edilinceye ve entegrasyon testleri başarıyla sonuçlanıncaya kadar devam eder.
- Bu yaklaşımda temel şart, entegre edilecek modüllerin birim testlerinin başarıyla tamamlanmış olmasıdır.
- Bu yaklaşım ile hedeflenen sistemin yüzdelik olarak ne kadarımn tamamlandığı ve test edildiği kolay bir şekilde belirlenebilir.
- Aşagıdan-yukarıya entegrasyon test stratejisi paralel programlama, döngüsel yazılım geliştirme metodolojileri için uygun bir test yaklaşımıdır.
- Şekil-4.3 de aşağıdan-yukarıya test yaklaşımı örneklendirilmiştir.

**Yukarıdan-aşağıya** tümleştirme test stratejisi, öncelikle sistem için en üst modülün (en dış modül, genellikle kullanıcı grafik arayüz modülü) test edilmesi ile başlar.

- Bu modülün ihtiyaç duyduğu alt modüllerin koçanları kullanılır.
- Bu yaklaşımda birçok koçan yazılması gerekir.
- En üst modül başarılı şekilde test edildikten sonra bir alt düzey modüller sistemle bütünleştirilir.
- Bu entegrasyondan sonra gerekli alt düzey tümleştirme testleri icra edilir.
- Bu durum en alt düzey modüller entegre edilinceye ve entegrasyon testleri başarıyla sonuçlanıncaya kadar devam eder.
- Bu yaklaşımda entegrasyon testleri kara kutu testleri olarak başlar ve gittikçe saydam kutu testlerin döner.
- Şekil-4.4 de yukarıdan-aşağıya test yaklaşımı örneklendirilmiştir.

<center><image src="./image/asagidanYukari.png"></image></center>

- Entegrasyon testleri koşturulan test durumlarmın geçme sayısı belirli bir orana ulaş-tığında veya tamamı geçtiğinde tamamlanmış olur.
- Bu aşamada bulunan hatalar yazılım geliştiricilere tanımlanmış olan bir hata bildirim mekanizmasma göre bildiril-melidir.
- Bildirilen bu hatalar çözümlendikten sonra yeniden oluşturulan yazılım yeni bir sürüm olarak teste alınmalıdır.
- Yapılan değişikliklerin mevcut yazılıma etkilerinin görülmesi için de yineleme 'testlerinin yapılması ihmal edilmemelidir.
- Entegrasyon testleri gerçekleştirilirken "yazılım ttimleştirme test planı" temel alınmalıdır.

<center><image src="./image/yukaridanAsagi.png"></image></center>

## 4.3. Sistem Testleri

- Geliştirilen yazılımın performans, güvenirlilik, işlevsellik gibi özelliklerini değerlendiren testlerdir.
- Birim testlerde ve entegrasyon testlerinde geliştirilen yazılımın tasarırna uygun olarak geliştirildiği doğrulanır.
- Sistem testleri ise müşterinin sistem-den istediklerini doğrulamayı amaçlar.
- Bu nedenle sistem test durumlarında sistem gereksinimleri temel almarak, sistemin çalışacağı, gerçek ortamda karşılaşılabilecek olan senaryolar tanımlanır.
- Sistem testleri, kullanıcı kabul testlerinden bir önceki adım olarak yazılım ve dona-nım entegrasyonundan sonra "sistem test planma" göre gerçekleştirilir.
- Sistemin iş-levsel, işlevsel olmayan gereksinimlerinin doğrulanması hedeflenir [Wu-2001). Şe-kil-4. de sistem testi adımları görülmektedir.

<center><image src="./image/testAdimlari.png"></image></center>

- Sistem testlerinin ilk adımı olarak işlevsel gereksinimlerin doğrulanması gerçekleştirilir.
- Bu doğrulama sonucunda sistemin işlevsel olarak çalıştığı gözlemlenir.
- İşlevselliği yönünden doğrulanan sistem üzerinde, bir sonraki adımda, işlevsel olmayan gereksinimlerin karşılandığı göstermek amacıyla işlevsel olmayan testler gerçekleştirilir.
- Bu testlerden bazıları şunlardır:

- **Stres Testleri:** Sisteme girdi oranı sistem tasarım oranını aştığı zaman sistemin davranışını gözlemlemek üzere gerçekleştirilen testlerdir.
- **Performans Testleri:** Sistem çıktılarının belirlenen ve kabul edilebilecek olan zaman dilimi içerisinde üretebildiğinin değerlendirilmesinin yapılabilmesi için gerçekleştirilen testlerdir.
- **Konfigürasyon ve Uyumluluk Testleri:** Geliştirilen sistemin farklı platformlarda ve donammlarda nasıl davrandığını değerlendirilmesi icin gercekleştirilen testlerdir.
- **Güvenlik Testleri:** Sistemin izinsiz kullanım teşebbüslerindeki davranışlarının degerlendirilmesi icin gercekleştirilen testlerdir.
- **Kullanilabilirlik Testleri:** Kullanici - sistem etkileşimini ve ergonomisini degerlendirmek üzere gerceklestirilen testlerdir.
- **Geri alma Testleri:** Bir hata durumunda sistemin otomatik veya elle yeniden normal duruma donmesini degerlendirmek icin gerceklestirilen testlerdir.
- **Kullanici Arayüz Testleri:** Kullanıcının ve yazilimın grafik gösterimi olarak nasıl bir etkilesim icerisinde olacağını, kullanıcının klavye, ekran veya fare ile sisteme verecegi girdilerin sistem tarafindan nasıl islenecegini degerlendirmek icin gerceklestirilen testlerdir.

- Bu testier bazen işlevsel testier icerisinde gereksinim olarak belirtilmiş olabilir.
- Bu durumda bu testler işleysel testler ile birlikte gercekleştirilmiş olur.
- İşleysel olmayan testleri tamamlanan sistem artik dogrulannnş olarak kullanici kabul testlerine hazer demektir.
- Sistem testleri sirasinda ortaya cikan hatalar proje hata yonetim sürece göre raporlanir ye gerekli düzeltme işlemleri gercekleştirilir.
- Gerekli düzeltmelerden sonra, düzeltmelerden sistemin geri kalaninin etkilenmediginin degerlendirilmesi icin sistem azerinde yineleme testleri gercekleştirilir.

## 4.4. Kabul Testleri

- Proje kabul testleri müşteri gereksinimlerinin dogrulanmasi ile gercekleştirilir.
- Bunun icin her bir kullanıcı gereksinimini dogrulayacak olan test durumlari ye test senaryolari oluşturulur.
- Geliştirilen sistem, tanımlanan bu test durumlari ye test senaryolari müsterininde de katilimi ile "kabul test planina" uygun olarak koşturulur.
- Sistemin tamamının bu testlerden geçmesi ile sistem müşteri tarafindan kabul edilmiş olur. Kabul testi literattir-de, kullanici ile birlikte gerceklestirilen testler oldugu icin aynı zamanda kullanici kabul testi olarak da isimlendirilir [Rogers-2009].

**Kabul testlerinin gerçekleştirilmesi ile aaşağıdaki durumlar gerçekleşir:**

**_1. Müşteri gereksinimlerinin kapsandığı doğrulanarak, yazılımın bu gereksinimleri ne oranda_**
**_karşıladığı ölçülür._**

- Müşteri gereksinimleri bir proje icin en önemli kayittir.
- Eger proje sonucunda bu gereksinimlerin tam olarak karplandigi esterilemez ise projenin başarılı bir şekilde tamamlandigi söylenemez. Bu nedenle geliştirilen sistemin bu gereksinimleri tam olarak kapsadigi ye gereksinimlere uygun olarak dogrulanmalidir.
  **_2. Daha önceki test eylemlerinde tespit edilemeyen problemlerin tespiti yapilabilir._**
- Birim testier sadece ilgili oldukiari inodül hakkinda bilgi verir.
- Sistemin tamami hakkmda bir bilgi, hele de given hic vermez.
- Kabul testleri ile oncelikle gelisti-filen yazılımın müsterinin istedigi yazılım olduğu doğrulayan ve varsa daha önceki test aşamalarında tespit edilemeyen hataların bulunmasi da hedeflendir.
  **_3. Geliştirilen sistemin müşteri gereksinimlerini nasıl karşıladığı gösterilir._**
- Birim testleri ile kod kapsamaya bakilirken kabul testler ile müsteri gereksinimlerinin kapsandigi dogrulanır [Canna-2001j. Bunu yaparken her bir kullanici gereksinimleri karsilik en az bir test durumu yazilir.
- Gereksinimler icin yazilan test durumlari kosturulur.
- Kabul test plamnda tanimlanan kabul kriterlerine ulasilmca kabul testleri tamamlanmış olur.

- Kabul testleri elle yapilabilecegi gibi sistemin durumuna gore otomatik olarak da gerçekleştirilebilir.
- Kabul testleri sistemin başansim dogrudan gosterdiginden gercekleştirilmesine ayri bir onem verilmelidir.
- Kabul testlerinde karşrlaşilan en önemli soru kabul test durumu ye senaryolannm kimin tarafindan yazilacagidir.
- Kabul test-lerinin yazilmasi dogrudan müşteri tarafindan olabilecegi gibi, projenin test ekibi tarafindan da yazilabilir.
- Eger test durumlan ye senaryolari test ekibi tarafindan ya- zihmşlar ise testier başlamadan mutlaka müşteri onayi alnu-nandrr.
- Bazi projelerde ise ortak bir ekip kurularak birlikte [Miller&Collins-20011.
- Kabul test durumlan ve senaryolan müşteri gereksinimlerinden cikartrldiklanndan dolayi yazi-hm tamamryla gercekleştirilmeden yazilmiş olmalidirlar.
- Yazilan test durumlan ve senaryolari ile mi.işteri gereksinimleri arasinda izlenebilirlik lcurulmalidir.
- Bu izlene-bilirlik ile milşteri gereksinimlerinin tamami icin test eyleminin gercekleştirilecegi garanti altma ahnmiş olur.
- Ancak bu, türn gereksinimlerin başanyla gerceklendigi anlamma gelmez. Kabul testleri icin aşagidaki adimlar bir sürec olarak işletilir.

1. Müşteri gereksinimleri belirlenir ye belgelendirilir.
2. Kabul test plamm hazirlanir.
3. Müşterişteri gereksinimlerini dogrulayacak test durumu ye senaryolari hazirlamr.
4. Test Hazirhk Gozden gecinne toplantisinda hazirlanan test durumu ye senaryolari onaylatihr.
5. Kabul testleri icin gerekli test ortammi hazirlan.
6. Sistem testlerinin başanyla sonuclanmasmdan sonra kabul testlerini gerceklqtirilir.
7. Kabul test planmda belirtilen kabul kriterlerine ulapicaya kadar testlerin yapilmasma devam
   edilir.
8. Test sonuclanm belgelendirilir ye müşteriye onaylatilir.

Kabul testleri bir yazılım projesinin başansmda en kritik adımdır. İyi planlanim ye bel-gelendirilmiş
kabul testleri projenin başarısına büyük katki saglar. Müsteri memnuniyetini artirir.

## 4.5. Özet

- Birim, Tümleştirme, Sistem ve Kabul testleri yazillm projelerinde gercekleştirilen dolt farkli test seviyesidir.
- Birim testier, metot, fonksiyon veya prosedtir gibi bir kod parcasinin kendisinden beklenen işlevsellig'i dogru olarak yerine getirdigini ye hata icermedigini gostermek icin yazilim geliştiriciler tarafindan gercekleştirilen testier-dir.
- Birim testlerden sonra ttimleştirme testleri gercekleştirilir.
- Birim testlerde amac en lctictik kod parcalannm ayri ayri kendilerinden beklenen işlevleri yerine getirdigi-nin dogrulanmasi iken ttimleştirme testlerinin amaci bir araya gelerek entegre edil-miş olan bir yazilimm icerisindeki bileşenlerin birbirleriyle uyum icerisinde dogru bir şekilde caliştigmin ye kendilerine ait gereksinimleri yerine getirdiginin dogru-lanmasidir.
- Tümleştirme testleri aşagidan yukariya veya yukaridan aşagiya olmak tizere iki farkli yaklaşimla gercekleştirilebilir.
- Başanyla tamamlanmiş ttimleştirme testlerinden sonra geliştirilen yazilimin performans, güvenirlilik, işlevsellik gibi özelliklerini degerlendiren sistem testier gercekleştirilir.
- Geliştirilen yazilim üzerinde son olarak kabul testi gercekleştirilir. Kabul testleri ile mtişteri gereksinimlerinin dogrulanmasi gercekleştirilir.

## 4.6 Sorular

- Test aşamaları nelerdir? Açıklayınız.
- Birim test nedir? Birim tesler nasil gerçekleştirilir?
- Bildiginiz bir siralama algoritmasi icin birim testinin nasil yapilacagini gosteriniz.
- Ardişil arama algoritmasi icin birim testinin nasil yapilabilecegini ornek üzerinde gosteriniz.
- Ttimleştirme testi nedir? Hangi ttir stratejiler ile gercekleştirilir?
- Sistem testi nedir? Sistem testi adimlanm aciklaymiz.
- Kabul testi nedir? Kabul testleri hangi durumlar gercekleştirilir?
- Kabul testleri nasil bir süreç icerisinde gercekleştirilir?
