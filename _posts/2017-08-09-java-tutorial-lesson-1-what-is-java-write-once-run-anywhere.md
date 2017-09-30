---
title: 'Java Tutorial - Lesson 1 : What is Java?  Write Once, Run Anywhere'
summary: 'Java Ders 1 : Java Nedir?'
image: java.png
permalink: java-tutorial-lesson-1-what-is-java-write-once-run-anywhere
date: '2017-08-10 01:30'
categories: k2
tags:
  - Hello World
  - Java
  - Programming
  - Tutorials
author: Nuri Çilengir
---
#### **Turkish-English**
## Java Nesne Yönelimli Programlama Nedir ?
Java, Sun Microsystems mühendislerinden **James** **Gosling** tarafından geliştirilmeye başlanmış,
*  **Açık kaynak kodlu**
*  **Nesneye yönelik**,
*  **Zeminden bağımsız**, 
*  **Yüksek verimli**, 
*  **Çok işlevli**,
*  **Yüksek seviye**,
*  **Adım adım çalışan** (yorumlanan-interpreted) bir dildir. 

Bunun anlamı Java bilgisayar sistemlerinin farklılıklarını baz alarak farklı sistemler üzerinde çalıştırlabilmesi düşücesiyle yapılmış bir projedir.Java'nın sloagnı olan bir defa yaz, her yerde çalıştır mantığı budur.Eğer bir MacOS işetim sistemiyle Java diliyle bir program yazmışsanız bunu programı Linux işletim sisteminde hiç birşey değiştirmeden çalıştırabilirsiniz.Java uygulamalarını çalıştımanız için geren ise herhangi bir Java Virtual Machine (JVM)'de çalışabilen tipik bytecode'dur (sınıf dosyası).Java,  Sun Microsystems tarafından tanımlanmış bazı kurallara sahiptir. Bu kurallara sadık kalındıkça JVM (Java Sanal Makinası) yada Java diline bağlı projeler oluşturulabilir. Örneğin, **Çöp Toplayıcı**  (**Garbage Collector**)
> Daha sonraki yazılarda **Garbage Collector**'den bahsedilecektir.

### Java ile ne yapılabilir ?
Kısaca aklınıza gelebilecek her şey.
* Grafiksel kullanıcı arayüz (GUI) uygulamaları; Applet'ler
* Veri tabanına erişim uygulamaları,
* Web tabanlı erişim uygulamaları; Servlet, JSP,
* Dağınık bileşenler (Distributed Components); Örneğin EJB, RMI,
* Akıllı telefonlar, cep telefonları, tabletler ve akıllı kartlar uygulamaları ve daha bir çok alanda tasarlanabilir ve geliştilebilir.

Kısaca bunları özetlemek gerekirse,
* **Appletler** bir tarayıcı içerisinde çalışan program parçasıdır ve web sayfalarına işlev katmak için programlamayla yapılabilecek işlemleri gerçekleştirir.

 ![]({{ site.assetsDir }}{{ page.permalink }}/Nasa-Word-Applet.jpg)

* **Servlet** Java programlamada dinamik web sayfaları üretmek için bir çok yol vardır Java Servlet bunlardan bir tanesidir.
![]({{ site.assetsDir }}{{ page.permalink }}/Servlet_HelloServletURL.png)

*  **JSP**, Servlet uzantısıdır, HTML içerisine yazdığımız JSP kodları sunucuda Servlet' e çevrilir. JSP' ler Java Beans' ler ile çalışır ve daha rahat bir geliştirme imkanı sunar.

	![]({{ site.assetsDir }}{{ page.permalink }}/web-bookstoreRequestFlow.gif)
*  **EJB** ; tüm uygulama sunucularında çalışabilen bir bileşen modeldir.J2EE sunucuları, enterprise bean'lerin dağıtık yapısını, güvenliği, ağdaki yeri saklanması gibi konuları hallederler. Programcıya sadece bean'de neyin nasıl yapılacağını belirtmek kalır. J2EE'nin temel bileşeni EJB olarak düşünülebilir.

 ![]({{ site.assetsDir }}{{ page.permalink }}/overview-serverAndContainers.gif)
*  **RMI** yani : Remote Method Invocation Uzak Metod Çağırma.Uzak nesne haberleşmesinde kullanılan RMI Java nın dağıtık nesneleri için destek sağlar. RMI uzak nesneler üzerindeki metodların çağrılmasına izin verir.RMI dağıtık nesneler kullanılarak dağıtık uygulamalar gerçekleştirmek için kullanılan yüksek seviyeli Java API’sidir

 ![]({{ site.assetsDir }}{{ page.permalink }}/Java-RMI.gif)
 
###  Java Paket Sisemi
Paket denilen şeyi aslında,  başkalarının yazıp java içerisinde kullanılacak şekilde hazırladığı program parçaları olarak ele alabiliriz.Yani paketler içinde programımızı yazmamız için bazı özel özellikler (Dosya işlemleri, Network işlemleri vs. ) bulunduran bir araçtır.Biz uygulumamızı bu paketler üzerinden yazarız ve bu bize var olan özellikleri yeniden yazmak yerine paket içinden kullanmamızı sağlar.Paketlere aynı zamanda Sınıf Kütüphaneleri (Class Libary) de deriz.

### JDK(Java Development Kit)
Java'da yazılan programların derlenip çalıştırılmalarını sağlar ve içinde çok sayıda kütüphane bulundurur.JDK'nın içinde Java Compiler, Java Interpreter, Toollar, API kütüphaneleri, JVM, JRE ve Java dökümantasyonlarını içerir.

