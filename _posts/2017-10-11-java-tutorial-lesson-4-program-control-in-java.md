---
title: 'Java Tutorial - Lesson 4  : Program Control in Java'
summary: Javada Program Kontorlü
image: java.png
permalink: java-tutorial-lesson-4-program-control-in-java
date: '2017-10-09 16:53'
categories: k2
tags:
  - tags
  - continue
  - switch case
  - switch
  - break
  - return
  - do-while
  - while
  - for
  - if else
  - else
  - İf
  - Hello Friend
  - Java Object Oriented Programming
  - Java OOP
  - 'Java '
  - Linux
  - Open Source
  - Programming
  - Tutorials
author: Nuri Çilengir
---
## Javada Program Denetimi
Hayatta sorgulamadığımız bir düşünce, var olsa dahi bize ait olabilir mi ? Şimdi ne alaka hayat, sorgulama, programlama vs.  Hemen izah edeyim bir program yazmak için programlama dillerini kullanırız. Programlama dilleri bizim anlayabileceğimiz insan diline daha yakın sadece içerisinde kurallar barındıran bir araç. Peki bilgisayarlar bizi ne şekilde anlıyorlar  ? Biz ekrana "HELLO WORLD !!" yazdırmak istediğimizde aslında bilgisayarın daha da genel manada makinelerin anlayabileceği dil bu mudur ? Bu konuya  [ilk dersimizde](http://nuricilengir.me/java-tutorial-lesson-1-what-is-java-write-once-run-anywhere) değinmiştik şimdi yeniden bir değerlendirelim. Biz yazdığımız programı çalıştırmak istediğimizde javada bu program ortak bir ara dile çevirilir (Javanın bir kere yaz heryerde çalıştır felsefesi.) Bu ortak dil yazdığımız programlama dilinden uzak makinanın anlayabileceği dile yakındır. Bilgisayarlar peki bu ortak dili nasıl sorgularlar ? Gelmek istediğim nokta bir bilgisayar ya da makinenin aslında programlama denetimi yaparkenki  mantıkla neredeyse eşdeğer bir şekilde çalıştığıdır. Basit olarak açıklarsak cihazdaki devreden geçen voltaj değerlerinin 0 volt = sıfır, 5 volt = bir değerine karşılık geldiği , sıfır ve bir değerlerinin de true ya da false değerlerini yani doğru ya da yanlış değerlerini döndürdüğüdür. O zaman programlamanın sorgu yani bir mantık barındırdığını söyleyebiliriz ve bu yüzden programlama öğrenmek için önemli olan yol aslında neyi nasıl yapacağınız değil neyi ne şekilde yapacağınızdır.
Uzattıysam kusuruma bakmayın elimden geldiğince size aslında programlamanın zor bir olay olmadığını ve sadece kod yazmayı öğrenmek ile gerçekleşmeyeceğini açıkmaya çalışıyorum. Yoksa if else while gibi konuları anlatan bir çok kaynak bulunmakta. Şimdi gelelim konularımıza...


### Koşul İfadeleri
![Koşul İfadeleri]({{ site.assetsDir }}{{ page.permalink }}/javatutorial-kosullar.jpg)
Adında anlaşılabileceği gibi durumları sorgulamak için kullandığımız ifadelerdir. Örneğin **not** adlı değişkenin **60tan** **küçük** ya da **büyük** veya **eşit** olduklarını ve bu durumlarda program akışında neler olmasını belirttiğimiz deyimlerdir. Program yazarken belkide en çok kullanacağımız yapılardandır. Peki nedir bunlar ? 
1.    **IF**
1. 1.  IF- ELSE
1. 2.  IF - ELSE IF -ELSE
2.    **Switch-Case**
  
#### if, if-else, if - else if - else
if bolğu tıpkı türkçe meali gibi kullanılır eğer olursa eğer koşul sağlanıyorsa ya da sağlanmıyorsa şunu yap. Else ise if bloğunda belirttiğimiz koşulların sağlanmadığı durumlarda eğer belirtmişsek çalışacak blocktur ve kullanımı şu şekildedir.

```java
           if (KOŞULUMUZ) {
            //koşul sağlandığında(true) çalışmasını istediğimiz kod bloğu
           }else{
            // koşul sağlanmadığında (false) çalışmasını istediğimiz kod bloğu
           }

```
Çalışma yapısını daha iyi anlamak için bir örnek yapalım. Örneğimiz şu şekilde olsun bir okulda okuyan öğrencilerin not ortalamaları 45 ten düşük ise onların kaldığını ekrana yazdıralım..

```java
    public class NotOrtalamasiDemo{
        public class void main(String[] args){
            int ortNot = 68;
            
            if(ortNot >= 45){
            System.out.println("Öğrenci Durumu : Başarılı");    
            }else{
            System.out.println("Öğrenci Durumu : Başarısız");    
            }
        }
    }
```
> ÇIKTI : Öğrenci Durumu : Başarılı

Kodumuzu açıklayalım..Yaptığımız işlem çok basit integer veri tipinde ortNot adlı değişkene 68 değerini atadık bunu x öğrencisinin not ortalaması kabul edelim.Daha sonra bu ortNot adlı değişkeni operatörler yardımıyla if yapısı içerisinde sorguladık. Dedik ki Eğer ortalama not 45'e eşit veya yüksekse öğrenci başarılı'yı ekrana yazdır. Eğer değilse ekrana öğrenci başarısız yadır. Şimdi bu örneği biraz daha ilerletelim bu seferde **else if** bloğunu işin içine sokalım **else if** if bloğu altında eğer koşulumuz sağlanmazsa başka bir koşul belirlememize yarar. Else'den farkı **else if** blokları içinde bir koşul daha belirtebiliriz fakat else için böyle bir durum söz konusu değil. Else eğer belirlediğimiz koşul veya koşulların sağlanmayacağı durumda gerçekleşmesini istediğimiz bloğu çalıştırır.  
Örneğimizi şu şekilde tanımlayalım yine 45 düşük not ortalamasına sahip öğrencilerin durmunu başarsız olarak ekrana yazdıralım. Buna ek olarak Öğrencinin not ortalamasın hangi harf notuna karşılık geldiğini sorgulayalım.
```java
    public class HarfNotuDemo{
        public class void main(String[] args){
            
            Scanner scn = new Scanner(System.in);
            
            System.out.print("Öğrenci Notunu Giriniz:");
		    int ortNot = scn.nextInt();
		    char sonuc;
		    
            if(ortNot >= 0 && ortNot < 50){
                sonuc = "F"
            }else if (ortNot>=50 && ortNot<60){
                sonuc = "D";   
            }else if (ortNot>=60 && ortNot<70){
                sonuc = "E";
            }else if (ortNot>=70 && ortNot<80){
                sonuc = "C";
            }else if (ortNot>=80 && ortNot<90){
                sonuc = "B"
            }else if (ortNot>=90 && ortNot<100){
                sonuc = "A";
            }else{
            System.out.println("Lütfen 0-100 aralığında geçerli bir değer giriniz !!");
                sonuc = "-";
            }
            System.out.println("Öğrenci Notu : " + sonuc);
        }
    }
    
```
Hadi gelin ne yaptığımızı görelim.
İlk önce ekrana Öğrenci Notunu Giriniz : yazdırdık ve daha sonra kullanıcan bir değer girmesini bekledik gelen değeride kullanıcan integer tipinde veri beklediğimizi javada tanımlayarak(`nextInt()`) kullanıcıdan aldığımız değeri integer tipindeki ortNot adlı değişkene atadık. Daha sonra char veri tipinde sonuç adında bir değişken tanımladık.Bu değişkenin amacı ekrana harf notunu bastıracağımız için bize tek harflik alanın yetecek olması. Daha sonra girilen değeri **koşul bloklarında sorguladık** eğer not 45ten küçükse sonuc değişkenine F notunu atadık. eğer 45'e eşit büyükse ve 60tan küçükse sonuc değişkenine D notunu atadık. Aynı işlemeri E,C,B,A değerleri için yaptık. Ve en sona bir else bloğu açtık eğer belirlediğimiz koşullar sağlanmazsa bu blok çalışacaktı. Biz bu blokta yazdığımız programı garanti altına almış ve bir hatanın önüne geçmiş olduk. Nasıl mı ? Kullanıcının 125 değerini girdiğini düşünelim 125 değeri bizim belirttiğimiz herhangi bir koşulu sağlamıyor olacaktı dolayısıyla yazdığımız kodta bir hata meydana gelecekti çünkü sonuc değişkeni boşken ekrana yazdırmaya çalışıyor olacaktık.**Else** bloğunda girdiği aralıkta bir hata olduğunu kullancıya bildirdik ve sonuc değişkenine - değerini atadık.Son olarak koşul bloklarının dışında ekrana Öğrenci notu : şeklinde bir yazı yadırdık ve koşul bloklarında sağlanan değeri öğrenci notu şeklinde ekrana yazdırdık.

**NOT:** if-elseif,else bloklarında koşul sağlanması durumunda diğer bloklarda belirlediğimiz koşullar sorgulanmaz koşul sağlandığı blokta tanımlanan işlemler yapılır ve program akışına devam eder.

#### Switch-Case

Switch-case yapısı if elseif else yapısına benzerdir. Çalışması tamsayıların karşılaştırılmasıyla doğru koşulun bellirlenmesiyle gerçekleşir. Yazım Şekli aşağıdaki gibidir.

```java
	    switch(sayi){
      case değer1(Koşul) : Çalışması istenen kod bloğu; break;
      case değer2(Koşul) : Çalışması istenen kod bloğu; break;
      case değer3(Koşul) : Çalışması istenen kod bloğu; break;
      case değer4(Koşul) : Çalışması istenen kod bloğu; break;  
        .
        .
        .
      default (else'e benzetebiliriz) : Çalışması istenilen kod bloğu;
    }
```
Şimdi çalışmasını örnek bir proje üzerinde görelim ve hakkında daha net yorumlar yapalım. Programımız kullanıcıdan 1 ile 12 arasında bir değer alalım ve bu değerin hangi aya karşılık geleceğini ekrana yazdıralım.
```java
public class SwitchCase{
   public static void main( String args[] ){
     printf("Lütfen 1-12 arasında bir değer giriniz.");
     Scanner scn = new Scanner(System.in);
     int gelensayi = scn.nextInt();

     switch(gelensayi){
       case 1: System.out.println("OCAK");
       case 2: System.out.println("ŞUBAT"); break;
       case 3: System.out.println("MART"); break;
       case 4: System.out.println("NİSAN"); break;
       case 5: System.out.println("MAYIS"); break;
       case 6: System.out.println("HAZİRAN"); break;
       case 7: System.out.println("TEMMUZ"); break;
       case 8: System.out.println("AĞUSTOS"); break;
       case 9: System.out.println("EYLÜL"); break;
       case 10: System.out.println("EKİM"); break;
       case 11: System.out.println("KASIM"); break;
       case 12: System.out.println("ARALIK"); break;
       default:
          System.out.println("Lütfen geçerli bir değer giriniz... !");
     }
   }
 }
```
 Bu programı if else yapısıyla yazdığımızı düşünelim nasıl bir kod yapısı oluşutururduk ? 
 gelen sayıyı if ve else if blokların kaça eşit olduğunu sorgulardık daha sonra koşul sağlanırsa  girilen değerin denk geldiği bir koşulumuz varsa o koşula uygun kodu çalıştırıdık yani bu uygulama için ekrana karşılık geldiği değeri yazdırırdık. Eğer koşullar sağlanmasaydı ve biz sağlanmadığı durumda yine bir şey yaptırmak istediğimizde else bloğunu kullanarak isteiğimiz işlemi gerçekleştirirdik. Burada bunlardan çok daha farklı bir şey yapmadık. case blokları içinde koşulumuzu belirledik ve eğer koşul sağlanırsa istediğimizi yaptırdık ve daha sonra break anahtar kelimesiyle koşulun sağlandığını ve artık diğer koşulları gezmenin gerek olmadığını belirttik.
Switch case deyimini if deyiminden ayıran en belirgin özellik break anahtar kelimesidir. Break'in kod içinde nasıl çalıştığını bu yazıda değerlendireceğiz fakat ilk önce switch yapısı içindeki görevinden söz edelim.
Eğer biz swicth-case yapısı içinde break anahtar kelimesini kullanmasaydık program yazdığımız her koşulu dolaşacaktı (1 den başlayıp 12. koşula kadar bir sorgu gerçekleşecekti.) kullanıcıdan 5 değerini aldığımızı varsaylım 5. ay Mayıs diğerlerini sorgulamamıza gerek var mı ? Yok fakat bazen program yazarken sorgulanmasını istediğiniz durumlar olacak break yapısı bu yüzden switch-case yapısı içindeki en önemli elemanlarımızdan biri.

Gelin şimdi yeni bir program yazalım bu sefer bir kategorileme programı olsun kullanıcan char ve integer tipinde iki değer alalım ve buna karşılık gelen bir üniversitenin ders kataloğunu  ekrana yazdıralım. Örenğin kullanıcı 1 ve C değerini girsin ve 1. yıl C (Computer Engineering) derslerini ekrana yazdıralım.

```java
  class iciceSwitchCase
{
    public static void main(String arg[])
    {
        Scanner scn = new Scanner(System.in);
        System.out.println(" X Üniversitesi Ders Kataloğu Sayfasına Hoş Geldiniz..");
        System.out.println("Görmek istediğiniz yıl'ı giriniz : ");
        int yıl = scn.nextInt();
        System.out.println("Görmek istediğiniz %d . yıl Bölümünün Kodunu Giriniz :");
        char bolum = scn.next();


        switch( yıl ){
            case 1: // 1. yıl
                System.out.println("İngilizce, Matematik, Fizik");
                break;
            case 2: // 2.yıl
                switch( bolum ){
                    case 'C':
                        System.out.println("Veri Yapıları, Java OOP, Bilgisayar Organizasyonu");
                        break;
                    case 'E':
                        System.out.println("Mikro İşlemciler, Mantıksal anahtarlama teorisiy");
                        break;
                    case 'M':
                        System.out.println("Teknik Çizim, Üretim Makineleri");
                        break;
                }
                break;
            case 3:
                switch( bolum ){  // 3. yıl
                    case 'C':
                        System.out.println("İşletim Sistemleri, Veri Tabanı Yönetimi");
                        break;
                    case 'E':
                        System.out.println("Mantık Tasarımının Esasları, Mikroelektronik");
                        break;
                    case 'M':
                        System.out.println("İçten Yanmalı Motorlar, Mekanik Titreşim");
                        break;
                }
                break;
                case 4:   // 4. yıl
                    System.out.println("Teknik Seçmeli,Teknik Seçmeli, Bitirme Tezi");
                    break;
        }
    }
}

```

Açıklayalım.
Her zaman yapıtıklarımızı yaptık en başta Scanner sınıfından bir scn adlı nesne oluşturduk. Ardından kullanıcan bir tam sayı birde string veri tipinde değer girmesini istedik.  `scn.next();` 'i ilk defa görüyoruz next() deyimi javada Kullanıcıdan String tipinde giriş yapılacağını belirtir. Daha sonra girilen değerleri swtich yapısı içinde koşullarımıza göre sorguladık. Kullanıcı 1 değerini girdiğinde 1 . sınfın derslerinin ortak olacağını görecek ve ekrana `İngilizce, Matematik, Fizik` yazacak . Kullanıcı 2. sınıf C kodunu yani Computer Engineering listediğimizde program ilk switch yapımız olan yılı sorgulayacak ve 2. yılın olduğu bloğa yönelecek. Bu blok içerisinde ayrı bir switch deyimi tanımladık. Burada char tipinde tuttuğumuz değeri sorguluyoruz yani 2. yılın C kodlu dersi olan değerler ekrana yazdıralacak `Veri Yapıları, Java OOP, Bilgisayar Organizasyonu` . switch-case yapısının iyice anlaşıldığını düşüyorum.



### Döngü İfadeleri

Döngü işlemleri istediğimiz işlemlerin belirlediğimiz koşul sağlanana kadar yapılmasını sağlarlar. Örneğin kullanıcı programdan X tuşuna basasıya kadar çıkmamasını ve istediği işlemleri gerçekleşmesini sağlamak isteyebiliriz ya da matematik işlemi içeren bir programımız olsun istediğimiz sonuca ulaşıncaya kadar bir takım işlemler yapmaya devam etmek gibi işlemler gerçekleştire bileceğimiz yapılardır. 


#### While, Do-While 
![]({{ site.assetsDir }}{{ page.permalink }}/while.png)
while yapısı istediğimiz kod bloğunu döngü koşulu doğru olduğu sürece sürdürür. Döngü false değerini döndürdüğünde ise tekrar edilen işlemden (kod bloğundan ) çıkılır ve program akışına devam eder.

```java
  while(koşul){
    //çalışmasını istediğimiz kod bloğu
	}
```
While deyimini daha net anlamak için bir uygulama yapalım. Kullanıcıdan 1 sayı alalım ve 1den kullanıcının girdiği değere kadar olan tüm sayiların toplamını ekrana yazdıralım.

```java
public class whileDemo{
    public static void main(String args[]){
        Scanner scn = new Scanner(System.in);
        System.out.println("Lütfen bir değer giriniz : ");
        int sayi = scn.nextInt();
        int sonuc 
        sonuc=0;
        int sayac;
        sayac = 0;
             while(sayac <= sayi){
              sonuc = sonuc + sayac; 
              sayac ++;
            }
        System.out.println("Sayılar toplamı : " + sonuc );
    }
}

```
Kullanıcıdan değer alma işlemini geçerek sayac adında değişkene geliyorum bunu döngümüzün koşulunu sınamak için tanımladık.  **sayac**  değerini girlen değerden büyük olup olmadığını sorguladık ve while döngüsü içinde arttırmak için kullandık. Girilen değerin 10 olduğunu var sayalım sayaç değerine 0 değerine atadık çünkü saydırma işlemine 0 dan başlamak istiyoruz daha sonra sayac değerinin küçük olması halinde while döngüsü içine girmesini istedik çünkü belirlediğimiz koşul true  daha sonra koşul değişkenine` sonuc + sayac` ile girilen değere kadar toplama işlemi gerçekleştirdik. ve sayac değerini 1 arttırdık. 10 a kadar toplama işlemiwhile içinde şu şeklide gerçekleşecektir.   0 + 0 ı sonu değişkenine atadık çünkü sonuç ve sayac değişkenlerinin ilk değeri 0dır daha sonra sayac değişkenini bir arttırdık ve döngü koşulun devam edip etmediğini kontrol etti. koşulumuz hala true değerini döndürdüğünü gördü ve döngü devam etti 0 + 1 sonuc 1, 1 +2, sonuc 3, 3 +3, sonuc 6 şekline sayaç değişkeni 11 olasıya kadar bu işlemi devam ettirdik. sayac 11 olduğunda while koşulu tekrar kontrol edilir ve artık koşul false değerini döndürdüğü görülür ve program akışına devam ederek sonuc değişekenin son değeri ekrana yazdırılır.


Bu sefer başka bir while uygulaması yapalım. kullanıcan 2 değer alalım ve bu iki değeri listeleyelim mesela kullanıcı 1 ve 8 değerlerini girsin çıktımız şu şekilde olsun
```
1.8
1.7
1.6
1.5
2.8
2.7
2.6
```

Programızın kodu ;

```java
public class whileDemoo{
    public static void main(String args[]){
      Scanner scn = new Scanner(System.in);
      System.out.println("Lütfen 2 adet sayı giriniz.. İlk sayı 3 ten küçük İkinci sayı 5ten büyük olmalı...");
      int sayiBir = scn.nextInt();
      int sayiIki = scn.nextInt();
        while(sayiBir < 3){
            while(sayiIki > 5){
                System.out.println(sayiBir + "." + sayiIki);
                sayiIki--;
            }
            sayiBir++;
        }
    }
}
```
Kodumuzu inceleyelim..
kullanıcıdan 3  küçük ve 5ten büyük 2  değer aldık daha sonra sayiBir'in 3ten kçük olup olmadığın sorguladık. ve while içinde ikinci bir while döngüsü oluşturduk. burada girilen ikinci sayımızın 5ten büyük olup olmadığını sorguladık ve eğer büyükse 2. whilemızın içine girdik sayı biri ve sayı ikiyi yazdırdık ve 2. whilenin içinde ikinci sayiIki değişkenini bir azalttık sayiIki 6 olduğunda içteki whilemızın koşulu sağlanmış olacak ve bir üsteki döngüye çıkcağız orada ise sayiBir değişkenini 1 arttıracağız ve tekrar koşul sağlanasıya kadar işlemleri tekrarlayacağız. İç içe kullandığımız döngü koşul gibi deyimlere **Nested** adını veririz bunu da ufak bir not olarak buraya düşelim.

#### Do-While Döngüsü
While dongüsünden farkı while bloğu içinde yazdığımız koşul true değerini döndürmese bile döngümüz en azından bir kere dönecektir.
```
   do{
   // çalışması istenen kod bloğu
 }while(koşul)
```


Hemen bir örnek üzerinde görelim..

```java
public class whileDoDemoo{
    public static void main(String args[]){
      Scanner scn = new Scanner(System.in);
      int x,y;
      do{
        System.out.println("Bölünecek sayıyı giriniz");
        x = scn.nextInt();
        System.out.println("Bölüm değerini giriniz");
        y = scn.nextInt();
        System.out.println(x + "Sayısının"+ y+ "sayısına bölümü :" + x/y + " ve kalan : "+ x%y);
      }while(x != 0)
      System.out.println("0 değeri girildi programdan çıkılıyor.");
    }
}
```
Programımızı açıklamak gerekirse şunlar söylenir, x ve y adlı iki adet integer tipinde sayı değişken oluşturduk. daha sonra kullanıcan değerlerimizi aldık ve println içerisinde işlemlerimizi yaptırdık ve eğer kullanıcı 0 değerini girmezse döngü tekrar dönecek ve tekrar kullanıcıdan 2 adet değer alınacak.

#### For Döngüsü

for döngüsünde while döngüsünden ayıran kısım sayacı kendi yapısı içinde yapsı ve değikeni kendi içinde tanımlamamızdır.

```java
for(Değişken;  Koşul; Değişkenin Kontürolü; ){
 //çalışması istenen kod bloğu
}
```

 for döngüsünde  1 den 10 a kadar olan sayıları ekrana yazdıralım ve for'un kullanımını görelim.



```java
public class ForDemo{
    public static void main(String args[]){
      for (x = 0 ; x=<10 ; x++ ) {
        System.out.println("x = " + x);
      }
      System.out.println("Sayma işlemi bitti ! ");
    }
}
```

Açıklayalım;
for parantezleri içinde x adında bir değişken oluşturduk 0 değerini atadık daha sonra koşulumuzu belirttik `x=<10` ve daha sonra x değişkenini arttırma işlemi yaptık. En son olarak döngü içinde 1 ile 10 arasındaki her değeri ekrana yazdırdık.

Fark ettiysek yapacağımız bir kaç satırlık işi for döngüsü içinde  tek bir satır içinde yapmış olduk.

Şimdi whilede yaptığımız nested uygulamasını burada da yapalım kullanıcıdan değer almak ile uğraşmayarak iç içe for kullanarak şu şekide bir çıktı elde edelim
```
1.8
1.7
1.6
1.5
2.8
2.7
2.6
```

```java
public class ForDemo{
    public static void main(String args[]){

      for(int disSayi = 1; disSayi <= 2;  disSayi++){
          for(int icSayi = 8; icSayi <= 6; icSayi--){
              System.out.println(dısSayi + "." + icSayi);
          }
        }    
    }
}
```

Dıştaki sayıyının başlangıç değeri olarak 1 atadık koşulumuzu belirttik sonra içteki sayıyı başlangiç değeri olarak 8 belirledik koşulumuzu belirttik ve sonra değerimizi azatacağımızı belirttik.Program çalışmaya başladığında disSayi başlangiç değerimiz 1 olarak belirlenir sonra ikinci icSayi değerimiz 8 olarak belirlenir sonra 2 for bloğumuzun içinde değişkenlerimiz ekrana yazdırılır ilk değerlerimiz 1 ve 8 olduğu için ekrana 1.8 yazdırılır daha sonra 2. for döngüsünde koşulumuz hala sağlanmadığı için 1.7,  1.6 olarak devam edilir ve daha sonra koşul sağlandığında 1.for döngüsüne dönüldü ve burada da hala koşulumuz hala false değerini döndürmediği için  1. for döngüsünde disSayi değişkenini 1 arttırdı ve 2. for döngüsünde yine aynı işlemler tekrarlandı.


şimdi for ile çarpım tablosunu ekrana yazdıralım

```
public void carpımTablosu(){
	for(int i=0;i<11;i++){
		for(int j=0;j<11;j++){
			System.out.printf("%d*%d=%d\t\t",i,j,i*j);
			}
		System.out.print("\n");
	}
```

Yukarıda anlattığımız şey burada da geçerlidir. Ve çıktımız şu şekilde olur...
```
1*1=1
1*2=2
1*3=3
1*4=4
1*5=5
1*6=6
1*7=7
1*8=8
1*9=9
1*10=10

2*1=2
2*2=4
2*3=6
....
..
. 
Şeklinde devam eder..
```

Yine for ile ilgili son 1 örnek yapalım ve artık olayı bitirelim..


```
public void Dosya_adı(){
	
	for(int i=50;i<=250;i+=50){
		for(int j=5;j<=9;j+=2){
			for(int k=5;k<=20;k+=5){
				for(int l=0;l<=9;l++){
					System.out.printf("Dosya_Adı %d_%d_%d_%d.txt\n",i,j,k,l);
				}
			}
		}
	}
	
}
```
Burada yaptığımız işlem örneğin DosyaAdı_100_7_5_8.txt adında bir dosya oluşturmak istiyoruz.Bu dosya ismini oluşturma konusunda for kulandık sınırlarımızı belirledik ve daha sonra dosya ismini ekrana yazdırdık.
Kodun açıklaması 50 ile 250 arasında 50şer 50şer artan  _ 5 ile 9 arasında 2şer artan _ 5 ile 20 arasında 5er artan _ 0 ile 9 arasında 1er artan for yapıları oluşturduk ve çıktmız şu şekilde oldu..


```
DosyaAdı_50_5_5_0.txt
DosyaAdı_50_5_5_1.txt
DosyaAdı_50_5_5_2.txt
DosyaAdı_50_5_5_3.txt
DosyaAdı_50_5_5_4.txt
DosyaAdı_50_5_5_5.txt
DosyaAdı_50_5_5_6.txt
DosyaAdı_50_5_5_7.txt
DosyaAdı_50_5_5_8.txt
DosyaAdı_50_5_5_9.txt
DosyaAdı_50_5_10_0.txt
DosyaAdı_50_5_10_1.txt
DosyaAdı_50_5_10_2.txt
DosyaAdı_50_5_10_3.txt
...
..
.
DosyaAdı_50_5_15_0.txt
DosyaAdı_50_5_15_1.txt
DosyaAdı_50_5_15_2.txt
...
..
.
Şeklinde devam eder.

```
Şunu görmenizi istiyorum en sonda oluşturdğumuz for yapısı ilk olarak çalışacak olandır yani o for döngüsünün koşulu sağlanmadıkça bir dıştaki for döngüsüne girilmedi bir sonraki for'a çıkıldığında da orada olan değiiklere göre yine en içteki for döngüsüne girdik...


### Dallandırma Deyimleri
1. break
2. continue
3. return

#### break Deyimi

break deyiminin 2 farklı kullanımı mevcuttur. Etiketli ve etiketsiz olmak üzere ikiye ayrılır. etiketsiz olanı switch deyiminde görmüştük. Orada kullandığımız break anahtar kelimesi switch yapısını koşul sağlanması durumunda sonlandırmamıza yarıyordu. Bu şekilde olan kullanım while for gibi döngüler içinde de kullanılabilir.

Örnel bir uygulama yapalım ve uygulamamızda for içinde  bir durumda döngü içinden çıkalım.


```
		int x;
		for ( x = 0 ; x<100 ; x++ ) {
			if (x==9) {
				break;
			}
			System.out.println("x = " + x);
		}
	System.out.println("x 8 değerine ulaştı ve döngüden çıkıldı.");
```


Burada for ile 0dan 99 kadar olan sayıları ekrana yazdırmak istedik ama for içerisinde if deyimiyle eğer x 9'a eşitse döngüden çıkılması gerektiğini belirttik. çıktımız şu şekilde oldu.

```
x = 0
x = 1
x = 2
x = 3
x = 4
x = 5
x = 6
x = 7
x = 8
x = 8
x 8 değerine ulaştı ve döngüden çıkıldı.
```
 
Etiketsiz break anahtar kelimesi for while gibi en içteki döngüleri sona erdirirken etiketli break ifadesi hangi döngünün başına koyulduysa o döngüsü sonlandırır.


```java

		cık:
		for ( int x=0; x<10 ; x++ ) {
			for (int y = 0;y< 100 ; y++ ) {
				if (x==9) {
					break cık;
				}
				System.out.println("y = " + y);
			}
		System.out.println("Döngüden çıkıldı.");
		System.out.println("x = " + x);
		}
```

cık adında bir etiket oluşturduk ve daha sonra içteki for'dan dıştaki for'a değil de for'un üstüne çıktık. Çıktımız şu şekilde olacak

```
x = 0
x = 1
x = 2
x = 3
x = 4
x = 5
x = 6
x = 7
x = 8
x = 9
Dögüden çıkıldı.
```
#### Continue Deyimi

Continue anahtar kelimesi, Döngü içinde o andaki döngü işlemini geçip bir sonraki işlemin yapılmasını sağlar ve break gibi etiketli ve etiketsiz kullanımı mevcuttur.

```java

		for ( int x=0; x<10 ; x++ ) {
            if(x == 3){
                continue;
            }
		System.out.println("x = " + x);
		}
	  System.out.println("Döngüden Çıkıldı.");
```

Hemen çıktı üzerinde olayı görelim.

```
x = 0
x = 1
x = 2
x = 4
x = 5
x = 6
x = 7
x = 8
x = 9
Dögüden çıkıldı.
```
Görüldüğü üzer for döngüsü içerisinde x'in 3'e eşit olmaı halinde continue deyimini kullandık ve çıktımızda 3 yazdırılmadı. Break'tan farkı döngüleri tamamiyle terk etmiyor oluşumuz sadece 1 kereliğini es geçiyoruz..

```java
        es :
		for ( int x=0; x<7 ; x++ ) {
           for (int y=0; y<10 ; y++)[]
            if(x == 3){
                continue es;
            }
        System.out.println("y = " + y);
          }		
		System.out.println("x = " + x);
		}
	  System.out.println("Döngüden Çıkıldı.");
```
Bu programda es adında etiket oluşturduk daha sonra bu etiki continue kullanarak döngüden çıkarttık fakat döngümüz  bu sefer kaldığı yerden devam edecektir.. Ve s çıktımız şu şekilde oldu
```
x = 0
x = 1
x = 2
x = 0
x = 1
x = 2
x = 0
x = 1
x = 2
x = 0
x = 1
x = 2
x = 0
x = 1
x = 2
x = 0
x = 1
x = 2
x = 0
x = 1
x = 2
Dögüden çıkıldı.
```
Çıktıda döngünün 0dan başlayıp 2 de sonlandığını görüyoruz bu işlem toplam 7 kere gerçekleşmiş yani dıştaki koşulumuz sağlanana kadar bu işlem devam etmiş çünkü dıştaki x değişkeninin koşulu hala sağlanmış değildi ve koşul sağlanana kadar her defasında döngüye giriliyordu.

#### return Deyimi 
return'un iki görevi vardır.İlk görevi eğer döndürmek istediğimiz bir değer varsa (Bu işlemi daha çok oluşturduğumuz metodlar içersinde gerçekleştiririz.) onu döndürmek.Diğeri ise eğer metodumuz void ise break gibi davranıp metottan çıkar.

```java
public class returnDemo{
    public int CarpmaIslemi(int x, int y){
        int sonuc = a*b;
        return sonuc; //return'un oluşturduğumuz metot içindeki kullanımı 
    }
    
    public void birseyYapma (int x){
        if(a==0){
            return; // void tanımlı metod olduğu için 0'a eşit olması halinde metotu terk edecek..
        }else{
            System.out.println("->" + a);
        }
    }
}
```
Bir sonraki dersimizde  metotlar, Constructorla, Statik alanlar Statik metodlar gibi konuları göreceğiz. Görüşmek üzere...
Nuri Çilengir