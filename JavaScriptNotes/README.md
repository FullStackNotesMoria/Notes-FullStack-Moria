# <center> JAVASCRIPT </center>

<center><img align="center"
  src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/2048px-Unofficial_JavaScript_logo_2.svg.png"  width="80px"></center>

<hr>

## ❓ JavaScript nedir?

- JavaScript, Netscape tarafından geliştirilmiş bir betik dilidir. 
- JavaScript Aralık 1995'te ortaya çıktı ve başlangıçta LiveScript olarak adlandırıldı, ancak adı kısa süre sonra pazarlama nedenleriyle değiştirildi.
- Aynı zamanda benzerlik gösteren ancak tamamen farklı bir dil olan 'Java' ile karıştırılmamalıdır.
- Hem istemci tarafı hem de sunucu tarafı öğeleriyle uyumlu çok hafif bir programlama dilidir.
- Nesne yönelimli bir programlama dilidir.
- Yorumlanmış bir programlama dilidir (talimatları doğrudan uygulayabilen bir program) ve kolayca HTML'ye gömülebilir.
- Birlikte, statik web sayfaları için dinamik olarak etkileşimli öğeler oluşturabilir.
- Daha iyi kullanılabilirlik sunar ve insanların web sayfalarıyla ilgili deneyimlerini yepyeni bir düzeye çıkarır.

<hr>

## ❓ JavaScript ve ECMA Script (ES) arasındaki fark nedir?

- ECMAScript, betik dilleri için bir standarttır.
- ECMA, Avrupa Bilgisayar Üreticileri Birliği anlamına gelir.
- JavaScript gibi diller ECMAScript standardını temel alır.
- ECMA Standardı, en bilinen JavaScript (Netscape) ve JScript (Microsoft) olmak üzere çeşitli kaynak teknolojilerine dayanmaktadır.

✨

- JavaScript, ECMAScript Standardının en popüler uygulamasıdır.
- Javascript’in temel özellikleri ECMAScript standardını temel alır fakat Javascript’in ECMA standardında olmayan başka ek özellikleri de bulunur.
- ActionScript ve JScript, ECMAScript’i uygulayan diğer dillerdir.
- Standartlaştırma için JavaScript ECMA’ya gönderildi ancak Javascript adındaki ticari marka sorunları nedeniyle standart ECMAScript olarak adlandırıldı.
- Her tarayıcının bir JavaScript tercümanı vardır.

<hr>

## ❓ var-let-const nedir? Aralarındaki Farklar Nelerdir ?

- var ile bir değişken oluşturduğumuzda (declaration) ve herhangi bir değer atamadığımızda (initialization), oluşturulan değişkenin değerine default olarak undefined atanır.
- Oluşturduğumuz bu değişkeni console.log ile çağırdığımızda undefined çıktısını alırız.
- 👇 Değer atamadan sadece değişken oluşturma işlemine "Variable Declaration" denilmektedir:

```javascript
var album; // variable declaration
console.log(album) // undefined
```

- 👇 Bir değişkene ilk değeri atama işlemine "Variable Initialization" denmektedir:

```javascript
var album = "Sari Cizmeli Mehmet Aga"; // variable declaration
console.log(album) // Sari Cizmeli Mehmet Aga
```

### ✨ Scope nedir?

- Scope, çalışma zamanı sırasında kodunuzun belirli bir bölümündeki değişkenlerin, fonksiyonların ve nesnelerin(objects) erişilebilirliğidir.
- Başka bir deyişle, Scope, kodunuzun belli kısımlarında değişkenlerin ve benzerlerinin görünürlüğüdür.

### 🚀 Global Scope:

👉 Global Scope özellikli değişkenler, fonksiyon içerisinden de erişilebilir durumdadırlar.

```javascript
/* Global Scope */
var sayHi = "Hello";

function greet(){
  console.log(sayHi);
}

greet(); // Hello
```

### 🚀 Function Scope:

