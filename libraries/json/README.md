---
description: JSON (JavaScript Object Notation)
---

# Json

### JSON Yapısı

Aşağıda örnek bir JSON verisi verilmiştir. Bu veride, en dışta bulunan köşeli parantezler bu verinin bir liste olduğunu belirtir. Köşeli parantezin içindeki her bir süslü parantez ile çevrelenen yapı ise bir nesnedir. Nesneler de 8. satırda görüldüğü gibi kendi içerisinde farklı nesneler içerebilir.

```json
[
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
    },
    {
        "id": 3,
        "first_name": "Noell",
        "last_name": "Bea",
        "email": "nbea2@imageshack.us",
        "gender": "Female",
        "ip_address": "180.66.162.255"
    },
    {
        "id": 4,
        "first_name": "Willard",
        "last_name": "Valek",
        "email": "wvalek3@vk.com",
        "gender": "Male",
        "ip_address": "67.76.188.26"
    }
]

```

Json dosyaları, Pythondaki dictionary yapısındadır. Bu dosyaları okumak için dahili kütüphanelerden biri olan "json" kütüphanesi kullanılır.

{% hint style="info" %}
**Dictionary veri yapısının detayları için: **[dictionary-dict.md](../../basics/veri-yapilari/dictionary-dict.md "mention")****
{% endhint %}
