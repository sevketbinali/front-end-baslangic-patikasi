# HTML Etiketleri

## HTML Etiketi

    HTML etiketi, dosya içeriğinin HTML dilinde yazıldığını tarayıcımıza bildirir. Bu etiket, kendi altında mutlaka <head> ve    <body> etiketlerini barındırmalıdır. Eğer bir HTML dökümanı oluşturmak isterseniz ilk yapacağınız iş bir <html> etiketi oluşturmaktır. Ardından HTML etiketi altına <head> ve <body> etiketlerini yazmalısınız.

```html
<html>
  <head></head> 
  <body></body>
</html>
```

## HEAD Etiketi

    <head> etiketi, site ziyaretçileri tarafından görülmesi gerekmeyen kodları içerir. Bu etiket altına yazılan kodlar genellikle arama motorları ve örümcekler (Crawler veya Spider diye geçer) içindir. Head etiketi altında bütün etiketleri kullanabilmeniz mümkün değil. Kullanabileceğiniz etiketler;

    <title> (Bu etiketi kullanmak şarttır.)
    <meta>
    <style>
    <script>
    <noscript>
    <link>
    <base>

```html
<html>
  <HEAD>
    <title> Sekmede Görülecek İsim </title>
    <meta name="Keywords" content="HTML,Kodluyoruz">
  </HEAD> 
  
  <BODY></BODY>
  
</html>
```
## BODY Etiketi

    Web sayfamızda görmek istediğimiz bütün içerikleri <body> etiketi altına yazıyoruz. Anlatacağım diğer etiketleri <body> etiketi içerisine yazacağız.
```html
<html>
  <HEAD>
    <title> Sekmede Görülecek İsim </title>
    <meta name="Keywords" content="HTML,Kodluyoruz">
  </HEAD> 
  
  <BODY>
    Site İçeriği
  </BODY>
</html>
```

    Not:

    Şu ana kadar oluşturduğumuz yapıyı idelerde kısayollar ile hızlıca oluşturabiliyoruz. Ben Visual Studio Code (VSC) kullanıyorum. VSC üzerinde "! + Enter" yazarak aşağıdaki yapıyı hızlıca oluşturabilirsiniz.

    <!DOCTYPE html> : Dökümanımızın HTML dilinde olduğunu tarayıcımıza bildiren talimattır. <html lang="en"> : Site içeriğinin dilini belirten etiket, "en" yerine "tr" yazabilirsiniz.

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

## H Etiketleri

    H etiketleri başlık etiketleridir. Büyükten küçüğe sırasıyla
 ```html  
<h1>
<h2>
<h3>
<h4>
<h5>
<h6>
```
Not: HTML otomatik olarak Başlık etiketlerinin öncesine ve sonrasına satır atlatır.

## P Etiketi

    <p> etiketi paragraf etiketidir. Sayfa içerisinde oluşturacağımız metinleri <p> etiketi ile oluştururuz. Aşağıdaki örnekte hem başlık etiketi hem de paragrafa etiketini kullandım.

Not: HTML otomatik olarak Paragraf etiketinin öncesine ve sonrasına satır atlatır.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h2>Kodluyoruz</h2>
    <p>HTML Etiketleri</p>
</body>
</html>
```

## BR Etiketi

    <br> etiketi satır atlatma etiketidir ve kapatmaya ihtiyaç duymayan etiketlerden biridir. Atlatmak istediğiniz satır sayısı kadar <br> etiketi kullanabilirsiniz. NOT: BR etiketinin farklı kullanımlarını görebilirsiniz. örn.(<br>,<br/>,<br />) Hepsi aynı işlevi yerine getirir 

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h2>Kodluyoruz</h2> <br>
    <p>HTML <br> Etiketleri</p>
</body>
</html>
```

## A Etiketi

    <a> etiketinin en önemli özelliği href özelliğidir. Bu etiket ile sayfaları linkleyebiliriz. Etiket içerisine yazılan içerik sayfa üzerinde gösterilecek içeriktir. href içine yazılan ise tıklandığında gideceği URL'dir.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <a href="https://www.kodluyoruz.org">Kodluyoruz</a>