👉 Eğer var ile tanımlanan bir değişken, bir fonksiyon içerisinde oluşturulmuş ise, sadece o ve nested dediğimiz fonksiyon içerisinde bulunan diğer fonksiyonlar içerisinde çağırılıp kullanılabilir.

```javascript
function getAlbumDate(){
  var albumDate = new Date();
  return albumDate
}

getAlbumDate(); // Tue Nov 29 2022 21:28:19 GMT+0300 (GMT+03:00)
console.log(albumDate); // Reference error albumDate is not defined
```

### 🚀 var & let & const:

👉 "var" function scope özelliği taşırken,

👉 "let" ve "const" block scope özelliği taşımaktadır.

👉 "Let" ve "const" block scope özellikli oldukları için herhangi bir şekilde scope dışında kullanılamazlar.

👉 Yani "let" ile oluşturulan bir değişken sadece oluşturulduğu yerdeki süslü parantezler içerisinde erişilebilirdir ve dışarısında kullanılamaz.

👉 Oluşturulan değişken önce kullanılıp daha sonra "var" keyword’ü ile tanımlanırsa herhangi bir hata oluşmaz(Hoisting). "let" ve "const" için bu durum geçerli değildir.

👉 "let" ve "const" ile oluşturduğunuz değişkenlere değer atadığımızda, "const" ile oluşturduğunuz değişken’e tekrar atama yapamayız, ancak "let" değişkenine yeni bir değer ataması yapabilirsiniz.

<hr>

## ❓ JS Data Types?

- Primitive
  + String
  + Boolean
  + Null
  + Undefined

- Non-Primitive (Object)
  + Array
  + Object
  + Function
  + Date
  + Regx

<hr>

## ❓ null ve undefined anahtar kelimeler arasında fark var mı?

<center><img align="center"
  src="https://talentgrid.io/wp-content/uploads/2021/05/0-null-undefined.png"  width="500px"></center>

- JavaScript bazı dillerden farklı olarak null ve undefined olarak iki ayrı durum kabul eder.

- JavaScript’te undefined, bir değişkenin bildirildiği ancak henüz bir değer atanmamış olduğu anlamına gelir.

- null ise bir atama değeridir, değişkene değersiz bir gösterim olarak atanabilir. typeof null bize nesne döndürür.

<hr>

## ❓ JS'de Hoisting'i açıklayınız.

<center><img align="center"
  src="https://d3n0h9tb65y8q.cloudfront.net/public_assets/assets/000/003/406/original/Hoisting.png?1654851517"  width="500px"></center>

- Hoisting, Javascript'te değişkenlerimizin başta tanımlanması işlemidir.
- Zaten kelime anlamı da kaldırmaktır.
- Hoisting olayının temel amacı aşağıda tanımladığınız değişkenlere yukardan veya herhangi bir yerden rahat bir şekilde ulaşmanızdır.

```javascript
x = 5;   // x'e 5 değerini atadık
console.log(x) // x değerini konsola yazdırdık
var x;  // x değişkenini tanımladık
```

```javascript
var x; // x değişken tanımlandı
x = 5; // 5 değeri atandı
console.log(x); //x değeri ekrana yazıldı
```

- Yukardaki örnek 1 ve örnek ikiyi detaylı incelediğimiz zaman görüyoruz ki değişkenin tanımlandığı yerin kullanmadan önce veya sonraki satırlar olmasının hiçbir önemi yok.
- Ancak kod bütünlüğü ve okunabilirlik açısından global değişkenleri kod bloğunun en tepesinde tanımlamak en doğru karar olacaktır.
- Diğer türlü uzun kodlarda karmaşıklığa sebebiyet verebiliriz.

### 🚩 Eğer önce değişkene değer verip sonra let veya const ile o değişkeni tanımlarsak Javascript "Reference Error" hatası verecektir. Yani ecmascript abimiz bu konuda biraz katı davranıyor 👇

```javascript
  isim = "Zafer";
  let isim;
  console.log(isim);
// kod çalıştığında  Reference error hatası verecektir.
```

<hr>

## ❓ JavaScript’de for-in döngüsü nedir?

