# Liste (list)

Listeler, birbiriyle alakalı birden fazla değeri tutmak için kullanılır. Köşeli parantez içerisinde virgüller ile ayrılarak gösterilirler. Örnek bir liste yapısı aşağıda verilmiştir.

```python
my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

## List Comprehension

Liste oluşturmanın kolay bir yoludur. Eğer herhangi bir listenin her elemanına bir işlem yapılacaksa kullanılır.

```python
squares = list()
for x in range(10):
    squares.append(x**2)

# Yukarıdaki işlem ile aşağıdaki işlem tamamen aynıdır
squares = [x**2 for x in range(10)]
```

