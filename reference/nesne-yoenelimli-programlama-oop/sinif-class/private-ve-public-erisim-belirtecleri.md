# Private ve Public Erişim Belirteçleri

Python dilinde, diğer dillerdeki gibi erişim belirteci bulunmamaktadır. Ancak bu şekilde erişim belirteçlerinin bulunmaması, bu işlevlerin olmadığı anlamına gelmez.

Public erişim belirteci, değişken veya fonksiyonun dışarıdan erişebileceğini tanımlar.

Private erişim belirteci, değişken veya fonksiyona sadece sınıf içerisinden erişilebileceğini belirtir.

Pythonda tanımlanan tüm değişken ve fonksiyonlar normalde publictir. Private olarak tanımlamak için değişken veya fonksiyon adının başına \__ (çift alt tire) getirilir. Aşağıda public ve private değişken ve fonksiyon örnekleri verilmiştir.

{% tabs %}
{% tab title="Kod" %}
```python
import datetime


class Person:
    name: str
    dob: int
    __age: int

    def __init__(self, name, dob) -> None:
        self.name = name
        self.dob = dob
        self.__calculate_age()

    def __calculate_age(self):
        self.__age = datetime.datetime.now().year - self.dob

    def recalculate_age(self):
        self.__calculate_age()


person = Person("Ahmet", 1999)
print(person.name)
person.recalculate_age()
person.__calculate_age()
print(person.__age)

```
{% endtab %}

{% tab title="Çıktı" %}
Ahmet

Ahmet Traceback (most recent call last): 

File "/home/ahmetkkn07/Desktop/private.py", line 24, in 

      person.\__calculate_age() 

AttributeError: 'Person' object has no attribute '\__calculate_age'

Traceback (most recent call last): 

File "/home/ahmetkkn07/Desktop/private.py", line 25, in 

      print(person.\__age) 

AttributeError: 'Person' object has no attribute '\__age'
{% endtab %}
{% endtabs %}

Yukarıda görüldüğü üzere 24. ve 25. satırdaki ifadeler hata verecektir. Çünkü private fonksiyon ve değişkenlere dışarıdan erişilemez. 12. satırda gördüğünüz gibi sınıfın içerisinden erişildiğinde ise hata alınmamıştır.