- for-in döngüsü, özellikle adım adım olarak nesnenin tüm özellikleri döngü için tasarlamıştır.
- Her yinelemede nesneden bir özellik seçer ve üzerinde gerekli işlemleri gerçekleştirir.

### ✏ Syntax 👇

```javascript
for (key in object) {
  // code block to be executed
}
```

### 👇 Example:

```javascript
const person = {fname:"John", lname:"Doe", age:25};

let text = "";
for (let x in person) {
  text += person[x]; // John Doe 25
}
```

<hr>

## ❓ JS'deki 'this' anahtar kelimesi nedir?

- Javascript this kelimesi ait olduğu nesneyi ifade eder.

- Nerede kullanıldığına bağlı olarak farklı değerler alabilir;

- Bir metot içerisinde kullanıldığı zaman ait olduğu nesneyi temsil eder.

- Tek başına kullanıldığı zaman global bir nesneyi temsil eder.

- Bir fonksiyon içerisinde kullanılırsa global bir nesneyi ifade eder.

- Eğer katı modda bir fonksiyonun içerisinde kullanılırsa undefined yani tanımsız değerini döndürür.

- Bir olayda (tıklama, çift tıklama gibi) olayın gerçekleştiği elementi temsil eder.

### ✔ Metot İçinde this Kullanımı ✔

👉 Bir nesnenin metodunda "this" şu şekilde kullanılır. Nesne içinde tanımlanan özelliklere "this.ozellikAdi" şeklinde ulaşırız. 👇

```javascript
<script>
  isimsoyisim: function() {
    return this.ad+ " " + this.soyad;
  }﻿
</script>
```

### ✔ Global this Kullanımı ✔

👉 "this" anahtar kelimesi tek başına kullanıldığında global bir nesneyi temsil eder.

```javascript
<div id="deneme"></div>
<script>
  var x = this;
  document.getElementById("deneme").innerHTML = x;
  // Çıktı: [object Window]
</script>
```

👉 Katı modda da this nesnesi window nesnesini temsil eder.

```javascript
<script>
  "use strict";
  var x = this;
  console.log(x);
  //Çıktı : [object Window]
</script>
```

### ✔ Fonksiyon İçinde this Kullanımı ✔

👉 Fonksiyon içinde this kullanıldığı zaman varsayılan window nesnesini temsil edecektir.

```javascript
<p id="demo"></p>
<script>
  document.getElementById("demo").innerHTML = myFunction();
  function myFunction() {
      return this;
  }
  // Çıktı: [object Window]
</script>
```

### ✔ Olaylarda (Event) this Kullanımı ✔

👉 Olaylarda this anahtar kelimesi olayın kullanıldığı elementi temsil eder.

```javascript
<button onclick="this.style.display='none'">Tıkla ve buton yok olsun.</button>
```

<hr>

## ❓ Spread operatörü niçin kullanılır?

- JavaScript spread operatörü (...), mevcut bir dizinin veya nesnenin tamamını veya bir kısmını başka bir dizi veya nesneye hızlı bir şekilde kopyalamamızı sağlar.

```javascript
const numbersOne = [1, 2, 3];
const numbersTwo = [4, 5, 6];
const numbersCombined = [...numbersOne, ...numbersTwo];

console.log(numbersCombined);
```

Output 👇

```bash
[1, 2, 3, 4, 5, 6]
```

- Spread operatörü genellikle destructuring ile birlikte kullanılır:

    + Örnek: Sayılardan birinci ve ikinci öğeleri değişkenlere atayın ve gerisini bir diziye koyun 👇

    ```javascript
    const numbers = [1, 2, 3, 4, 5, 6];

    const [one, two, ...rest] = numbers;

    numbers.lenght() // 6

    numbers[2]  // 30
    ```

- Spread operatörünü object ile de kullanabiliriz:

```javascript
const myVehicle = {
  brand: 'Ford',
  model: 'Mustang',
  color: 'red'
}

const updateMyVehicle = {
  type: 'car',
  year: 2021,
  color: 'yellow'
}

const myUpdatedVehicle = {...myVehicle, ...updateMyVehicle}

//Check the result object in the console:
console.log(myUpdatedVehicle);
```

