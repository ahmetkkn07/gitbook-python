# Liste (list)

Listeler, birbiriyle alakalı birden fazla değeri tutmak için kullanılır. Köşeli parantez içerisinde virgüller ile ayrılarak gösterilirler. Örnek bir liste yapısı aşağıda verilmiştir.

```python
my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

## Listelerde İşlemler

Listelerin çeşitli metotları vardır. Bunlar çoğu işlemi uğraşmadan yapmamızı sağlar.

### Ekleme

Listeye veri eklemek için üç farklı metot vardır. Bunlar append, extend ve insert metotlarıdır.

#### append

Listenin sonuna ekleme işleminde kullanılır.

```python
my_list = [1, 2, 3]

my_list.append(4)
# my_list = [1, 2, 3, 4]
```

#### extend

Listeyi iterable bir nesne ile genişletmeye yarar.

```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]

list1.extend(list2)
# list1 = [1, 2, 3, 4, 5, 6]
```

#### insert

İstenilen indekse (zero indexed) değer eklemeyi sağlar.

```python
my_list = [10, 20, 30]

my_list.insert(1,100)
# my_list = [10, 100, 20, 30]
```

### Silme

Silme işlemi için remove, pop ve clear metotlarından yararlanılır.

#### remove

Verilen değere eşit olan ilk elemanı listeden kaldırmaya yarar. Yani aynı değer birden fazla kez tekrar ediyorsa ilk sırada olan kaldırılır.

```python
my_list = [8, 7, 7, 5, 7, 6]

my_list.remove(7)
# my_list = [8, 7, 5, 7, 6]
```

#### pop

Verilen indekste bulunan elemanı kaldırır ve return eder. Eğer indeks verilmezse son elemanı kaldırır ve return eder.

```python
my_list = [1, 2, 3, 4]

last = my_list.pop()
# last = 4, my_list = [1, 2, 3]

x = my_list.pop(1)
# x = 2, my_list = [1, 3]
```

#### clear

Listenin tüm elemanlarını siler.

```python
my_list = [1, 2, 3, 4]

my_list.clear()
# my_list = []
```

### Sıralama

Listenin elemanlarını sıralamak için sort metodu kullanılır. Bu metoda reverse parametresi de gönderilebilir. Eğer gönderilmeze varsayılan değeri False olarak verilmiştir. Eğer biz bu değeri True gönderirsek tersten sıralama yapılır.

```python
fruits = ["orange", "apple", "pear", "banana", "kiwi", "apple", "banana"]

fruits.sort()
# ["apple", "apple", "banana", "banana", "kiwi", "orange", "pear"]

fruits.sort(reverse=True)
# ["pear", "orange", "kiwi", "banana", "banana", "apple", "apple"]
```

### Ters Çevirme

Listedeki elemanların sırası reverse fonksiyonu yardımıyla ters çevrilebilir.

```python
fruits = ["apple", "apple", "banana", "banana", "kiwi", "orange", "pear"]

fruits.reverse()
# ["pear", "orange", "kiwi", "banana", "banana", "apple", "apple"]
```

### İstenen Elemanın Sayısı

Listedeki istenen eleman sayısı, count fonksiyonu yardımıyla bulunur. Bu fonksiyona parametre olarak istenen eleman gönderilir.

```python
fruits = ["orange", "apple", "pear", "banana", "kiwi", "apple", "banana"]

cnt = fruits.count('apple')
# cnt = 2
```

### Kopyalama

Listedeki elemanlar başka bir listeye copy fonksiyonu yardımıyla kopyalanır.

```python
list1 = [1, 2, 3]
list2 = list1.copy()
# list2 = [1, 2, 3]
```

{% hint style="warning" %}
copy metodu kullanmak yerine = kullanılırsa liste kopyalanmaz, listenin referansı eşitlenir. Yani iki değişken de aynı listeyi işaret eder.
{% endhint %}

## List Comprehension

Liste oluşturmanın kolay bir yoludur. Eğer herhangi bir listenin her elemanına bir işlem yapılacaksa kullanılır.

```python
squares = list()
for x in range(10):
    squares.append(x**2)

# Yukarıdaki işlem ile aşağıdaki işlem tamamen aynıdır
squares = [x**2 for x in range(10)]
```

