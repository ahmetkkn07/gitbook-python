# loads

JSON yapısındaki stringi dictionary veri yapısına çevirmek için kullanılır.

{% tabs %}
{% tab title="Kod" %}
```python
import json


json_str = """[
    {
        "id": 1,
        "first_name": "Jeanette",
        "last_name": "Penddreth",
        "email": "jpenddreth0@census.gov",
        "gender": "Female",
        "ip_address": {
            "v4": "26.58.193.2"
        }
    },
    {
        "id": 2,
        "first_name": "Giavani",
        "last_name": "Frediani",
        "email": "gfrediani1@senate.gov",
        "gender": "Male",
        "ip_address": "229.179.4.212"
    }
]"""

json_dict = json.loads(json_str)
print(json_dict[0]["email"])

```
{% endtab %}

{% tab title="Çıktı" %}
gfrediani1@senate.gov
{% endtab %}
{% endtabs %}

{% hint style="info" %}
**load metodu dosyadan okurken, loads metodu string bir değişkenden parse işlemi yapar.**
{% endhint %}
