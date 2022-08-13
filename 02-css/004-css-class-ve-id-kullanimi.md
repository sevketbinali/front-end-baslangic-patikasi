# Class ve ID Kullanımı 

Web sayfamızı oluştururken HTML elementlerimize bazı stil özellikleri eklemek isteriz. Bazı yazıların renkli, bazı resimlerin küçük veya bazı butonların farklı şekilde olması gerekebilir ve biz de bunun için CSS kullanırız.

Aşağıda html elementlerine nasıl stil özellikleri eklediğimize bakalım.

```css
<p>Bugün kodluyoruz</p>
<p>Yarın da kodluyoruz<p>
p {
	color: red;
}
```
**Sonuç:**
![sonuc](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/css/css-ile-class-ve-id-kullanimi/assets/Screenshot_1.jpg)

Yukarıda görüldüğü üzere iki farklı ``` <p></p> ```elementimize kırmızı renk özelliği eklemiş olduk. Fakat sadece belirli ```<p></p>``` elementine istediğimiz herhangi bir özelliği eklemek istersek ne yapacağız? Bu durumda class veya id seçicilerini kullanmamız gerekiyor.

## class Kullanımı

Class seçicisi, HTML üzerinde aynı class’a sahip elemana ulaşmamızı sağlar.

Class seçicisi CSS’de . ile belirtilir.
```css
.class{
     özellikler
}
<h4>Birinci Başlık</h4>
<h4>İkinci Başlık</h4>
<h4>Üçüncü başlık</h4>
```

Yukarıda 3 adet ```<h4></h4>``` elementimiz bulunuyor. Bunlardan sadece ikincisine kırmızı renk özelliği eklemek istersek class seçicisini kullanabiliriz.

```html
<h4>Birinci Başlık</h4>
<h4 class="text-red">İkinci Başlık</h4>
<h4>Üçüncü Başlık</h4>
```

Daha sonra bunu istediğimiz özelliği ekleyelim.
```css
.text-red{
   color:red;
}
```

**Sonuç:**

![sonuc](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/css/css-ile-class-ve-id-kullanimi/assets/Screenshot_2.jpg)

Bir class’ı birden fazla HTML elementi için kullanabiliriz.
```css
<h4>Birinci Başlık</h4>
<h4 class="h-green">İkinci Başlık</h4>
<h4 class="h-green">Üçüncü Başlık</h4>

.h-green {
   color:green;
}
```
**Sonuç:**

![sonuc](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/css/css-ile-class-ve-id-kullanimi/assets/Screenshot_3.jpg)

Eğer bir HTML elementinin birden fazla class özelliğine sahip olmasını istiyorsak aynı anda iki farklı class’ı kullanabiliriz. Bunun için sadece iki class arasına boşluk bırakmak yeterli olacaktır.
```css
<h4>Birinci Başlık</h4>
<h4 class="h-blue">İkinci Başlık</h4>
<h4 class="h-blue thick">Üçüncü Başlık</h4>

.h-blue{
    color:blue;
}
.thick{
       font-style: italic;
}
```

**Sonuç:**
![sonuc](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/css/css-ile-class-ve-id-kullanimi/assets/Screenshot_4.jpg)

Bir HTML elementi kendini kapsayan elementin (parent elementi) stil özelliklerine sahip olur.
```css
<div class="intro"><p>Birinci Paragraf</p><p>İkinci Paragraf</p>

</div>
.intro{
    color:pink;
 }
 ```

**Sonuç:**

![sonuc](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/css/css-ile-class-ve-id-kullanimi/assets/Screenshot_5.jpg)

Yukarıda  ```<div></div> ``` elementine CSS özelliği ekledik fakat altındaki elementler (child elementleri) de bu özelliğe sahip oldu.

## id Kullanımı

ID seçicisi, HTML üzerinde aynı id’ye sahip elemana ulaşmamızı sağlar.

ID seçicisi CSS’de # ile belirtilir.

ID seçicisinin kullanım amacı olarak class seçicisinden bir farkı yok diyebiliriz. İkisi de belirli HTML elementlerine CSS özellikleri eklemeye yöneliktir. Fakat id seçicisinin class seçicisinden bazı farkları vardır.

#id {
     özellikler
}

Bir id’yi sadece bir HTML elementi üzerinde kullanabiliriz.

<h4 id="main-title">Birinci Başlık</h4>
<h4>İkinci Başlık</h4>
#main-title{
	color:red;
}

**Sonuç:**
![sonuc](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/css/css-ile-class-ve-id-kullanimi/assets/Screenshot_6.jpg)

Aşağıdaki yanlış bir kullanımdır!

<p id="title">Birinci paragraf</p>
<p id="title">İkinci paragraf</p>

Bir html elementinin sadece bir tane id’si olabilir.

Aşağıdakiler yanlış kullanımlardır.

<p id="title" id="text-green">Birinci paragraf</p>
<p id="title text-blue">İkinci paragraf</p>

Böyle kullanımlar geçerli değildir.




