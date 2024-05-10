KGM NTCIP TESTER Kullanım Kılavuzu
1.	Cihaz Ekleme ve Bağlantı Kurma

İlgili Github linki üzerinden indirilen Setup dosyası kurulumu yapılır. Kurulum tamamlandıktan sonra uygulamanın kısayolu masaüstüne oluşacaktır.
Program çalıştırıldığında bizi sol tarafta işlem menüsü, sayfanın üst tarafında ise kavşağı seçebileceğimiz yani işlem yapmak istediğimiz kavşağın seçim penceresi bulunmaktadır.
Solda görünen menüden “KKC” sayfasına girildiğinde;
 
Bizi böyle bir sayfa karşılayacaktır. Sağ üst köşede ise “+” butonuna basarak test edilmesini istenilen kavşağın bilgilerini aşağıdaki ekrana girerek kayıt işlemi yapılmaktadır.

Yukarıdaki bilgilerde görüldüğü gibi cihazın ID, Adı, Markası, Versiyonu, IP Adresi ve Port numarası girilerek kayıt işlemi tamamlanır.
Eklediğimiz cihazla işlem yapmak için ise aşağıdaki resimde görüldüğü gibi listeden ilgili kavşak seçilmelidir.

Seçim yapıldıktan sonra yazılım NTCIP parametrelerinin olmaz ise olmazı olan “1.3.6.1.4.1.1206.4.2.1.8.1” OID numaralı Channel Parameter’in Maximum Channels parametresine GET isteği atmaktadır. Eğer işlem başarılı olmuş ise bağlantı sorunu olmayıp aşağıdaki resimde görüldüğü gibi seçim ekranının sol kısmında “Bağlandı” şeklinde bir değişim olacaktır. 

Eğer bağlantı kurulamadı ise yukarıdaki resimde görüldüğü gibi “Bağlı Değil” uyarısı vermektedir. Eğer uyarı alıyor iseniz cihazı daha detaylı kontrol etmek için menüden “Parametre Testi” sayfasına gidip bilgileri doldurarak detaylı test ve bilgiye ulaşabilirsiniz.

2.	Parametre Testi
Eğer bağlantınız başarısız veya cihaza tek parametre ile GET/SET gönderme veya ayrı bir IP/PORT girerek gönderip sonuçların Loglarını görmek istenilir ise Menüden “Parametre Testi” sayfasına gidilerek testler yapılabilir.
 
Yukarıdaki resimde görülen parametrelerin anlamları aşağıda listelenmiştir.

IP/Port Girerek Gönder : Eğer seçili cihaz değil de manuel olarak IP/Port girmek isterseniz bu sicimi yapmalısınız. Seçim yapıldıktan sonra IP Adres ve Port Girilebilir duruma gelecektir.
IP Adres : Tester Yazılımının kurulu olduğu bilgisayarın Cihaza ulaşabileceği IP adresidir.
Port : Cihazın SNMP Protokolünün Port adresidir. Varsayılan olarak 161 kullanılmaktadır.
Community : Cihazın haberleşme keywordu olarak tanımlanır. Cihazda nasıl tanımlandıysa o yazılmalıdır.
SNMP Versiyon : SNMP Versiyon numarasıdır. V1 Authentication kullanmadığı için Kullanıcı Adı ve Şifre girilmemektedir. V3 Seçilmesi durumunda Kullanıcı Adı ve Şifre girilmesi zorunludur. Cihazda tanımlanmış kullanıcı adı şifre ile doldurulmalıdır.
GET/SET : Hangi işlemi yapmak istediğinizi seçmelisiniz. GET ise seçim yapmanıza gerek yoktur. Bu durumda Parametre Tipi ve Değer girilmesine gerek yoktur. SET yapmak istenildiğinde seçim yapılır. Parametre ve Değer girilerek cihaza gönderim yapılır.
OID: istek atmak istediğiniz OID bilgisini girmelisiniz.
Parametre Tipi : Göndermek istediğiniz parametrenin tipidir. Octet String, Integer, Counter…
Değer :  SET Etmek istediğiniz parametrenin değerini girmelisiniz.

İlgili değerler girildikten sonra Test butonuna basarak testi yapabilir. Cihazın verdiği cevabı ise sağ taraftaki LOG ekranından görebilirsiniz.

3.	Tüm Parametreler Testi
   
Menü üzerinde bulunan “Tüm Parametreler” sayfasına gidilerek. Seçilmiş olan cihazı hangi parametreler ile teste girmesini istiyorsak seçim yaptıktan sonra Başlat butonuna basarak testi başlatabilirsiniz. Test bittikten sonra karşınıza aşağıdaki gibi bir ekran karşılayacaktır. Tabloda cihazın hangi parametrelere GET cevabı verdiği, hangi parametrelerin SET değerinin yapıldığı ve SET işlemi sonucunda parametrenin gerçekten değişip değişmediğinin sonuçlarını görebilirsiniz.
Test üç aşamadan oluşmaktadır. 
1.	GET : Cihaza ilgili parametreye GET isteği atılır ve gelen cevap tutulur.
2.	SET : ReadOnly değil ise Cihaza ilgili parametreyi rastgele bir değer SET edilir.
3.	Kontrol: Cihaza set işlemi yapıldıktan sonra değişim kontrol edilir.

Eğer GET işlemi başarılı olmuş, SET işlemi başarılı olmuş ise Kontrol işlemine geçilerek SET işlemi teyit edilir. Bu işlem de başarılı olmuş ise test başarılı olarak kabul edilir. 

Tüm testler tamamlandıktan sonra ise resimde görüldüğü gibi Rapor doküman klasörünü açan butona basılarak rapora erişilebilir. Dosya Yolu ise “C:/[Kullanıcı Klasörü]/Belgeler/NTCIP TESTER” klasöründen erişilebilir.

 
