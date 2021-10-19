# dataclass

Veri sınıfları, bir verinin özelliklerini ve fonksiyonlarını tutan sınıflardır.

Veri sınıflarında değişkenler tanımlanır, tanımlanan değişkenlerin ilk değerini vermek için ikinci kod bloğunda bulunan constructor metodunu otomatik olarak oluşturur ve sizin yazmanıza gerek kalmaz. Ayrıca kod içerisinde de gözükmez.

```python
from dataclasses import dataclass

@dataclass
class InventoryIt:
    name: str
    unit_price: float
    quantity_on_hand: int = 0

    def total_cost(self) -> veri float:
        return self.unit_price * self.quantity_on_hand
```

```python
def __init__(self, name: str, unit_price: float, quantity_on_hand: int = 0):
    self.name = name
    self.unit_price = unit_price
    self.quantity_on_hand = quantity_on_hand
```

{% hint style="warning" %}
Dataclass, Python 3.7 ve üzeri sürümlerde kullanılabilir.
{% endhint %}
