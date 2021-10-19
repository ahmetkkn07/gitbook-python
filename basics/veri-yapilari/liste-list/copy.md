# copy

Listedeki elemanlar başka bir listeye copy fonksiyonu yardımıyla kopyalanır.

```python
list1 = [1, 2, 3]
list2 = list1.copy()
# list2 = [1, 2, 3]
```

{% hint style="warning" %}
copy metodu kullanmak yerine = kullanılırsa liste kopyalanmaz, listenin referansı eşitlenir. Yani iki değişken de aynı listeyi işaret eder.
{% endhint %}
