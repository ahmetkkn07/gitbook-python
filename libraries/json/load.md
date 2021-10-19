# load

load methodu, dosyadan okunan json verisini yüklemeye yarayan metottur.

{% tabs %}
{% tab title="Kod" %}
```python
import json


JSON_FILE = "data.json"


with open(JSON_FILE, "r") as file:
    datas = json.load(file)


for data in datas:
    print(data["first_name"])

print("ip", datas[0]["ip_address"]["v4"])

```
{% endtab %}

{% tab title="Çıktı" %}
Jeanette

Giavani

Noell

Willard

ip 26.58.193.2
{% endtab %}
{% endtabs %}

Yukarıdaki kod bloğunda, örnek json verisi dosyadan okunmuştur. Burada datas değişkeninin tipi \[dict] yani dictionary listesidir. For döngüsü ile her bir nesne üzerinde gezindiğimiz takdirde data değişkeni dictionary tipinde olur.

Dictionary veri yapısında bir özelliğin değerine erişmek için key ismi verilen değer kullanılır. 11. satırda görüldüğü üzere tüm verilerin "first\_name" anahtarına karşılık gelen değerleri ekrana yazdırılmıştır.

İç içe nesne içeren verilerde ise 13. satırda görüldüğü gibi peş peşe anahtarlama yapılabilir.