</body>
</html>
```

## UL - OL - Li Etiketi

    <ul> ve <ol> etiketleri liste oluşturma etiketleridir. Listeyi oluşturduktan sonra içeriğini oluşturmak için <li> etiketini kullanıyoruz.

    <ul> = "unordered list" sırasız liste anlamına geliyor. <ol> = "ordered list" sıralı liste anlamına geliyor.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
   
    <ul>
        <li>HTML</li>
        <li>CSS</li>
        <li>JavaScript</li>
    </ul>
    
    <ol>
        <li>HTML</li>
        <li>CSS</li>
        <li>JavaScript</li>
    </ol>
    
</body>
</html>
```

## HR Etiketi

`<hr>` etiketi konusal bir geçişi temsil eder. Yazı yazarken yeni bir paragrafa başlamaya benzetebiliriz. Varsayılan olarak sayfaya yatay bir çizgi ekler ama bu özelliği değiştirilebilir. Bu etiket kapatılmaya ihtiyaç duymaz.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <p>
      HTML yani Hiper Metin İşaretleme Dili, web sayfalarında gördüğümüz iskelet
      yapısını oluşturmak için kullanılan metin işaretleme dilidir.
    </p>

    <hr>

    <p>
      CSS, HTML elementlerinin çeşitli medya araçlarında nasıl ekrana
      yansıtılacağını tanımlayan bir dildir. Tek seferde birden çok sayfa için
      kurallar belirtebilir.
    </p>

    <hr>

    <p>
      JavaScript, HTML ve web için bir programlama dilidir. Dinamil olarak HTML
      içeriğini ve özelliklerini, CSS'i değiştirebilme gibi işlemleri
      gerçekleştirebilir.
    </p>
  </body>
</html>
```

## STRONG ve B Etiketi
    <strong> etiketi bir metinin arama motorlarına önemli olduğunu bildirmek için kullanılır. Kullanıldığı zaman metini kalın yapar. Eğer sadece metini kalınlaştırmak isterseniz <b> etiketini kullanabilirsiniz.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h2><strong> Kodluyoruz </strong></h2>
    <p><b> HTML </b> Etiketleri </p>
</body>
</html>
```

## Script Etiketi

    <script> etiketi JavaScript kodlarını HTML içerisine yazabilmemizi sağlar.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script>
        document.write("Kodluyoruz")
    </script>
</body>
</html>
```

## Button Etiketi

    <button> etiketini buton oluşturmak için kullanırız. Buton üzerine yazmak istediğiniz içeriği etiketin içine yazmanız yeterlidir.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <button> Buton </button>
</body>
</html>
```

## img Etiketi

    Resim eklemek için<img> etiketini kullanıyoruz. <img src=”resim.jpg” alt=”açıklama yazısı” /> src="" kısmına eklemek istediğimiz görselin yolunu yani kaynağını yazmalıyız. Eğer görselimiz ve HTML dosyamız aynı klasörde ise görselin adını ve uzantısını yazmamız yeterlidir. alt="" kısmına görselin açıklamasını yazıyoruz fakat isterseniz boş bırakabilirsiniz. Bu etiket kapanmaya ihtiyaç duymaz.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <img src=”görseller/kodluyoruz.jpg” alt=”Kodluyoruz Bootcamp” />
</body>
</html>
```

## iframe Etiketi

    Belge içinde belge gösterebilmemizi sağlayan etikettir. Genelde başka bir sitedeki belgeyi kendi sayfamızda göstermek için kullanırız. örn: Youtube'dan bir videoyu sayfamızda göstermek istersek <iframe> kodlarını sayfamıza eklememiz yeterli.(video üzerinde sağ tıklayıp yerleştirme kodunu kopyala diyerek iframe kodunu kopyalayabiliriz.)
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <iframe width="1519" height="581" src="https://www.youtube.com/embed/BHPYQHnD_QA" frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen></iframe>
</body>
</html>
```

## Yorum Satırı

    HTML dilinde yorum satırı<!-- ile başlar --> ile biter.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- Örnek Yorum Satırı -->
    
    <!-- 
        2. Örnek Yorum Satırı 
    -->   
</body>
</html>
```