### JRE (Java Runtime Environment)
Bir java uygulamasını çalıştırmak için gerekli minimum araçları içeren yapıdır.

### JVM (Java Virtual Machine)
Java'nın platform bağımsız olması demek, herhangi bri makinede yazılmış ve bir işlemci ile derlenmiş bir java uygulamasını, tek bir noktasını bile değiştirmeden başka bir makine ya da işlemci altında çalıştırabilmesi JVM'den(Java Virtual Machine) gelir.
 
###  Java Nasıl Çalışır ? 
![]({{ site.assetsDir }}{{ page.permalink }}/image004.jpg)
Bir programı derlemek için **javac**  komutunu kullanırız (Java derleyicisi).Örnek olarak, Merhaba.java adlı bir programı derlemek için şunu kullanırız :
```
javac Merhaba.java
```

Java compiler  java kaynak kodunu byte koda çevirir. Çevrilen Bytecodes  Java Virtual Machine (JVM) tarafından çalıştılır.Virtual machine (VM) bilgisayarı simule eden bir uygulamadır fakat  kendisiyle iletişime geçen programlardan işletim sistemini gizler. Yani **javac** komutu ile kaynak kod derlenir sonucunda ***Byte kod*** elde eldilir. Daha sonra **java** komutuyla çalıştırılır. Byte kod oluşulurken proje içerisindeki class için fiziksel bir **.class** dosyası oluşurulur.  



 
 


## What is Java Object-Oriented Programming?
Java started to be developed by James Gosling, a Sun Microsystems engineer.
Java has features like 
*  **Open Source**,
* **Object Oriented**,
* **Platform Independent**,
* **Highly Efficient**,
* **Multifunctional**,
* **High Level**,
* **Interpreted**.

This means that Java computer systems can run on different systems based on their differences.The phrase "**run once, run everywhere**" is based on this logic.If you have written a program in Java on a MacOS operating system, you can run it without changing anything in the Linux operating system.Typical ByteCode (class file) that can run in any Java Virtual Machine (JVM) if it is necessary to run Java applications.Java has some rules defined by Sun Microsystems.As long as you stick to these rules, you can create Java language-dependent projects on the JVM (Java Virtual Machine).For example, **Garbage Collector.**
> Later articles will mention the Garbage Collector feature.

### What can be done with Java?
In short, everything you can think of can be done.
* Graphical user interface (GUI) applications; applets
* Applications that access the database,
* Web based access applications; Servlet, JSP,
* Distributed Components; For example, EJB, RMI,
* Smartphones, mobile phones, tablets and smartcard applications and many more can be designed and developed.

To summarize them briefly,
* **Applets** are part of a program that runs in a browser and performs operations that can be done by programming to add functionality to web pages.

 ![]({{ site.assetsDir }}{{ page.permalink }}/Nasa-Word-Applet.jpg)
* **Servlets** There are many ways to generate dynamic web pages in Java programmers Java Servlets are one of them.

 ![]({{ site.assetsDir }}{{ page.permalink }}/Servlet_HelloServletURL.png)
* **JSP** is the Servlet extension, and the JSP code we write in the HTML is converted to Servlet on the server. JSPs work with Java Beans and provide more comfortable development.

 ![]({{ site.assetsDir }}{{ page.permalink }}/web-bookstoreRequestFlow.gif)
*  EJB; A component model that can work across all application servers. J2EE servers handle issues such as the distributed structure of enterprise beans, security, storage on the network, and so on. It's up to the programmer to just specify what is done in the bean. The basic component of J2EE can be thought of as EJB.

 ![]({{ site.assetsDir }}{{ page.permalink }}/overview-serverAndContainers.gif)
RMI yani : Remote Method Invocation.RMI used in remote object communication provides support for Java's distributed objects.RMI allows calling methods on remote objects.RMI is a Java API used to make distributed applications using distributed objects.
 ![]({{ site.assetsDir }}{{ page.permalink }}/Java-RMI.gif)
### Java Package System
We can treat packages as program pieces that others write and prepare to use in java.In other words, we have some special features  in packages for writing our program (file operations, network operations, etc.).We write our implementation through these packages.That is, packages prevent us from rewriting a feature. We use these features from within packages.
### JDK(Java Development Kit)
JDK allows you to compile and run programs written in Java, and it contains a large number of libraries.The JDK contains Java Compilers, Java Interpreter, tools, API libraries, JVM, JRE, and Java documentation.
### JRE (Java Runtime Environment)
JRE is a structure that contains the basic tools necessary to run a java application.
### JVM (Java Virtual Machine)
Java's platform independence means that a Java application written on any machine and compiled with a processor can be run on another machine or processor without changing a single point, thanks to the Java Virtual Machine.
### How Does Java Work?
 ![]({{ site.assetsDir }}{{ page.permalink }}/image004.jpg)
 We use ** javac ** command to compile a program (Java compiler).As an example, to compile a program called Hello.java we use:
 ```
javac Hello.java
```
Java compiler translates java source code into byte code. Translated Bytecodes are run by the Java Virtual Machine (JVM). A virtual machine (VM) is an application that simulates a computer, but its communication hides its operating system from passing programs. That is,  source code is compiled with  javac  command and BYTE code is generated. It is then executed with the java command.When the bytecode occurs, a physical X file is created for the class in the project.