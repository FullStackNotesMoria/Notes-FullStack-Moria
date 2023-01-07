# <center> HTML </center>

<center><img align="center"
  src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQpngGRjYX1ca7qAADU3K6eGLj7ShQE3L2otdzfryl_Y9Ht2QRoQKYQbsXd36XIxMbYOw0&usqp=CAU"  width="90px"></center>

<hr>

## ❓ HTML Nedir?

- Kısaca HTML internetin dilidir.
- <b>"Hypertext Markup Language"</b> ifadesinin kısaltmasıdır.
- Web site, web uygulama ve benzeri şeylerin oluşturulmasında kullanılan bir dildir.

<hr>

## ❓ Tag nedir?

- Tag'ler arasına içeriğin yerleştirildiği sembollerdir.
- Sitenin erişime açıldığında uygun bir şekilde sunulması için içeriği şekillendirmek ve düzenlemek için kullanılır.

<hr>

## ❓ "Physical tag" ve "logical tag" arasındaki fark nedir?

- Physical tag'lerin arasında yerleştirilen içerikler biçimlendirilir ve stil eklenerek bu tag'lere göre (parametrelere göre) görüntülenir.
- Logical tag'ler çevreledikleri metnin  önemini ve anlamını belirler.

👇 Örneğin:

```html
<p style="color: blue";><it>Bunlar görünümü tanımlayan physical tag'lerdir.</it></p>
<em>Bunlar vurgulanmış bir paragrafı tanımlayan These are logical tag'lerdir.</em>
```

<hr>

## ❓ "Attribute" nedir?

- Attribute bir tag'in sahip olduğu EK bir özelliktir.
- Bu özelliklik sitenin yayınlanmış sürümünde tag'in ne fonksiyona sahip olacağını belirler.
- Attribute'lar tag'in adının görüntülendiği aynı alanda atanır.

👇 Örnek: Resme genişlik ekleme:

```html
<img src="https://cdn.bitdegree.org/learn/pom-laptop.png?raw=true" width="100">
```

<hr>

## ❓ HTML5 ile gelen semantik tag'lerden bazılarını sayınız.

- HTML5, HTML'nin en yeni ve güncel sürümü.
- HTML'nin yeni sürümüyle pek çok farklı semantik tag tanıtıldı.
- 👉 header, footer, main, article.

<hr>

## ❓ "Block" ve "inline" elementlerin arasındaki fark nedir?

- Block elementler olabildiğince yer kaplayacak şekilde programlanır.
- Inline elementler ise minimum miktarda yer kaplayacak şekilde tasarlanır.

<hr>

## ❓ "Image map" ne için kullanılır?

- Image map birçok farklı bağlantıyı tek bir görsele bağlamanızı sağlayan bir araçtır.
- Muhteşem olmasının sebebi şahane banner'lar ve site kapak görselleri oluşturmanızı sağlarken istediğiniz şeyi bağlantılama imkanı da sunar.

```html
<map name="creaturemap">
  <areashape="rect"coords="34, 44, 270, 350"alt="Doggo"href="https://www.bitdegree.org">
  <areashape="rect"coords="290, 172, 333, 250"alt="Gaming"href="http://www.bitdegree.org">
  <areashape="circle"coords="337, 300, 44"alt="Level up"href="http://www.bitdegree.org">
</map>
```

<hr>

## ❓ "Anchor" tag'leri nedir?

- Anchor tag'leri hyperlink oluşturmak için kullanılır.
- Bu bağlantılar var olan bir içeriğin (metnin) üzerinde oluşturulur.
- Toplamda üç anchor tag bulunur; 
  + active,
  + visited
  + unvisited.

<hr>

## ❓ Tüm tarayıcılar HTML5'i destekliyor mu?

- Evet ve hayır.
- "Tüm" ifadesinin ne anlama geldiğine bağlı.
- Mevcut tarayıcıların çoğu sorunsuz bir şekilde HTML5'i destekliyor.
- Ancak bu tarayıcıların eski sürümleri için aynı şey geçerli olmayabilir.

<hr>

## ❓ "Semantik element'ler" nedir?

