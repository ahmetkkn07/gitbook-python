# Tuple

Tuple veri yapısı, liste ile benzer özelliklere sahiptir. listelerden farkı, içerisindeki değerlerin değiştirilememesidir.

```python
tup = (1, 2, 3)
tup[0] = 5
```

Yukarıdaki kod parçasında 2. satır hata verecektir. Çünkü tuple içerisindeki değer sonradan değiştirilemez.

{% hint style="info" %}
**Tuple veri yapısı içerisindeki değiştirilemez ancak içerisinde referans türünde veri tutuyorsa bu verilerin değeri değiştirilebilir.**
{% endhint %}

```python
tup = ([1, 2, 3], [3, 2, 1])
tup[0].append(4)
```
