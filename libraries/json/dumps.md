# dumps

Dictionary veya dictionary listesi veri yapısındaki değişkenin değerini, JSON yapısındaki stringe çevirmek için kullanılır.

{% tabs %}
{% tab title="Kod" %}
```python
import json


dict1 = {
    "emp1": {
        "name": "Lisa",
        "designation": "programmer",
        "age": "34",
        "salary": "54000"
    },
    "emp2": {
        "name": "Elis",
        "designation": "Trainee",
        "age": "24",
        "salary": "40000"
    },
}

json_str = json.dumps(dict1, indent = 6)
print(jsonstr)

```
{% endtab %}

{% tab title="Çıktı" %}
```
{
      "emp1": {
            "name": "Lisa",
            "designation": "programmer",
            "age": "34",
            "salary": "54000"
      },
      "emp2": {
            "name": "Elis",
            "designation": "Trainee",
            "age": "24",
            "salary": "40000"
      }
}
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
**dump metodu dosyaya aktarırken, dumps metodu string bir değişkene aktarır.**
{% endhint %}
