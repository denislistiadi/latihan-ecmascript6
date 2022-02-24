# ECMAScript 6

### Deklarasi Variabel
Di dalam ecmascript 6, mendeklarasikan variabel menggunakan **let** dan **const**, yang sebelumnya menggunakan **var**.
Menggunakan **let** jika variabel akan diinisialisasi ulang, dan gunakan **const** jika tidak diinisialisasi ulang.
Misal:
``` Javascript
    // Sebelum ecmascript 6
    var fruits = ["apel","jeruk", "anggur"];

    // Setelah ecmascript 6
    let fruits = ["apel","jeruk", "anggur"];
    // atau menggunakan const
    const fruits = ["apel","jeruk", "anggur"];
```

### Template Literals
Di dalam ecmascript 6, menggabungkan string menggunakan template literals, misalnya:
``` Javascript
    // Tanpa template literals
    console.log(error + " tidak ditemukan");

    // Menggunakan template literals
    console.log(`${error} tidak ditemukan`)
```

### Destructuring Object

``` Javascript
    const fruits = {
        first = "Anggur",
        second = "Pisang"
    };

    // Sebelum ES6
    const first = fruits.first;
    const second = fruits.second;

    // Setelah ES6
    const {first, second} = fruits;
```

### Function
Di dalam ES6 terdapat 2 penulisan function syntax, yaitu regular function dan arrow function
``` Javascript
    // Regular function
    function perkenalan(name) {
        console.log(`Nama saya adalah ${name}`);
    };

    // Arrow function
    const perkenalan = (name) => console.log(`Nama saya adalah ${name}`);
```

### Class
Sebelum ES6, untuk membuat class menggunakan **constructor function** dan untuk menambahkan method menggunakan konsep **prototype**. 
Namun setelah ES6, class dapat dibuat dengan menggunakan **class**. Misal:
``` Javascript
    // Class Sebelum ES6
    function Person(name) {
        this.name = name;
    };

    Person.prototype.sayHello = function() {
        console.log("Hello, my name is " + this.name);
    };

    var Andi = new Person("Andi");

    // Class Setelah ES6
    class Person {
        constructor(name) {
            this.name = name;
        }

        sayHello() {
            console.log(`Hello, my name is ${this.name}`);
        }
    }

    const Andi = new Person("Andi");
```
Di dalam class ES6, untuk mengakses parent class, menggunakan keyword **extends**. Dan untuk mengakses properti atau method, bisa menggunakan **super()**. Misal:
``` Javascript
    class Person {
        constructor(name) {
            this.name = name;
        }
    }

    class Student extends Person {
        constructor(name, school) {
            super(name);
            this.school = school;
        }
    }
```
### Promise
Di dalam ES6, untuk menggantikan callback menggunakan promise. Promise dapat dibuat dengan menggunakan **.then** atau **async/await**. Misal:
``` Javascript
    const clickButton = () => {
        Person.getData()
            .then(data => console.log(data))
            .catch(error => console.log(error));
    };

    // Menggunakan async/await
    const clickButton = async () => {
        try{
            const data = await Person.getData();
            console.log(data);
        } catch (error) {
            console.log(error);
        }
    };
```

### Module
Sebelum ES6, mengimport module menggunakan <script"></script> tag. Di ES6, mengimport module menggunakan import. Misal:
``` Javascript
    // Sebelum ES6
    <script src="module.js"></script>

    // Setelah ES6
    import {name, age} from "module.js";
```


##### Dan didalam directory *src/script* adalah latihan mengubah kode saya agar sesuai dengan EcmaScript 6.