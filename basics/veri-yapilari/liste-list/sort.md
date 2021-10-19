# sort

Listenin elemanlarını sıralamak için sort metodu kullanılır. Bu metoda reverse parametresi de gönderilebilir. Eğer gönderilmeze varsayılan değeri False olarak verilmiştir. Eğer biz bu değeri True gönderirsek tersten sıralama yapılır.

```python
fruits = ["orange", "apple", "pear", "banana", "kiwi", "apple", "banana"]

fruits.sort()
# ["apple", "apple", "banana", "banana", "kiwi", "orange", "pear"]

fruits.sort(reverse=True)
# ["pear", "orange", "kiwi", "banana", "banana", "apple", "apple"]

```
