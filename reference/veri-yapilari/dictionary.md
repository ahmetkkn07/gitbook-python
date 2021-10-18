---
description: >-
  Dicitionary veri yapısı, anahtar:değer (key:value) çiftlerini saklamak için
  kullanılır.
---

# Dictionary

Aşağıda örnek bir dictionary yapısı görülmektedir.

```python
car = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
```

Bir dictionary içerisinde aynı anahtar birden fazla kullanılamaz çünkü her bir anahtar, karşılığındaki değere erişmek için kullanılır. Aşağıda değerlere erişim için bir örnek verilmiştir.

{% tabs %}
{% tab title="Kod" %}
```python
print(car["brand"])
print(car["model"])
print(car["year"])
```
{% endtab %}

{% tab title="Çıktı" %}
Ford

Mustang

1964
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
Aynı anahtar birden fazla kez kullanıldığında hata vermez ancak önceki anahtar ezilir. Örneğin:
{% endhint %}

{% tabs %}
{% tab title="Kod" %}
```python
car = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964,
  "year": 2020
}
print(car["year"])
```
{% endtab %}

{% tab title="Çıktı" %}
2020
{% endtab %}
{% endtabs %}
