# class

Metotları ve değişkenleri olan, örneği oluşturularak tekrar tekrar kullanılabilen kod bloklarına sınıf denir. Aşağıda basit bir sınıf tanımlaması verilmiştir.

```python
class Class1:
    str = "text"
    num = 10
   
    def print_text(self):
        print(self.str)
```

### Önemli Noktalar

* Sınıf isimleri PEP8 standardına göre CamelCase olarak verilmelidir.
* Kalıtım (inheritance) için "class ClassName(SuperClass):" şekilnde tanımlanır.

### Nesne

Sınıfları kullanabilmek için örneğini oluşturmamız gerekir. Bu örneklere nesne ismi verilir. Bir sınıftan teorik olarak sonsuz sayıda nesne oluşturulabilir.

Aşağıda nesne oluşturmanın bir örneği verilmiştir.

```python
class Car:
    brand: str
    model: int
    
    def run(self):
        print("Car is running")

car = Car()
car.brand = "Ford"
car.model = 2020
car.run()
```

### Constructor (\__init\_\_)

Constructor, nesne oluşturulurken çağrılan fonksiyondur. Yukarıdaki kodun 8. satırında bunun bir örneği vardır. init fonksiyonu içerisinde bazı değişkenlerin varsayılan değeri verilebilir, veya dışarıdan parametre olarak alınan değerler kullanılabilir. init fonskiyonu initialize yani ilklendirme kelimesinden gelmektedir.

Yukarıdaki sınıfı, init fonksiyonu ile tekrar yazalım

```python
class Car:
    brand: str
    model: int
    
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model
    
    def run(self):
        print("Car is running")

car = Car("Ford", 2020)
car.run()
```

5\. satırda başlayan fonksiyon constructor fonksiyonudur. 12. satırda bu fonksiyon, iki parametre ile çağrılmıştır. self anahtar kelimesi ise sınıfın kendisine ait değişkenlere erişim için gereklidir.

### Sınıf Değişkenleri ve self Anahtar Kelimesi

Sınıf değişkenleri, sınıftan üretilen her bir nesne için ayrı değer alabilen değişkenlerdir. Sınıf içerisinde self anahtar kelimesi ile, sınıf dışarısında ise nesne ismi ile erişebiliriz. Aşağıda bunun bir örneği görülmektedir.

```python
class Person:
    name: str
    age: int
    
    def __init__(self, name, age):
        self.name = name
        self.age = age
        
    def change_name(self, new_name):
        self.name = new_name

person = Person("Ahmet", 22)
person.change_name("Ahmet KÖKEN")
person.age = 23

```

Yukarıdaki kod bloğunda 2. ve 3. satırda sınıf değişkenleri tanımlanmıştır. Bunların ilk değerleri init fonksiyonu içerisinde verilmiştir. 10. satırda self anahtar kelimesi ile sınıf değişkenine erişimin bir örneği, 14. satırda ise nesne ile sınıf değişkenlerine erişimin bir örneği verilmiştir.