Output 👇

```bash
{brand: 'Ford', model: 'Mustang', color: 'yellow', type: 'car', year: 2021}
```

- String ifadelerde kullanımı:

```javascript
let name = "JavaScript";

let arrayOfStrings = [...name];

console.log(arrayOfStrings); // ["J", "a", "v", "a", "S", "c", "r", "i", "p", "t"]
```

- Fonksiyon çağrılarında Spread Operatör kullanımı:

```javascript
function sum(a,b,c){
    return a+b+c;
}

const nums = [1,2,3];

sum(...nums) // 6
```

<hr>

## ❓ Anonymous Function nedir?

- Anonymous Function, kendisiyle ilişkilendirilmiş herhangi bir adı olmayan bir fonksiyondur. 

- Normalde JavaScript'te bir fonksiyonu tanımlamak için fonksiyon adından önce "function" anahtar sözcüğünü kullanırız, ancak JavaScript'teki anonim fonksiyonlarda fonksiyon adı olmadan yalnızca "function" anahtar sözcüğünü kullanırız.

- Anonim bir fonksiyona ilk oluşturulduktan sonra erişilemez, yalnızca bir fonksiyon olarak değer olarak saklandığı bir değişken tarafından erişilebilir. 

- Anonim bir fonksiyonun birden çok argümanı olabilir, ancak yalnızca bir ifadesi olabilir.

### ✏ Syntax 👇

```javascript
function() {
    // Function Body
 }
```

- Ayrıca aşağıda gösterilen "arrow function" tekniğini kullanarak da Anonymous Function bildirebiliriz:

```javascript
( () => {
    // Function Body...
} )();
```

### ✔ Örnek:

- Bu örnekte, konsola bir mesaj yazdıran isimsiz bir fonksiyon tanımlıyoruz. Fonksiyon daha sonra greet değişkeninde saklanır. Greet()'i çağırarak fonksiyonu çağırabiliriz. 👇

```javascript
<script>
  var greet = function () {
      console.log("Welcome to GeeksforGeeks!");
  };

  greet();
</script>
```

- Output 👇

```bash
Welcome to GeeksforGeeks!
```

<hr>

## ❓ JavaScript'te "Anonymous ve Named Function" arasındaki fark nedir?

- JavaScript'te anonim fonksiyonlar (function expression), kendilerine atıfta bulunacak bir ad veya tanımlayıcı olmadan üretilen fonksiyonlardır; şu şekilde tanımlanırlar 👇

```javascript
function(){
  // Function Body
  }
```

- Kendilerine atıfta bulunacak bir ada veya tanımlayıcıya sahip normal fonksiyonlar (function declaration), adlandırılmış fonksiyonlar olarak adlandırılır ve şu şekilde tanımlanır 👇

```javascript
function displayMessage(){
  // function..body
  }
```
| Anonymous Functions                                                                     | Named Functions |
| :---:                                                                                   |    :----:   |
| Anonim fonksiyonlar asla kaldırılmaz (hoisted) (derleme sırasında belleğe yüklenir).    | Adlandırılmış işlevler kaldırılır (derleme sırasında belleğe yüklenir).       |
| Anonim bir fonksiyonu çağırırken, onu yalnızca bildirim satırından sonra çağırabilirsiniz.  | Bildirimden önce bir name function çağrılabilir.        |
| ES6'dan önce, anonim fonksiyonların ad özellikleri boş dizeye ayarlanmıştı.  | ES6'dan önce, adlandırılmış fonksiyonların ad özellikleri, fonksiyon adlarına ayarlandı.       |
| Anonim fonksiyonlar, IIFE'ler (Instantly Invoked Function Expressions) (Anında Çağrılan İşlev İfadeleri) geliştirirken çok kullanışlı olabilir.  | Adlandırılmış fonksiyonların yeniden kullanımı daha kolaydır, bu da temiz kodun (clean code) oluşturulmasına yardımcı olur.       |
| Daha kolay programlama için anonim fonksiyonlar bağlam kapsamına (context scoping) izin verir. Fonksiyonlar veri olarak kullanıldığında arrow function kullanılmalıdır.  | Fonksiyon adı hata günlüğünde (error log) göründüğünden, named functions hata ayıklama ve hangi işlevin bir hata ürettiğini belirlemede oldukça kullanışlıdır.       |

