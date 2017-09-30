---
title: 'Java Tutorial - Lesson 2 :  Everything is object'
summary: This lesson will describe the object class and data types in Java
image: java.png
permalink: java-tutorial-lesson-2-everything-is-object
date: '2017-09-25 13:19'
categories: k2
tags:
  - Class
  - Data Types
  - Haep
  - Hello Friend
  - Java
  - Nesne
  - Object
  - Open Source
  - Programming
  - Sınıf
  - Stack
  - Tutorials
author: Nuri Çilengir
---
## Herşey Nesne !
Java dilinde yazılan herhangi bir program çalışırken nesneler oluşturur ve bu yüzden javada herşeye nesne gibi davranılır. Nesneleri kullanmak için ise referanslara ihtiyaç duyarız.
Örnek vermek gerekirse,
günlük hayatta neredeyse her yerde kullandığımız kumandalar. Elimizde bir televizyon kumandası var biz bu kumandayla eğer bir televizyonumuz varsa onu kontrol edebiliriz sesini açar ya da kısar veya kanal değiştiririz ve bunun gibi uygulamaları televizyon kumadasıyla yaparız.Aslında bu örnek biraz yetersiz kalıyor çünkü elimizde bir kumanda olması onu yönetebileceğimiz televizyonun ya da herhangi bir cihazın olduğu anlamına gelmiyor. Mesela javada bu şunu gösterir.
```java
String kumanda;
```
Biz burada **String** veri tipinde bir referans tanımladık fakat kumanda referansına bağlı her hangi bir televizyonumuz ya da cihazımız yok.Bu yüzden biz bu kumanda referansına bir nesne yani bir televizyon  atamak istersek şu şekilde yapmalıyız.
```java
String kumanda = new String("Televizyon");
```
Burada String tipindeki bir referansa yine String tipinde bir nesne atadık. Peki **NESNE** nedir ?
### Nesne (Object) ve Sınıf (Class) nedir ?

#### Nesne (Object) Nedir ? 

Javada nesneler sınıflar tarafından üretilir(Sınıf nedir ? ona da geleceğiz. ). Bu sefer bir telefonumuz olduğunu düşünelim. Bu telefonun bir çok özelliği bulunur mesela bilmem kaç GB veri depolama, bilmem ne MP kameraya sahip olma ya da mesaj gönderme, internete bağlanma gibi. Elinizdeki bu X markanın Y modeli telefonundan dünyada milyonlarca bulunmaktadır. Elimizdeki telefon nesneyi  ve “Y” modeli ise sınıfı temsil eder.Telefonun fiziksel özelliklerini nesnenin **durumu** olarak görür ve yazılımsal işlevlerini **davranışları** olarak görürsek nesne mantığını aslında her programlama dilinde çözmüş oluruz.Öte yandan nesneleri kitap cümleleriyle tanımlamak gerekirse;
> Belirli bir sınıfa ait olan ve o sınıfın imkanlarına sahip olan veri tipleridir ve nesneler bizim oluşturduğumuz veri tipleridir.

```
Sinif_Adi Nesne_Adi = new Sinif_Adi();
```

 #### Sınıf (Class) Nedir ? 
 
Sınıflar nesnelerin tüm özelliklerini içeren şablonlardır. X marka telefonun Y modelinin tüm işlevlerini ve özelliklerini yani durum ve davranışlarını sınıflar barındırır.

```
class Sinif_Adi {
               // ifadeler;
                ..
}
```



-----
## Temel Veri Tipleri

Veri Tipi | Uzunluk | En Çok| En Çok | Sınıfı
:--- | ---: | :---| :---
boolean | - | - | true  ya da  false | Boolean
char | 16-bit | Unicode 0 | Unicode 2^16-1 | Character
byte | 8-bit | -128 | 127 | Byte
short | 16-bit | -32,768 | 32,767 | Short
int | 32-bit | -2,147,483,648 | -2,147,483,647 | Integer
long | 64-bit | -2^63 | -2^63-1 | Long
float | 32-bit | IEEE 754 (Kesirli Sayı) | IEEE 754 | Float
double | 64-bit | IEEE 754 Kesirli Sayı) | IEEE 754 | Double
void | - | - | -| Void

Veri tipleri bize değişkenlere atayacağımız verilerin tiplerini ayırt etmemizi sağlar.

