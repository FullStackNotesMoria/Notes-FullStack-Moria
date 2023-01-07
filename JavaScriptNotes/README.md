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

# JS 01-INTRO 

```javascript
console.log("Bu index.js dosyasidir");
console.log("***** Data Types *****");

//*  CONST ve LET, ECMASCRIPT6 ile gelmiştir. VAR eski versiyonlardan beri bulunmaktadır.

//? ===================  CONST  ======================

const fs = "Cohort 13";
console.log(fs);

const sayi = 20;
console.log(sayi);
console.log(typeof sayi);

//* Tirnak icindekiler string (text) olarak atanir.
const sayi1 = "33";
console.log(sayi1);
console.log(typeof sayi1);

// sayi1 = 55; //!Assignment to constant variable.

// const pi; //! Missing initializer in const
// pi = 3.14

const s1 = "hello ";
const s2 = "FS13";
console.log(s1 + s2); //? String Concationation
// JS default olarak + operatorunde eger degiskenlerden en az birisi string ise bunlari birine ekler. (Toplama yapmaz)

const n1 = "5";
const n2 = 10;
console.log(n1 + n2); //? String Concationation

//! Ayni alan (scope) icerisinde ayni isimle yeniden degisken tanimlanamaz.
// const n1 = 5;

// n2 = n2 + 1; //! error

//? ======================  LET  ========================
//* LET de CONST gibi yaygın kullanılan değişken tanımlama yöntemidir.
//* CONST'dan farkı, sadece tanımlama kısmında değil istenildiği zaman değeri değiştirilebilir.
//* CONST gibi tanımlandığı blok içerisinde geçerlidir. Başka yerlerden erişilemez. (Block-Scoped)
//* CONST kullanamadığımız durumlarda (değişkenin değeri sürekli değişecekse) LET kullanmalıyız.

let dil = "javascript";
console.log(dil);

dil = "java";
console.log(dil);

dil = true;
console.log(dil, typeof dil);

dil = 3.14;
console.log(dil, typeof dil);

let cohort;
console.log(cohort); //* undefined (tanimsiz, type'ı yok)

cohort = 3;
console.log(typeof cohort); //? number

// let cohort = "FS13"; //!SyntaxError: Identifier 'cohort' has already been declared (at app.js:60:5)
//! Ayni alan (scope) icerisinde ayni isimle yeniden degisken tanimlanamaz.

let num1 = 5;
let num2 = 3;
let result = num1 + num2; //?8
console.log(++result); //?9
console.log(result);

//! JS ilk kez gormus oldugu count'u bir degisken olarak tanimladi
count = 55; //! var olarak tanimladi.
console.log(count);
count = 22;
console.log(count, typeof count);

//? ===================  VAR ===========================
//* VAR ile bir değişken tanımlandığında LET de olduğu gibi değeri sonradan değiştirilebilir.
//* VAR değişkenleri global degiskenler gibidir.
//* LET ve CONST ile tanimlanan degiskenler block-scope 'dur
//* Yani sadece tanimlandigi block (alan) icerisinde gecerlidir.

var x = 11;
console.log(x);

//? Cesitli blok (scope) ornekleri
// if(){
//   let  x= 5

// }else{
//  x
// }
// x

// for(){
//    const y=4

// }
// console.log(y)

//? Bir block oluşturduk. Blok denilince if-else,
//? switch-case, fonksiyon vb. yapilarin ic alani dusunulebilir.
{
  //! Burasi local bir alandir.
  let a = 2;
  const b = 3;
  console.log(a, b);
}
//! a ve b bu alanda tanimli degildir.
// console.log(a, b); //! error

{
  //! Burasi local bir alandir.
  var c = 99; //?var ile tanimlanan bir degisken hep global olur.
  console.log(c);
}
console.log(c);

//? Her hangi bir bloğun dışı global alandir
var varNumber = 1; //* Global degiskenler
let letNumber = 2;

{
  varNumber = 11; //* Global degiskenlere veri yaziyoruz
  letNumber = 22;
}
//* Global degiskenleri okuyoruz.
console.log(varNumber, letNumber);

console.log("**********************");

//*Global degiskenler
var varNumber1 = 3;
let letNumber1 = 4;
{
  var varNumber1 = 33;
  let letNumber1 = 44; //! yeni bir local degisken olsuturduk
  console.log(letNumber1); //! local degiskeni okuduk
}

//* Global degiskenleri okuyoruz
console.log(varNumber1, letNumber1);
```


