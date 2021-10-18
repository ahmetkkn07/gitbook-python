---
description: >-
  Dicitionary veri yapısı, anahtar:değer (key:value) çiftlerini saklamak için
  kullanılır.
---

# Dictionary (dict)

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
print(car.get("year"))
```
{% endtab %}

{% tab title="Çıktı" %}
2020
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Anahtar ile erişirken köşeli parantez kullanırsak, eğer o anahtar sözlükte yoksa hata vercektir. Bu hatanın önüne geçmek için get kullanılabilir. Eğer o anahtar sözlükte yoksa None değerini döndürecektir.
{% endhint %}

### For Döngüsü ile Gezinme

Dictionary nesnesi üzerinde listede olduğundan biraz daha farklı şekilde gezinilir. Aşağıda k anahtarı, v ise değeri temsil etmektedir.

{% tabs %}
{% tab title="Kod" %}
```python
knights = {
    "gallahad": "the pure", 
    "robin": "the brave"
}

for k, v in knights.items():
    print(k, v)
```
{% endtab %}

{% tab title="Çıktı" %}
gallahad the pure

robin the brave
{% endtab %}
{% endtabs %}