- Basit elementler (tag'ler) bir sayfanın nasıl görünmesi gerektiğiniz tanımlamayı hedeflerken semantik elementler web sayfasına anlam katar.
- Semantik elementlere örnek:
  + form
  + table
  + article.
- Gördüğünüz üzere ne türde içerik olacağını açık bir şekilde belirtiyor.

<hr>

## ❓ HTML5'te veri nasıl saklanır?

- HTML5'te veri saklamanın iki yolu var;
  + local storage
  + session storage.

- Local storage'da saklanan veriler güvenlidir ve geliştirici tarayıcıdan çıkmaya karar verdikten sonra silinmez.
- Session storage'da tarayıcıdan çıktığınız anda veri otomatik olarak silinir.

<hr>

## ❓ Sitenize JavaScript nasıl eklenir?

- inline, script block ekleyerek 👇

```html
<script>
function smile(sw) {
    if (sw == 0) {
        document.getElementById("learn").innerHTML = "SAD!";
    } else {
        document.getElementById("learn").innerHTML = "HAPPY!";
    }
}
</script>
```

- Bir JavaScript dosyasına bağlayarak (src) 👇

```html
<script src="scripts-tag-example.js"></script>
```

<hr>

## ❓ "Application cache" nedir?

- Application cache, projenizi (sitenizi) offline modda çalıştırmanıza olanak sunan bir fonksiyondur.
- Cache mekanizması ile site kullanıcılarının offline olduğu durumlarda da sitenin belirli içeriğine erişmesini sağlamış oluyoruz.
- Kaynaklarınızı çok daha hızlı yüklediğinden test için muhteşemdir.

<hr>

## ❓ "Marquee" nedir?

- Marquee (kayan yazı), sitenize aşağı doğru kaydırılabilen bir yazı eklemenize olanak sunan bir fonksiyondur.
- Bunu "marquee" tag'leri ekleyerek gerçekleştirebilirsiniz.

```html
<marquee width="60%" direction="up" height="100px">
This is a sample scrolling text that has scrolls in the upper direction.
</marquee>
```

<hr>

## ❓ WebSQL nedir?

- WebSQL, sitenizi ziyaret eden/sitenize kaydolan kişiler hakkında belli bilgilere sahip bir veri tabanıdır.
- Veri tabanında arama tercihleri, belli eylemler ve benzeri şeyler saklanır.
- Önemli bir nokta WebSQL'nin herhangi bir şifre, kredi kartı bilgisi vb. şeyleri saklamamasıdır ‼

<hr>

## ❓ "Entity" nedir?

- Bu ve buna benzer HTML mülakat soruları gelirse işvereniniz muhtemelen HTML'nin desteklemediği özel karakterlerden bahsediyordur.
- Entity'ler yer tutuculardır.
- Dosyada başka bir karakterin olması gerektiği belli bir yeri doldururlar.
- Web tarayıcı bu karakteri desteklemediğinden yer tutucu kullanmanız gerekir.

<hr>

## ❓ "Cite" tag nedir?

- "cite" tag'i metnin başka bir yerden alınmış kısmını belirtmek için kullanılır.
- Atıfta bulunulan metni gösteren bir inline tag'idir.

```html
<cite>Sophie's Choice</cite> by William Styron
```

<hr>

## ❓ Bir metin alanı için varsayılan boyut ne?

👉 Değiştirilmemiş bir metin alanında bulunabilecek maksimum karakter miktarı <b>13</b>'tür.

<hr>


## ❓ Font Awesome Nedir? Nasıl Kullanılır?

- Font awesome web sayfası tasarlarken sıklıkla kullanılan ikonları font olarak sunan CSS kütüphanesidir.

- Peki ne gerek var kullanmaya derseniz. Daha önceleri her bir ikonu çeşitli resim editörleri ile tasarlıyorduk. Kullandığımız ikonlar genellikle standart görünümde ve benzerdi.

- Oluşturduğumuz ikonların sayısı fazla olduğundan dolayı her ikon için sunucuya tekrar istek gidiyordu.

- Sunucuya tekrar istek gönderilmesi [CSS sprite tekniği](https://www.yusufsezer.com.tr/css-sprite-teknigi/) ile çözüldü.

- Resim editörleri ile oluşturmuş olduğumuz ikonları hazırlamak zahmetli ve sürekli benzer işlemlerle uğraşıyorduk.

- Ayrıca CSS sprite tekniği uygulasak bile ikonların genişlik ve yüksekliklerini değiştirdiğimizde bozulmalar meydana geliyordu.

- İkonun rengini değiştirmek zaman alıyordu. İşte bu sorunlara çözüm olarak font awesome geliştirildi.

<hr>


### 🚩 Font awesome kurulumu 👇

- Font awesome kurulumu için font awesome dosyalarını https://fontawesome.com sitesinden indirin.

- İndirmiş olduğunuz dosya içerisindeki css ve fonts klasörünü çalışma klasörünüze çıkartın.

- CSS klasörü içerisinde font-awesome.css ve font-awesome.min.css dosyaları çıkmaktadır.

- font-awesome.min.css dosyası .min ekinden anlaşılacağı üzere minimize edilmiş yani sıkıştırılmış dosyadır ikisini de kullanabilirsiniz.

- Çalıştığınız HTML dosyasının <head> </head> etiketleri arasına CSS dosyasını dahil edin 👇

```html
<link rel="stylesheet" href="css/font-awesome.css" />
```

- Böylece font awesome kurulumu tamamlanmış oldu.

<hr>


### 🚩 Font awesome nasıl kullanılır?

- Font awesome ikonlarını kullanabilmek için kesinlikle "fa" sınıfını kullanmamız gerekiyor. Eklenmediğinde font awesome düzgün çalışmayacaktır.

```html
<i class="fa fa-user-plus"></i>
<i class="fa fa-try"></i>
```

- İkonların boyutlarını büyütmek için fa-lg, fa-2x, fa-3x, fa-4x, fa-5x eklememiz yeterli olacaktır 👇

```html
<i class="fa fa-user-plus fa-3x"></i>
```

- Font awesome ikonlarını döndürmek için 👇

  - fa-rotate-90
  - fa-rotate-180
  - fa-rotate-270
  - fa-flip-horizontal
  - fa-flip-vertical

```html
<i class="fa fa-user-plus fa-3x fa-rotate-90"></i>
```

- İkona kenarlık vermek için "fa-border" sınıfını eklememiz yeterli olacaktır 👇

```html
<i class="fa fa-try fa-border fa-3x"></i>
```

- İkonlara döndürme animasyonu eklemek için "fa-spin" veya "fa-pulse" sınıflarından birini eklememiz yeterli olacaktır 👇

```html
<i class="fa fa-try fa-spin fa-3x"></i>
```

- ✔ Animasyonlar daha çok sitenin yüklenme aşamasını gösteren ikonlarda kullanılır 👇

```html
<i class="fa fa-spinner fa-pulse fa-5x"></i>
<i class="fa fa-refresh fa-spin fa-5x"></i>
```

<hr>