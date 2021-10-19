# Set

Set yani küme veri yapısı, matematikteki küme kavramı gibi aynı elemanın birden fazla tekrar etmediği veri türüdür. Süslü parantez ile gösterilir.

{% tabs %}
{% tab title="Kod" %}
```python
my_set = {1, 2, 3, 5, 6, 2, 1, 3, 2, 5}
print(my_set)
```
{% endtab %}

{% tab title="Çıktı" %}
{1, 2, 3, 5, 6}
{% endtab %}
{% endtabs %}

Setlere aynı eleman birden fazla kez eklense de sadece bir tanesi yer alır.

Diğer veri türleri set() fonksiyonu yardımıyla kümeye dönüştürülebilir.

Matematiksel küme işlemleri bu veri türünde yapılabilir.

```python
a = set("abracadabra")
# a = {"a", "r", "b", "c", "d"}

b = set("alacazam")
# b = {"a", "l", "c", "z", "m"}

print(a)
# >> {"a", "r", "b", "c", "d"}
print(b)
# >> {"a", "l", "c", "z", "m"}

# letters in a but not in b
# a'da olup b'de olmayan harfler
print(a - b)
# >> {'r', 'd', 'b'}

# letters in a or b or both
# a veya b'de olan harfler (birleşim)
print(a | b)
# >> {'a', 'c', 'r', 'd', 'b', 'm', 'z', 'l'}

# letters in both a and b
# a ve b'de olan harfler (kesişim)
print(a & b)
# >> {'a', 'c'}

# letters in a or b but not both
# a ya da b'de olan harfler (ortaklar hariç)
print(a ^ b)
# >> {'r', 'd', 'b', 'm', 'z', 'l'}
```
