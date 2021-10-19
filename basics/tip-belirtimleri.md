# Tip Belirtimleri

Python dilinde bir değişken her tipte değeri tutabilir. Ancak programlarımızı geliştirirken mümkün olduğunca bir değişkene farklı tipte değerler vermememiz gerekir. Bu şekilde program geliştirildiğinde hem üzerinden zaman geçtiğinde dönüp kodlara bakınca anlamakta sorun yaşayabiliriz hem de başka geliştiriciler kodları okuduğunda kolay anlayamaz.

Bu sorunların önüne geçmek için değişkenlerimizi tanımlarken tiplerini belirtebiliriz. Program çalışırken bu tiplerin yine bir önemi yoktur ancak geliştirme ve bakım faaliyetleri sırasında kolaylık sağlamaktadır. Aynı şey fonksiyonların dönüş tipi için de geçerlidir. Aşağıda farklı şekillerde tip belirtim örnekleri bulunmaktadır.

Tip belirtmenin diğer bir avantajı da geliştirme sırasında IDE veya editörün kod tamamlama özelliklerini etkin bir şekilde kullanabilmektedir. Tipi belirtilmeyen değişkenlerde kod tamamlama özellikleri tam çalışmayabilir.

## Örnek 1

```python
def greeting(name: str) -> str:
    return 'Hello ' + name
    
```

Yukarıda name değişkeni için string bir değer beklendiği belirtilmiştir. Ayrıca -> str ifadesi ile de bu fonksiyonun, çağrıldığı yere string türünde bir veri göndereceğini ifade eder.

## Örnek 2

```python
Vector = list[float]


def scale(scalar: float, vector: Vector) -> Vector:
    return [scalar * num for num in vector]
    

new_vector = scale(2.0, [1.0, -4.2, 5.4])

```

Yukarıdaki kodun 1. satırında type alias örneği görülmektedir. Eşittirin sağ tarafında görüldüğü şekilde bir tür, Vector olarak isimlendirilmiştir. Artık Vector kelimesi bu türü ifade etmektedir. 4. satırda tanımlanan fonksiyonda ise ikinci parametre ve dönüş değeri olarak bu tür kullanılmıştır.

## Örnek 3

```python
from typing import NewType

UserId = NewType('UserId', int)
some_id = UserId(524313)

```

NewType yardımıyla kendimiz de bir değişken tipi yaratabiliriz. Yaygın bir kullanımı olmasa da bu mümkündür.

## Örnek 4

```python
def square(number: int | float) -> int | float:
    return number ** 2
    
```

Python 3.10 sürümü ile beraber pipe işareti (|) ile birden fazla tip belirtebiliriz. Yukarıdaki fonksiyonda number değişkeninin integer veya float değer alabileceği ve integer veya float değer döndürebileceği belirtilmiştir.

## Örnek 5

```python
a: str = "a"
b: int = 7

name: str
age: int

```

Yukarıda değişken tanımlama sırasında tip belirtme ve ilk değer ataması yaparken tip belirtme örneği görülmektedir.

## Örnek 6

```python
from typing import Dict, List


dict_of_users: Dict[int,str] = {
    1: "Jerome",
    2: "Lewis"
}

list_of_users: List[str] = [
    "Jerome", "Lewis"
]

```

Dictionary ve list tipleri, typing modülünden import edilerek tip belirtmekte kullanılabilir. Bu veri yapılarının hangi ilkel (primitive) tipi kullanacağı da içerisinde belirtilir.

## Örnek 7

```python
from typing import Dict


class User:
    def __init__(self, name):
        self.name = name


users: Dict[int, User] = {
    1: User("Serdar"),
    2: User("Davis")
}


def inspect_user(user:User) -> None:
    print (user.name)


user1 = users[1]
inspect_user(user1)

```

Bu örnekte de bir sınıfın veri tipi olarak belirtildiği görülmektedir. Bu şekilde tip belirtmek, bu değişkenin belirtilen sınıfın bir objesini alabileceğini belirtir.
