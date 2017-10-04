---
title: 'Java Tutorial - Lesson 3  : Assingments and Oparators'
summary: Javada Atama ve Operatörler
image: java.png
permalink: java-tutorial-lesson-3-assingments-and-oparators
date: '2017-10-02 20:49'
categories: k2
tags:
  - Assignments
  - Data Types
  - Hello Friend
  - Hello World
  - Java Object Oriented Programming
  - Java OOP
  - 'Java '
  - Linux
  - Open Source
  - Operators and Assignments
  - 'Operators '
  - Programming
author: Nuri Çilengir
---
## Atamalar Ve Operatörler
Geçtiğimiz derste Sınıf Nesne ve Veri Tipleri hakkında bilgi edinmiştik. Bu derste Nesne ve Veri Tipi gibi kavramları nasıl yönlendireceğimizi göreceğiz.
### Atamalar
Java programlama dilinde atama işlemleri değişkenin sağ tarafından sol tarafına doğru gerçekleşir. Veri Tipini belirlediğimiz bir değişkene atama işlemi yapmak için SAĞ taraftaki değerin SOL taraftaki değişkene aktarılmasıyla gerçekleşir. Örnek vermek gerekirse;

```java
int Degisken;
Degisken = 35; // Doğru Atama Şekli
35 = Degisken; // Yanlış Atama Şekli
```
Atama işleri veri tipleri için son derece basittir. Veri tipleri değeri doğrudan içinde tutar dolayısyla değişen sadece içerikleri olur.
```
int degiskenBir, degiskenIki;
degiskenBir = 35;
degiskenIki = 45;
degiskenBir = degiskenIki;
```
Burada ki olayı sırasıyla açıklamak gerekirse;
İlk önce degiskenBir ve degiskenIki adında iki adet integer veri tipinde değişken tanımladık.Daha sonra bu değikenlere 35 ve 45 değerlerini atadık. Peki 
`degiskenBir = degiskenIki; ` ? burada ise değeri 45 olan değişkeni değeri 35 olan değişkene atadık yani artık degiskenBir'in yeni değeri 45 olmuş oldu.
### Nesneler Ve Atamalar
[Geçtiğimiz derste ](http://nuricilengir.me/java-tutorial-lesson-2-everything-is-object) gördüğümüz Nesne kavramı için atama işlemi veri tiplerine uyguladığımız işlemden biraz daha meşakkatli denilebilir.Nesneleri yönetmek için referansları kullanırız. Eğer nesneler için atama işlemi gerçekleştirecek olursa nesnelerin değil nesnelere bağlı olan referansların gösterdiği değerlerde değişiklik olacağıdır.
```java
class Sayi{
  int x;
}
public class NesneAtamaları{
  public static void main (String[] args){
    Sayi n1 = new Sayi();
    Sayi n2 = new Sayi();
    n1.x = 23;
    n2.x = 15;
    System.out.println("1  : n1.x  = "+n1.x+" |  n2.x = "+ n2.x);
    n1 = n2;
    System.out.println("2 : n1.x = "+n1.x+" |  n2.x = "+ n2.x);
    n1.x = 35;
    System.out.println("3 : n1.x = "+n1.x+" |  n2.x = "+ n2.x);
  }
}
```
Bu uygulamada ne yaptık  ? 
Önce 2 tane Sayi adında nesneler oluşturduk. Bu nesneler Sayi türündeki bağlıdırlar(n1 ve n2 ).  Bu referanslar 2 ayrı Sayi nesnesini belirtirler. Daha sonra n1 referansının belirttiği Sayi nesnesine 23 değeri atandı. Aynı işlemi n2'ye uyguladık. Ve sonra` System.out.println`'le bunları görmek için ekrana yazdırdık.
Çıktımız ise şu şekilde oldu :

>1 :  n1 .x  =  23 |  n2.x = n2.x = 15
>2 :  n1 .x  =  15 |  n2.x = n2.x = 15
>3 :  n1 .x  =  35 |  n2.x = n2.x = 15

Burada önemli olan 11. satırda  `n1 = n2;`'de gerçekleşen olay bunu anlarsak nesneleri atama konusunu anlamış oluruz.
n1 artık n2'nin işaret ettiği nesneyi gösterir.

![]({{ site.assetsDir }}{{ page.permalink }}/javatutorial.png)
n1'in gösterdiği Sayi nesnesine ne olacak artık kullanılmıyor ?  burada javanın **Garbage Collector** devreye girecektir.  **Garbage Collector** konusunu daha sonra göreceğiz...
## Javada Operatörler
Operatörler programlama dilinde en temel işelemleri gerçekleştirmemizi sağlayan simgesel yapılardır. Java programlama dilinde oldukça fazla ve kullanışlı operatör alanına sahiptir.
1. Aritmetik Operatörler
2. İlişkisel Operatörler
3. Mantıksal Operatörler
4. Bitwise Operatörler 

Operatörler genelde işlem yaptıkları değişken ya da sabit sayısına göre kategorilendirirler tekli operatör (unary operator)  ya da ikili operatör (binary operator) ve  üç adet değişken yada sabite ihtiyaç duyan operatörlere üçlü operatör denir
**Unary Operator : **
```
-> operatör değişken //prefix (ön ek)
ya da
-> değişken operatör //postfix (Son ek )
```
**Binary Operator**
```
-> değişkenBir operatör değişkenIki  // (infix)ara ek 
```
**Üçlü Operatör** Javada üçlü operatör bir adettir.
```
-> değişkenBir ? değikenIki : değişkenUc
```


#### Aritmetik Operatörler


Opretör  | Açıklama 
:--- | ---:
+ |  Toplama 
- | Çıkarma
* | Çarpma 
/ | Bölme
% | Mod alma

```java
int x,y;
double z,h;
x = 5;
y = 9;
z = 6,66;
h = 3,35;
//Değişkenleri ekrana yazdıralım
System.out.println("Değişken değerleri : ");
System.out.println("x  : " + x);
System.out.println("y  : " + y);
System.out.println("z :  " + z);
System.out.println("h  : " + h);
 // örnek bir toplama işlemi
 System.out.println(" x + z : " + (x + z));
 //yine bir toplama işlemi
 double toplam = x + z;
 System.out.println(" x + z : " + toplam);
 // Çıkartma işlemi 
 System.out.println(" y - h : " + (y-h));
 // Bölme işlemi
 System.out.println(" y / x: " + (y/x));
 // Çarpma İşlemi 
 System.out.println(" x * y: " + (x*y));
 //Mod alma işlemi
 System.out.println(" y % x: " + (y%x));
```
> Çıktı:
> Değiken değerleri : 
> x :5
> y : 9
> z :6,66
> h:3,35
>  x + z :11,66 
>  x + z :11,66
>  y - h :6,65
>  y / x :1
>  x * y:45
>  y % x:4

#### Not : + ve - operatörleri karakter tipindeki verileri sayısal tipe dönüştüme görevi de üstlenirler.
```java
char ch = 'n';
int x = +ch;
int y = -ch;
System.out.println("ch = " + ch);
System.out.println("x = " + x);
System.out.println("y = " + y);
```
> Çıktı : 
> ch : n
> x : 78
> y : -78

Hazır yeri gelmişken **Casting** işlemine de değinelim..
#### Casting İşlemi (Tip Dönüşümleri)
Program yazarken belirlediğimiz değişkenleri başka bir değişkene dönüştmek gerekebilir bu tip durumlarda casting işlemini yani tip dönüşü uygularız.
peki java programlama dilinde tip dönüşümleri nasıl olur   ? 
```java 
public class Casting{
   public class void main(String[] args){
int x  = 21;
double y = (double) x;
double z = 5,38;
int h = (int) z;
long g = (long) z;
System.out.println("y : "+ y +"h : "+ h + "g :" + g);
   }
}
```
> Çıktı :
> y : 21.0  h :5 g : 5

Ufak bir not eğer eğer kesirli bir değere casting yaparsak dönüş yuvarlama işlemine göre gerçekleşir.
#### Bir arttırma ve Bir Azaltma 
Bazen program yaparken elimizdeki değikenlerin programın akışı sırasında belirlediğimiz değere kadar artmasını veya azalmasını isteyebiliriz. (yani bir sayaç mantığı ile çalışması)Arttırma ve Azaltma operatörleri adından da anladığımız gibi arttırmak ve azaltmak işlemlerini yaptığımız kısaltılmış yazım şekilleridir. Bu operatörler ön ve arka ek olarak (Ön ve arka ekleri biraz yukarıda göstermiştik) kullanılabilirler. Fakat buradaki  önemli kısım bu eklerin neye göre ön ya da arka olarak kullanıldığı yahut ön veya arka ek olarak kullanırsak ne olacağıdır.


 No | Operatör | Kullanımı 
:--- | ---: | :---
1 | ++ | degisken++
2 | ++ | ++degisken
3 | -- |  degisken--
4 | -- | --degisken

1.  `degisken++` Önce değişkenin değerini hesaplar daha sonra bir arttırır
2.  `++degsiken` Önce değişkenin değerini bir arttırır daha sonra değerini hesaplar
3.  `degisken--`Önce değişkenin değerini hesaplar daha sonra bir azaltır
4.  `--degsiken` Önce değişkenin değerini bir azaltır daha sonra değerini hesaplar


Hemen örneklendirmeye geçelim..

```java
public class ArttırmaVeAzaltma {
 
  static void yazdır(String p) { 
    System.out.println(p); 
  }
 
  public static void main(String[] args) {
 
    int degisken = 1; 
    yazdır("Değişkenin değeri : " + degisken);
    yazdır("++degisken : " + ++degisken);     
    yazdır("degisken++ : " + degisken++);     
    yazdır("Değişkenin değeri : " + degisken);
  } 
}
```
İlk önce ArttırmaVeAzaltma classı (Sınıfı) içinde **static** tanımlı yazdır adında bir method oluşturduk metotumuzun işlevi  System.out.println gibi çalışmak yani yazdır("...") şeklinde kullanmak bunu yapmamızdaki amaç System.out.println'i kısaltmak daha verimli kod yapısı oluşturmaktır. Bu konular daha detaylı bir biçimde işlenecektir. Gelelim main'de ne yaptığımıza.ilk önce adı degisken olan integer tipinde bir değişken tanımladık. Bu değişkene 1 değerini atadık ve hemen ardından ekrana yazdırdık. 
 > Değişkenin değeri : 1 


`++degisken`de değikenin değeri önce bir arttırdık daha sonra değişkeni yazdırdık.

> ++degisken : 2


`degisken++`da ilk önce değişkeni yazdırdık ve daha sonra değişkenin değerini bir arttırdık

> degisken++ : 2

En son satırda ise değişkenin son durumu görmek için tekrar ekrana yazdırdık ve çıktı şu şekilde oldu..

> Değişkenin değeri : 3

Burada sadece arttırma operatörlerini kullandık ama aynı işlemler azlatma operatörleri içinde geçerli olacaktır. Anlamamız gereken nokta değişkenlerin bu operatörlerle değerlerinin nasıl arttığıdır veya azaldığıdır.
### İlişkisel Operatörler

İlişkisel operatörler matematikte yaptığımız sorgulamaların java yazılım dilindeki gösterimidir. Bunlar iki değişkenin birbirlerine karşı olan durumlarını sorgulamamızı sağlarlar ve java dilinde kullanım şekilleri aşağıdaki tabloda yer almaktadır.

Operatör | Kullanımı | Koşul
:--- | ---: | :---
> | x>y  | Eğer x **büyükse** y'den TRUE değeri döner
 >=| x >=y |Eğer x **büyükse** **veya** **eşitse** y'den TRUE değeri döner
 <| x < y |Eğer x **küçükse** y'den TRUE değeri döner
 <=| x <= y |Eğer x **küçükse** **veya** **eşitse** y'den TRUE değeri döner
 ==| x == y |Eğer x **eşitse** y'ye TRUE değeri döner
!=|  x != y |Eğer x **eşit** **değilse** y'ye TRUE değeri döner

Gelin sizinle bir sayının tek yada çift oldğunu hesaplayan bir program yazalım..

>Henüz öğrenmediğimiz bir iki şey göreceğiz ama dersler ilerledikçe bunları açıklamış olacağız..

```java
import java.util.Scanner;

Public class IliskiselDeneme {
  public static void main(String[] args) {

	Scanner scan = new Scanner(System.in); // Javada kullanıcıdan değer almamızı sağlayan Scanner sınıfı

    System.out.println("Lütfen bir değer giriniz : ");
    int sayi = input.nextInt(); //int tipinden değer beklediğimizi javada belirtiyoruz..
   
    if(sayi%2 == 0){ 
        System.out.printf("%d çift bir sayıdır", sayi); //printf C dilinden miras alınmıştır println ile aynı işlevi görür ekrana yazdırmak için kullanırız. 
	}else{
        System.out.printf("%d tek bir sayıdır", sayi); // %d ise prinf içinde yazdıracağımız tam sayı anlamına gelmektedir.
	} 
    	/* burada printf'in kullanımına biraz daha değinmek istiyorum
	   Yukarıda %d yazdığımızda ekrana yazdıracağımız değerin bir tam sayı olduğunu belirttiğimizi söylemiştik
	   peki biz printf fonksiyonu içinde birden fazla tam sayı değeri ya da ondalıklı yazdırmak istersek ne yapmalıyız ? 
       öncelikle 2 adet değişken tanımlayalım
       int x = 2;
       double y = 3,14;
       şimdi de bu değişkenleri printf kullanarak ekrana yazdıralım
       System.out.printf("Tam sayı : %d Ondalıklı sayı : %f", x,y);
       */
      
  }
}
```
Yukarıda ki kodu açıklamak gerekirse, ilk önce Scanner sınıfını tanımladık daha sonra ekrana kullanıcıdan bir değer girmesini talep ettik.`input.nextInt()`'ile kullanıcıdan girilen değerin tam sayı olması gerektiğini javaya bildirdik. Daha sonra kullanıcının girdiği değeri integer tipinde sayi adlı değişkene atadık ve İF(KOŞUL) bloğunu açtık burada if koşuluna girilen değerin modunu aldırdık ve işlemin sonucu 0'a eşitse ekrana çift yazdırmasını istedik ELSE bloğunda(yani belirlemiş olduğumuz koşul sağlanmazsa else içinde yaptığımız işlerin gerçekleşmesini istedik)  girilen değerin modunun 1 olmaması durumunda ekrana tek sayı yazmasını istedik.Mesela kullanıcı 658 değerini girdiğini farz edelim çıktı şu şekilde olacaktır.
> 658 çift bir sayıdır.

### Mantıksal Operatörler

Mantıksal Operatörler birden çok karşılaştırma işlemini birleştirip tek bir koşul ifadesi şeklinde sorgulamak için kullanırız.


Operatör | Kullanımı |  Anlamı
:--- | ---: | :---
&& | x && y  | **VE** Operatörü
II | x II y | **VEYA** Operatörü
 ^| x ^ y | **YA DA** Operatörü
 ! | ! x | **DEĞİL** Operatörü
 
 Hadi bunlarıda örnek bir program üzerinde görelim. Bu sefer kullanıcan 2 adet değer girmesini isteyeceğiz ve girdiği değerlere göre kullanıcının burcunu ekrana yazdıracağız. (Burç konusundan hoşlanmıyorum ama bu konuyu en iyi özetleye bileceğim örnek olacak malesef :D )
 
```java
import java.util.Scanner;

public class Burclar {

	public static void main(String[] args) {

		Scanner scn = new Scanner(System.in);
		int gun,ay;
		System.out.print("Ay Giriniz:");
		ay=scn.nextInt();
		System.out.print("Gün Giriniz :");
		gun=scn.nextInt();

        if ((ay==1 && gun<=20)||(ay==12 && gun>=21)) {
            System.out.println(“Oğlak”);
        }else if((ay==1 && gun>=21)||(ay==2 && gun<=19)) {
            System.out.println(“Kova”);
        }else if((ay==2 && gun>=20)||(ay==3 && gun<=20)) {
            System.out.println(“Balık”);
        }else if((ay==3 && gun>=21)||(ay==4 && gun<=20)) {
            System.out.println(“Koç”);
        }else if((ay==4 && gun>=21)||(ay==5 && gun<=20)) {
            System.out.println(“Boğa”);
        }else if((ay==5 && gun>=21)||(ay==6 && gun<=21)) {
            System.out.println(“İkizler”);
        }else if((ay==6 && gun>=22)||(ay==7 && gun<=22)) {
            System.out.println(“Yengeç”);
        }else if((ay==7 && gun>=23)||(ay==8 && gun<=23)) {
            System.out.println(“Aslan”);
        }else if((ay==8 && gun>=24)||(ay==9 && gun<=23)) {
            System.out.println(“Başak”);
        }else if((ay==9 && gun>=24)||(ay==10 && gun<=23)) {
            System.out.println(“Terazi”);
        }else if((ay==10 && gun>=24)||(ay==11 && gun<=22)) {
            System.out.println(“Akrep”);
        }else if((ay==11 && gun>=23)||(ay==12 && gun<=21)) {
            System.out.println(“Yay”);
        }
	}
}
```
Hemen açıklayalım. 
ilk koşulumuz `(ay == 1 && (ve) gun <=20) II (ya da) (ay == 12 &&(ve) gun>=21) `
eğer kullanıcı ay değerini 1 girerse ve gün değeri 20den küçük eşitse burcu oğlaktır ya da ay değeri 12 ise ve girdiği gun değeri 21'e büyük veya eşitse burç oğlaktır. Yazdığımız çoklu koşul ifadelerini  bu şekilde açıklayabiliriz.


> NOT : Mantıksal Operatörlerden &&(VE), II (YA DA) tekli karakterli de kullanılabilir. Örneğin `ay == 1 & gun<=20` şeklinde de yazabilir arasındaki fark eğer çift karakterle yazarsak (&&, II ) koşul soldan işleme başlar ve ifade en sona gelmeden kesin bir sonuca ulaşılırsa ifadenin geri kalan kısmı görmezden gelinir ve program akışına devam eder.Eğer biz bu operatörleri tek karakterle yazsaydık (&,I) koşul kesin bir ifade ile sağlansa bile operatörün her iki yanındaki işlemler yapılmak zorunda olacaktı ve bu işlemler yapıldıktan sonra program akışına devam etmiş olacaktı.

**Önümüzdeki ders Javada 
Koşul ( İF, İF ELSE, İF ELSEİF ELSE, SWİTCH CASE) 
Döngü(WHİLE,DO-WHİLE,FOR) 
Dallandırma(BREAK,CONTINUE,RETURN) 
ve İstisna(TRY-CATCH-FİNALLY, THROW) konularını göreceğiz...**