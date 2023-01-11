# <center> CSS </center>

<center><img align="center"
  src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d5/CSS3_logo_and_wordmark.svg/1200px-CSS3_logo_and_wordmark.svg.png"  width="90px"></center>

<hr>

## ❓ z-index?

- Üst üste gelen bloklarınız varsa bunların sırasını belirtir.

- En arkada kalmasını istediğiniz bloklar için genellikle -9999 değeri kullanılır.

- Apartman katları gibi düşünülebilir.

- Sayı büyüdükçe blok üst kata çıkar. Z-index’i 1 olan blok, Z-index’i 2 olan blok parçasının altında kalacaktır. [Deneyiniz...](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index)

<hr>

## ❓ Display flex?

- Boyutları bilinmeyen-dinamik alanları daha kolay yönetmek için W3C bize "Al abicim sana flex, istediğin gibi alanını yönet" demiş. 

- Hatırlarsınız, eskiden öğeleri sağa-sola dayamak için "float" kullanır, dikey ortalamak için CSS’e takla attırırdık.

- Ancak flex yapısı ile, artık kapsayıcıya (container) ve içindeki öğelerine esneklik getirebiliyoruz.

- Flex’i kullanmamızın en büyük sebebi, esnek yapıları kolayca yönetmek için.

- Çünkü yapıya esneklik verdiği için, yatay ve dikey hizalarda nasıl görüneceğini, öğelerin kendi içinde hizalanmalarını ve sırasını belirlemek gibi güzel özellikleri bulunuyor.

- Ayrıca tüm çözünürlüklerde ve cihazlarda daha hızlı ve esnek bir yapı kullanmak için, flex bizim tamda ihtiyacımız olan şey.

- Kullanılan özellikler 👇

    - [flex-direction](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-direction)

    - [flex-wrap](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-wrap)

    - [flex-flow](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-flow)

    - [justify-content](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content)

    - [align-items](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items)

    - [align-content](https://developer.mozilla.org/en-US/docs/Web/CSS/align-content)

<hr>

## ❓ Margin padding arasındaki fark nedir?

<center><img align="center"
  src="https://media.geeksforgeeks.org/wp-content/uploads/cssmarginandpadding.png"  width="500px"></center>

- "Margin" dediğimiz şey “dış kenar boşluğudur”.

- "Padding" ise “iç kenar boşluğu” olarak tanımlanabilir.

<hr>

## ❓ Media Query & Responsive Tasarım?

- Web üzerinde trafik yoğunluğunun %90’ı mobilden geliyor. Bu yüzden tasarlanan web sitelerinin mobil kullanıma uygun bir şekilde responsive tasarıma sahip olması gerekiyor, bu konuda CSS media query yapısı büyük rol oynuyor.

- Büyük ekranlardaki içeriği küçük ekranda uygun olarak göstermek için veya farklı ekran boyutlarında sayfa içeriğini taşma, kayma yapmaması için medya sorgu yapısı kullanılıyor. Web siteleri kodlanırken farklı mobil ekran ölçülerine göre responsive CSS kodları ile optimize hale getiriliyor.

- Media query ile spesifik ekran genişliklerinde HTML elemanlarına CSS kodları uygulanabiliyor.

- <b>"Min-width"</b> kullanıldığında medya sorgusunun altına yazılan CSS kodları <b>belirtilmiş olan piksel değerinin üzeri için geçerli olur.</b> Aşağıdaki örnekte "en fazla 751 piksele kadar" p etiketinin font büyüklüğü 17 piksel olarak belirtilmiştir.

```css
@media (min-width: 751px) {
   p {
     font-size: 17px;
   }
}
```

- <b>"Max-width"</b> kullanıldığında, medya sorgusunun altına yazılan CSS kodları <b>belirtilmiş olan piksel değerinin altı için geçerli olur.</b> Aşağıdaki örnekte olduğu gibi en fazla 750 piksele kadar p etiketinin font büyüklüğü 14 piksel olarak belirtilmiştir.

```css
@media (max-width: 750px) { 
   p {
     font-size: 14px;
   }
}
```

- <b>"Orientation: landscape"</b> kullanımında <b>medya sorgusunun altına yazılan CSS kodları mobil cihazlar yatay konuma getirildiğinde geçerli olur.</b> Aşağıdaki örnekte mobil cihaz [yatay konuma](https://juniortoexpert.com/wp-content/webp-express/webp-images/uploads/media-query-orientation-landscape-2-300x147.png.webp) geldiğinde kutunun rengini değiştirecek CSS kodu belirtilmiştir.

```css
div {
    height: 100px;
    width: 100px;
    background-color: bisque;
}
@media (orientation: landscape) {
    div {
        background-color: brown;
    }
}
```

<hr>

## ❓ "id" ve "class" seçiciler arasındaki fark nedir?

- CSS "class" birden çok öğeye bir stil uygulamasıdır 👇

```html
<!DOCTYPE html>
<html>
  <style>
      .kutu{
          width: 300px;
          height: 300px;
          margin:10px;
          background-color: red;
      }
  </style>
  <body>
    <div class="kutu">Merhaba Dünya</div>
    <div class="kutu">Merhaba Dünya</div>
    <div class="kutu">Merhaba Dünya</div>

    <p class="kutu">Merhaba Dünya</p>
    <p class="kutu">Merhaba Dünya</p>
  </body>
</html>
```

- "id" ise, benzersiz bir öğeye bir stil uygular 👇

- ID ayrıca, bir öğeye doğrudan bağlanmak için özel bir URL kullanabilmeniz ve JavaScript tarafından kullanılması bakımından da özeldir.

```html
<!DOCTYPE html>
<html>
  <style>
      #slogan{
          color:red;
          font-style: italic;
      }
  </style>
  <body>
    <h1 id="slogan">Tasarım ve Kodlama</h1>

    <p>Merhaba Dünya</p>
    <p>İkinci Satır</p>
  </body>
</html>
```

<hr>