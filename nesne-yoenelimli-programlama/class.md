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

### Sınıf Değişkenleri ve self Anahtar E