* **Byte:** byte veri tipi bellekte 1 byte yer kaplar. Bu yüzden Java'da ki en küçük veri tipidir.
* **Char:** char veri tipi bellekte 2 byte yer kaplar ve işaretsiz tam sayıdır.Char veri tipi içiresine girilen sayının **UNİCODE** karşılığını saklar.Yani sadece bir harflik karakter saklar.
* **Short:** short veri tipi bellekte 2 byte ye kaplar. İçerisinde kısa tam sayıları tutar.
* **Int:** int veri tipi integer(tam sayı) kelimesinin kısaltılmış halidir. Bellekte 4 byte yer kaplar ve orta uzunluktaki sayıları tutar.
* **Long:** int veri tipinin taşıyamacağı büyğklükteki sayıları tutar ve bellekte 4byte yer kaplar.
* **Double:** Double veri tipi ondalıklı sayıları tutmak için kullanılır. Bellekte 8 byte yer kaplar.15 haneye kadar duyarlıdır.
* **Float:** Float veri tipi double gibi ondalıklı veri tiplerindendir. Bellekte 4 byte yer kaplar ve 7 haneye kadar duyarlıdır.
> Java programlama dilinde float değişkenleri tanımlanırken değerin sonuna **F** koyulur. Bunun nedeni yazılan sayının double olarak anlaşılmasını engellemektir.
* **Boolean:** Boolean bir mantıksal veri tipidir. Bellekte  1byte yer kaplar. Bunu mantıksal işlemlerin sonuçlarını kontrol etmek için kullanırız. Boolean bize **true** ya da **false** değerini döndürür.


Veri tiplerinin kullanımı ;

``` java
public class veriTipleri {
 
    public static void main(String[] args) {
 
        byte d1 = 9;
        short d2 = 35;
        int d3 = 1997;
        long d4 = 1234567;
        float d5 = 35.5f;
        double d6 = 345.2;
        char d7, d8;
        d7= 78;
        d8 = 'N';
        boolean d9 = true;
        boolean d10 = false;
 
        System.out.println("byte Tipinin Değeri: " + d1);
        System.out.println("short Tipinin Değeri: " + d2);
        System.out.println("integer Tipinin Değeri: " + d3);
        System.out.println("long Tipinin Değeri: " + d4);
        System.out.println("float Tipinin Değeri: " + d5);
        System.out.println("double Tipinin Değeri: " + d6);
        System.out.println("char Tipinin Değeri 1: " + d7);
        System.out.println("char Tipinin Değeri 2: " + d8);
        System.out.println("boolean Tipinin Değeri: " + d9);
        System.out.println("boolean Tipinin Değeri: " + d10);
    }
}
```

Çıktısı ise şu şekildedir.
> byte Tipinin Değeri: 9
> short Tipinin Değeri: 35
> integer Tipinin Değeri: 1997
> long Tipinin Değeri: 1234567
> float Tipinin Değeri: 35.5f
> double Tipinin Değeri: 345.2
> char Tipinin Değeri: N
> char Tipinin Değeri: N

### Depolanan Veriler Nerede Tutulmaktadır ? 

![]({{ site.assetsDir }}{{ page.permalink }}/Java-Heap-Stack-Memory-Nuri-Cilengir.png)

Depo toplam 4 alandan oluşur.

* **Stack(Yığın)**: Bulunduğu nokta belleğin(RAM) içindedir. Bu alanda bulunan **stack pointer** (yığın işaretçisi) doğrudan işlemciden donanım yardımı alır. Stack Pointer 'in aşağı inmesiyle yeni bir bellek alanı oluşturur, stack pointer 'in yukarı çıkması ile bellek alanı boşaltır. Stackte önemli nokta referansların kendilerinin tutulmasıdır. Stackte Java derleyicisi tutulacak verilerin uzunluklarını ve ömürlerini bilmek zorundadır. Stack alan progam çalıştığı andan itibaren belirlenir daha sonra bu alanın boyutu değiştirilemez. 
* **Heap**: Stack alana göre daha geniş ve kalıcı bir alandır. Genellikle ne kadar yer kaplayacağı belli olmayan nesneleri burada tutarız. Heap  alanın dezavatajı ise hızdan ödün vermektir.
*  **Statik Alan** : Bu bölge de  RAM'in üzerinde bulunur. Statik alanda veriler programın çalıştığı süre boyunca tutulurlar. Tüm nesneler bu statik verileri görebilirler. Bir veriyi statick yapmak için başına ***static*** anahtar kelimesi gelmelidir.
*  **Sabit Disk**: Programda bazen uygulama sonlandıktan sonra tutmak istediğimiz verileri sabit diskte tutarız.