## Emmet ile Daha Hızlı HTML Yapıları Oluşturmak

Emmet web geliştiricilerinin sıklıkla zamandan tasarruf etmek ve daha hızlı kod yazmak için kullandığı bir eklentidir. Emmet’in temel mantığı, yazılımcıya kodlama yaparken zaman kazandırmasıdır. Örneğin hepimiz bir html dosyasının iskeletini biliriz:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
</body>
</html>
```

Emmet sayesinde çok daha hızlı bir biçimde ! + Tab kullanarak bu yapıyı oluşturabilirsiniz. Bunu tek tek yazmaktansa iki tuşa basarak yapmak çok güzel değil mi?

Anlayacağınız üzere Emmet bazı kısa yollarla basit bir biçimde HTML ve CSS kodu yazmamıza yardımcı olur. Aynı kodu tekrar tekrar yazmanızı engellerken üretkenliğinizi de arttırmış olur. Emmet neredeyse tüm text editörlerinde mevcuttur, bu yüzden onu yüklemenize gerek yoktur. Ama herhangi bir nedenden IDE’nizde mevcut değilse [bu sayfadan](https://emmet.io/download/) yükleyebilirsiniz.

## Emmet’deki Kısa Yollara Gelecek Olursak...

Emmette kullandığımız bazı kısa yollar var, şimdi bunları örnekleriyle tek tek inceleyelim.

<b>1)</b>  - > ifadesini kullanarak kardeş element oluşturuyoruz.

Örneğin şekildeki, gibi ul tagı içerisinde li tagı oluşturmak istiyorsunuz. Bunun için yapmanız gereken tek şey ul>li yazarak Tab’a basmak.
```html
<ul>
  <li></li> 
</ul>
```
Bu işlemi yaptıktan sonra ul tagına eklemek istediğimiz bir kardeş eleman kalmayınca ise ^ ifadesini kullanarak ul tagı dışına çıkıp yeni taglar oluşturabiliriz.

Örneğin ul tagı içinde li tagı oluşturduktan sonra ul tagı dışında bir p tagı eklemek istiyorum. Bunun için ul>li^p yazarak taba basabilirim.
```html
<ul>
    <li></li> 
</ul>
<p><p/>
```
<b>2) </b> Peki ya bu ul tagı içerisine birden fazla li oluşturmak istiyorsam, ne yapmalıyım?

Bunun için * ifadesini kullanırız. ul>li*3 yaparak ul tagı içerisinde üç adet li tagı oluşturabilirsiniz.
```html
<ul>
  <li></li> 
  <li></li> 
  <li></li> 
</ul>
```

<b>3) </b> Bunu yerine benzer biçimde kardeş eleman-tag eklemek için + ifadesi de kullanılabilirdi: ul>li+li+li

<b>4) </b> Tag eklerken onlara class özelliği vermek için de . ifadesini kullanırız.

Örneğin ul.class1>li.class2 yazılarak tab tuşuna basıldığında:
```html
<ul class="class1">
    <li class="class2"></li>
</ul>
```
Bu şekilde bir kod oluşur. Aynı şekilde ul.class1>li.class2*3 denerek bir yerine üç adet class2 sınıfından li tagı oluşturulabilirdi.

<b>5) </b> Bir id özelliği eklemek için ise # ifadesini kullanırız. Yeni bir örnekle id özelliği eklemeyi görelim. ul#id1>li#id2 diyerek aşağıda gördüğünüz kodu oluşturabiliriz.
```html
<ul id="id1">
    <li id="id2"></li>
</ul>
```

<b>6) </b> Burada + ve * ifadesinin farkını da daha kolay anlayabiliriz.

Örneğin ul tagının içine aynı id’ye sahip 3 adet li eklemek istiyorsam * ifadesi kullanılabilir.

Fakat amacım farklı id’lere sahip üç adet li tagı oluşturmaksa ul>li#id1+li#id2+li#id3 yapılır.

<b>7) </b> Peki otomatik artış sağlayan değerleri tek tek yazmak amacımız zaman tasarrufu iken ne kadar mantıklı?

Emmet bunun için de bir kısa yola sahip ```:$``` ifadesi. Yani yukarda görmüş olduğunuz ul>li#id1+li#id2+li#id3 şeklinde yazdığımız kod bloğunu çok daha basit bir biçimde ul>li#idNo$*3 diyerek yazabiliriz.

Böylece otomatik olarak idNo1, idNo2 ve idNo3 idlerine sahip üç adet li tagımız olur.
```html
<ul>
  <li id="idNo1"></li>
  <li id="idNo2"></li>
  <li id="idNo3"></li>
</ul>
```
<b>8) </b> Sırada oluşturulan tagların içine text yazılması var:

Textlerimizi {} ifadesinin içine yazmamız yeterli: p{Emmet ile tag içine text yazma}
```html
<p>Emmet ile tag içine text yazma</p>
```

<b>9) </b> Bir diğer emmet kısa yolunu ise kodumuzda içerik olmadığı zamanlarda kullandığımız anlamsız yazıları yani “lorem ipsum”ları oluşturmak için kullanıyoruz.

Örneğin bir paragraf oluşturacaksınız ve bu paragrafın henüz bi içeriği yok fakat boş durmasındansa oraya metin geleceğini belirtmek istiyorsunuz veya metin geldiğinde nasıl görüneceğini görmek istiyorsunuz. Anlamsız harfler veya zaman gerektiren rastgele cümleler oluşturmak yerine bu kısayolu kullanabilirsiniz : p>lorem Taba bastığınızda aşağıdaki gibi bir çıktı alacaksınız.
```html
<p>Lorem ipsum dolor sit, amet consectetur adipisicing elit.Facere dolore sint ea? Molestiae ratione ullam, illo commodi ipsum soluta mollitia itaque,maiores maxime natus reiciendis architecto. Quaerat culpa beatae dicta.</p>
```
<b>10) </b> Bu kadar uzun bir lorem yazısı istemiyorsanız yapmanız gereken tek şey lorem yazdıktan sonra yanına kaç kelimeli bir lorem oluşturmak istediğinizi eklemek.

Örneğin 5 kelimeli bir lorem yazısı istiyorsunuz. Bunun için p>lorem5 yazmanız yeterli.
```html
<p>Lorem ipsum dolor sit amet.</p>
```
<b>11) </b> Son olarak Emmet’in bir özelliğinden bahsedeceğim. li.className yazıp Tab’a bastığımızda ne oluşmasını bekleriz? Evet className class’ına ait bir li tagı oluşmasını. peki herhangi bir tag koymaksızın sadece .className yazdıktan sonra Tab’a basarsak ne olur?

Cevap:
```html
<div class="className"></div>
```
Gördüğünüz gibi bir div oluşturdu. Emmet’e bir tag vermeksizin . veya # ifadelerini kullandığımızda bunun div tagı olduğunu biliyor.

Ama biz bunu ul tagı içinde denersek tepkisi ne olur? Hadi deneyelim!:
```html
<ul>
  <li class="className"></li>
</ul>
```

Gördüğünüz gibi ul>.className yazıp Tab’a bastığımızda ise bunun li elementi olduğunu algılıyor.

Emmet’in kendi sitesindeki cheat sheete [buradan](https://docs.emmet.io/cheat-sheet/) ulaşabilirsiniz. Bu konuda bol bol egzersiz yapmayı unutmayın lütfen, emin olun başta eliniz alışana kadar çok zorlansanız da emmet kullanımı çalışma hızınızı arttıracak ve sizi gereksiz çabadan kurtaracaktır.