# JS 02-DATATYPE-OPERATORS

```javascript
// // * =======================================================
// // *                 ARITMETIK OPERATORLER
// // * =======================================================

// console.log(" **** Operators ****")

// const cola = 20
// const gumm = 5
// const biscuits = 15

// const totalPrice = cola + gumm + biscuits

// // totalPrice++ //? Hata

// console.log("TOTAL PRICE:", totalPrice)

// //? + operatoru String Concatination islemi de yapar.
// console.log("TOTAL PRICE:" + totalPrice) //? String Concatination

// const comments = totalPrice + " TL"
// console.log(comments)

// const commets = 50 + 40 + " TL"
// console.log(commets)

// const firstName = "Ahmet"
// const lastName = "Can"
// console.log(firstName + " " + lastName)

// const s1 = 5,
//   s2 = "4",
//   s3 = "three"

// console.log(s1 + s2) //? 54
// console.log(s1 - s2) //? 1
// console.log(s1 - s3) //? NaN (Not A Number)
// //! String ifadeyi number a cevirmeye calisti fakat mumkun olmadigi icin NaN dondurdu.

// const difference = s1 - s3
// console.log(difference, typeof NaN) //? NaN'in data type'ı number'dir.

// //* Bir islemin sonucunun NaN olup olmadigini anlamak icin isNaN() fonksiyonu kullanilabilir.
// console.log(isNaN(difference)) //?true

// //? Ornek
// //?-----------------------
// const yearOfBirth = 1920
// const name = "John"
// console.log(name + " is " + (2022 - yearOfBirth) + " years old")

// //* Sistem tarih ve saat bilgileri icin Date() kullanilabilir.
// // const date = new Date()
// // console.log(date)

// console.log(
//   name + " is " + (new Date().getFullYear() - yearOfBirth) + " years old"
// )

// //! ========== Template Literals ============

// //? 3 sekilde de string tanimlanabilir.

// const message1 = "Merhaba Javascript"
// const message2 = "Merhaba Javascript"
// const message3 = `Merhaba Javascript` //? Template literals

// console.log(`${name} is ${2022 - yearOfBirth}
// years old`)

// //* CAPRMA VE US ALMA (Multiply, Pow)
// //*--------------------------------------

// //? Ornek
// //?-------------------------------------
// //? Kullanicidan veri girisi istedik.
// // ? prompt ile kullancidan alinan veri default olarak string'dir
// //? Bu veriyi number'a Number() fonksyinu ile cevirebilriz.
// // const r = +prompt("Please enter r:")
// const r = Number(prompt("Please enter r:"))
// const pi = 3.14
// // const square = pi * r * r //? carpma
// const square = pi * r ** 2 //? us alma
// console.log(`Square of Circle: ${square} `)
// console.log(`Square of Circle: ${square.toFixed(3)} `)

// console.log(`Square of Circle: ${Math.floor(square)} `)
// console.log(`Square of Circle: ${Math.ceil(square)} `)
// console.log(`Square of Circle: ${Math.trunc(square)} `)
// console.log(`Square of Circle: ${Math.round(square)} `)

// //?Bazi fonksiyonlar
// // Math.floor();  //* her zaman en yakin alt tamsayiya yuvarlar
// // Math.ceil();  //* her zaman en yakin ust tam tamsayiya yuvarlar
// // Math.trunc(); //* sayinin tam kismini alir.
// // Math.round(); //* en yakin tam sayiya yuvarlar.
// // Math.random(); //* 0 ve 1 arasında rasgele sayi uretir.

