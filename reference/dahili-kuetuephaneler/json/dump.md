# dump

Bir dictionary verisini veya dictionary listesi verisini, dosyaya aktarmaya yarayan metottur.

{% tabs %}
{% tab title="Kod" %}
```python
import json
  
JSON_FILE = "output.json"
dict1 ={
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
  
with open(JSON_FILE, "w") as file:
    json.dump(dict1, file, indent = 6)
  
```
{% endtab %}

{% tab title="Çıktı" %}
{% code title="output.json" %}
```json
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
{% endcode %}
{% endtab %}
{% endtabs %}

{% hint style="info" %}
JSON verisi değişik yapılarda olabilir. Detaylı bilgi için: [https://www.json.org/json-en.html](https://www.json.org/json-en.html)
{% endhint %}