<hr>

## ❓ Async - Await mantığı ve asenkron programlamayı açıklar mısınız?

<center><img align="center"
  src="https://csharpcorner-mindcrackerinc.netdna-ssl.com/article/thread-behaviour-in-synchronous-and-asynchronous-method/Images/image-20211224112443-6.png"  width="500px"></center>

- Javascript, bir <b>single-threaded</b> programlama dilidir. (Birim zamanda -1- tane iş parçacığı çalıştırıyor)

- Bilgisayarda <b>o anda çalışan programlar</b> "process" olarak adlandırılıyor. "Thread" ise iplik anlamına geliyor, yani process içinde alt parçacıklar.

- Kolumuz bir "process" ise parmaklarımız "thread" (iş parçacığı)'dir.

- CPU (Central Process Unit), birden fazla iş yaparken aslında zamanı küçük dilimlere böldüğünde milisaniye seviyesinde. Belli bir zaman aralığında birden fazla iş yapıyormuş gibi geliyor.

- Ancak Java, C++, Python'da multi-threaded aktif hale getirilebiliyor. (browser'lar, web API'ler sayesinde arka tarafta asenkron kodların çalışmasını sağlıyor)


    + <b>Asenkron programlama nedir?</b>

        - Asenkron programlama, bir uygulamada ana akışta meydana gelebilecek gecikmelerde akışın bloklanmamasını ve devam etmesini sağlayan programlama türüdür.

        - Bu yüzden bloklanmayan kod diyoruz.

        - Senkron(sıralı) programlamada bir işlem sonuçlanmadan diğer bir işleme başlanamaz.

        - Asenkron programlamada ise  bir işlem sonuçlanmadan diğer bir işlem başlayabilir. Bu bizi özellikle yüksek bekleme sürelerinin olduğu API işlemlerinde, programımızın bloke olmasından kurtarır.

    + <b>Senkron ve Asenkron arasındaki fark</b>

        - <b>Senkron(synchronous)</b> yani eşzamanlı programlama, işlemleri sırayla yaptırdığımız programlama türüdür.

        - Bir işlem bitmeden diğerine geçilmez veya sırada olan işlem atlanmaz.

        - <b>Asenkron(asynchronous)</b> yani eşzamansız programlama ise birden çok işlemin aynı anda yürütülmesi prensibiyle çalışır.

        - İşlemler herhangi bir sıraya alınmadan, diğer işlemlerden bağımsız şekilde yürütülür.