// const randomNumber = Math.random() //? 0 - 1 arasinda rasgele sayi
// console.log(randomNumber)

// //? 0-100 arasinda sayi uretmek istenirse
// const rasgele = Math.round(Math.random() * 100) //?
// console.log(rasgele)

// //* ARTTIRMA VE AZALTMA (Inc, Dec)
// //*--------------------------------------

// //? Ornek : 1 eksiltme, 1 arttirma
// let a = 5
// a++
// console.log(a++) //? 6
// y = a + 5 //? 7 + 5
// console.log(--y) //? 11

// //? Ornek : 5 arttirma
// let z = 4
// z = z + 5
// z += 10 //? z = z + 10

// //? Ornek : 10 eksiltme
// let k = 20
// k -= 10 //? k = k - 10
// console.log("k:", --k) //? k:9
// console.log({ k }) //? {k:9}

// //? Ornek : 3 katini alma
// let b = 4
// b = b * 3
// b *= 3 //? b = b *3
// console.log({ b })

// //* MOD
// //*--------------------------------------
// const number = prompt("Please enter a 3-digits number:")

// const ones = number % 10
// const tens = Math.floor(number / 10) % 10
// const hundreds = Math.trunc(number / 100)
// console.log(`Hundreds: ${hundreds}, Tens: ${tens}, Ones: ${ones} `)

// // * ================================================
// // *          KARSILASTIRMA OPERATORLERI
// // * ================================================

// const num1 = 3

// console.log(num1 == 3) //? true
// console.log(num1 === 3) //? true
// console.log(num1 === "3") //? False

// const num2 = "3"

// console.log(num1 == num2)
// console.log(num1 != num2) //? false

// const num3 = 5
// const num4 = "1"

// console.log(num1 > num3) //?false  (3>5)
// console.log(num1 <= num3) //? true  (3 <= 5)

// console.log(num2 > num4) //? "3" > "1" ASCII'ye gore kiyaslama yapilir

// * ================================================
// *            MANTIKSAL OPERATORLER
// * ================================================

const v1 = true
const v2 = false

// console.log(v1 && v2) //? false
// console.log(v1 || v2) //? true

// console.log(!v1) //?false

// //? Ornek:
// const age = prompt("Please enter your age:")
// const healty = confirm("are you healty?")
// console.log(age, healty)

// if (age >= 18 && healty == true) {
//   console.log("Ehliyet alabilir")
// } else {
//   console.log("ehliyet alamaz")
// }

//? Javascripte surekli falsy olan 6 deger bulunmaktadir.
const nal = null
const tanimsiz = undefined
const bos = ""
const sayiDegil = NaN
const sifir = 0
const falsy = false

console.log(Boolean(0)) //? false
console.log(Boolean(5)) //? true
console.log(Boolean(-5)) //? true
console.log(Boolean(12.4)) //? true

console.log(v1 && null && true && true) //? null
console.log(v1 && 4 && true && 5) //? 5
console.log(0 && v1) //? 0
console.log(v1 || 0) //? true

const num5 = 0 //? falsy

if (num5 === true) {
  console.log("sayi sifir degildir")
} else {
  console.log("sayi sifirdir")
}

// * =============================================
// *            TIP DONUSUMLERI
// * =============================================

const dolar = "1000"
const tl = "500"

const totalMoney = Number(dolar) + Number(tl)
const totalMoney1 = +dolar + +tl
const totalMoney2 = parseInt(dolar) + parseInt(tl)
const totalMoney3 = parseFloat(dolar) + parseFloat(tl)
console.log(totalMoney3)

console.log(Number(null)) //? 0
console.log(Number("")) //? 0
console.log(Number("12.3")) //? 12.3
console.log(Number("1ab")) //? NaN
console.log(Number("0b101")) //? 5 ("binary sayi sistemi")
console.log(Number("0x10")) //? 16  (hex sayi sistemi)
console.log(String(55))

```