- <b>ÇÖZÜMLER:</b>

    + 1- [XMLHttpRequest](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) (Eski yöntem, Ornek: AJAX),
    
    + 2- [Promise](https://www.w3schools.com/js/js_promise.asp),

        - Bir Promise asagidaki state(durumlari) icerebilir:

            - <b>pending:</b> ilk state, fulfilled veya rejected olmayan
            
            - <b>fulfilled:</b> islem basariyla tamamlandigini gosteren state.

            - <b>rejected:</b> islemin basarisizlikla tamamlandigini gosteren state

    ```javascript
    const myPromise = new Promise((resolve, reject) => {
    let success = Math.floor(Math.random() * 5);
    const data = { a: 1, b: 2 };
    if (success) {
        resolve(data);
        console.log(`Task performed successfully`);
    } else {
        reject(new Error(`Task Failed`));
    }
    });

    myPromise.then((res) => console.log(res)).catch((err) => console.log(err));
    ```
    + 3- [Fetch API](https://www.w3schools.com/jsref/api_fetch.asp) (Promise'in basitlestirilmis hali),

    ```javascript
    fetch("https://api.github.com/users")
  .then((res) => {
    //? arrow function'da süslü kullanmazsak "return"e gerek yok.
    //! error handling 👇
    if (!res.ok) {
      //? hatayı algılamak için gelen cevabı yakalıyoruz 👇
      throw new Error(`Something went wrong: ${res.status}`);
    }
    return res.json();
  })
  .then((data) => updateDom(data))
  .catch((err) => console.log(err));
    ```

    + 4- [ASYNC-AWAIT](https://www.w3schools.com/js/js_async.asp) (Fetch API'nin makyajlammis hali)

        - Async-Await ECMAScript 2017 ile Javascript diline eklenmistir.

        - Aslinda Promise yapisinin syntax olarak basitlestirilmis halidir.

        - Bu baglamda sentetik seker <b>(Synthetic sugar)</b> benzetmesi yapilabilir.

        ```javascript
        let fault = false;

        const getUsers = async () => {
        //? try-catch blogu: Özellikle dış kaynaklı verilere erişirken o verilere erişememe, okunamama, bulamama ihtimali yüksek olduğundan; hata döndürdüğünde kullanıcıya hata olarak giderek programın kitlenmesini önlemek için hata getirebilecek yerleri tespit ederek bir hata ortaya çıkması durumunda o hatayı yönetmemizi sağlıyor. Try'ın içinde yazılan kodlarda hata olursa programı kitlemeden catch'in içinde yazılacak kod ile bu durumu kullanıcıya bildirir.
        try {
            const res = await fetch("https://api.github.com/users"); //! 1. çalışacak..
            if (!res.ok) {
            fault = true;
            //!   throw Error kısmını burada kullanmadık çünkü throw kullanınca kod bloğu aşağıya geçmiyor.
            }
            const data = await res.json(); //! 2. çalışacak
            updateDom(data); //! 3. çalışacak
        } catch (error) {
            console.log(error);
        } finally {
            fault = false;
        }
        };

        getUsers();

        const updateDom = (data) => {
        const userDiv = document.querySelector(".users");

        if (fault) {
            userDiv.innerHTML = `<h1 class= "text-danger">Data can not be fetched</h1> <img src="./img/404.png" alt=""/>`;
        } else {
            data.forEach((user) => {
            //? destructuring --> içindekileri ayırma:
            const { login, avatar_url, html_url } = user;
            userDiv.innerHTML += `<h2 class="display-1 text-warning">NAME: ${login}</h2>
                <img src=${avatar_url} alt="" width=50% /><p class=" text-primary display-6">HTML URL: ${html_url}</p>`;
            });
        }
        };
        ```

<hr>

## ❓ Zamanlayıcılar JavaScript’te nasıl çalışır?

- Zamanlayıcılar, belirli bir zamanda bir kod parçasını çalıştırmak veya kodu belirli bir aralıkta tekrarlamak için kullanılır.
- Bu, setTimeout, setInterval ve clearInterval işlevleri kullanılarak yapılır.
- ✔ SetTimeout (fonksiyon, gecikme) işlevi yukarıda bahsedilen bir gecikmeden sonra, belirli bir fonksiyonu çağıran bir zamanlayıcı başlatmak için kullanılır.
- ✔ SetInterval (fonksiyon, gecikme) yapılması ne zaman fonksiyon defalarca belirtilen gecikme sadece duraklamalara verilen işlevini yürütür.
- ✔ ClearInterval (id) işlevi durağına zamanlayıcı talimatını verir.

- Zamanlayıcılar tek bir iş parçacığı içinde çalıştırılır ve bu nedenle olaylar kuyruğa girerek yürütülmeyi bekler.

<hr>

## ❓ JavaScript’teki pop() yöntemi nedir?

<center><img align="center"
  src="https://global.discourse-cdn.com/freecodecamp/original/3X/b/0/b00a422dc8e2aecb652465b994082eed84b94bc5.png"  width="475px"></center>

- pop() metodu dizinin son elemanını siler ve dizinin yapısını değiştirir.
- Aynı zamanda da diziden silinen elemanı döndürür.
- pop() yöntemi, shift() yöntemine benzer.
- Aralarındaki fark, shift yönteminin dizinin başlangıcında çalışmasıdır.
- pop() metodu, verilen dizideki son öğeyi alır ve onu döndürür. Daha sonra çağrıldığı dizi değiştirilir.

<hr>

## ❓ == ile === farkı nedir?

<hr>

<center><img align="center"
  src="https://miro.medium.com/max/897/1*9f4jjunUcLqYJd02WI2LQA.png"  width="475px"></center>

- İki eşittir (==) ve üç eşittir (===) arasındaki en temel fark tip ve değer karşılaştırmasıdır.

- === kullandığınızda iki değerin hem tipini hem de değerini karşılaştırırken,

```javascript
var num = 0;
var obj = new String('0');
var str = '0';

console.log(num === num); // true
console.log(obj === obj); // true
console.log(str === str); // true
console.log(num === obj); // false
console.log(num === str); // false
console.log(obj === str); // false
console.log(null === undefined); // false
console.log(obj === null); // false
console.log(obj === undefined); // false
```

- == ise değerlerin tiplerini eşitleyerek sadece değer karşılaştırması yapar.

```javascript
var num = 0;
var obj = new String('0');
var str = '0';

console.log(num == num); // true
console.log(obj == obj); // true
console.log(str == str); // true

console.log(num == obj); // true
console.log(num == str); // true
console.log(obj == str); // true
console.log(null == undefined); // true

// both false, except in rare cases
console.log(obj == null);
console.log(obj == undefined);
```

<hr>

## ❓ Bir toplama fonsiyonu yap...

```javascript
<script>
  function Topla(sayi1, sayi2) {
    return sayi1 + sayi2;         // sayi1 ve sayi2 toplamını döndürür
  }
  alert(Topla(10, 5));
</script>
```

<hr>

## ❓ JavaScript’te innerHTML kullanmanın dezavantajları nelerdir?

- innetHTML, body kısmında yer alan bir HTML etiketinin içeriğini değiştirmemizi sağlar.
- innerHTML özelliği ile sayfanın istenen yerine HTML kodları ekleyebilriz.
- JavaScript ile sayfaya HTML kodları eklerken, tırnak işaretlerini karıştırırsak sorun yaşarız.
- Bu nedenle çift tırnak içerisinde tekrar tırnak işareti kullanmamız gerekirse, içteki tırnak işaretlerini tek tırnak olarak yazmalıyız.

👉 JavaScript’t  innerHTML kullanmanın dezavantajları:

- İçerik her yerde değiştirilir durumda olur.
- += “İnnerHTML = innerHTML + ‘html'” gibi kullansanız bile, yine de eski içerik html ile değiştirilir
- Tüm innerHTML içeriği yeniden ayrıştırılır ve öğeler halinde oluşturulur, bundan dolayı daha yavaştır.
- İnnerHTML doğrulama sağlamaz ve bu nedenle muhtemelen belgeye geçerli ve bozuk HTML ekleyebilir ve onu kırabiliriz.

<hr>

## ❓ JavaScript’te ‘use strict’ nedir ve nasıl etkinleştirilebilir?

- JavaScript use strict anahtar kelimesi kullanım amacı kodun katı kurallı olarak çalıştırılacağını belirtir.
- Katı kurallı kullanımda değişken oluşturulmadan kullanmaya izin verilmez.
- JavaScript kodlarının katı kurallı olarak yorumlanması için kod veya fonksiyon başına “use strict”; yazmak yeterli olacaktır.
- Katı kural tanımı kod başına yazılırsa tüm kodlar katı kurallı olarak çalışacaktır.

```javascript
"use strict";
x = 3.14;       // This will cause an error because x is not declared
```

```javascript
x = 3.14;       // This will not cause an error.
myFunction();

function myFunction() {
  "use strict";
  y = 3.14;   // This will cause an error
}
```

<hr>