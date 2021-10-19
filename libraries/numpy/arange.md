# arange

range komutu ile benzer işleve sahiptir. Başlangıç ve bitiş değerleri arasında birer birer artan bir numpy dizisi üretir.

```python
import numpy as np


x = np.arange(10, 20)
print(x)
# [10  11  12  13  14  15  16  17  18  19]
```

İsteğe bağlı olarak artış miktarı da parametre olarak verilebilir.

```python
import numpy as np


x = np.arange(0, 100, 3)
# [ 0  3  6  9  12  15  18  21  24  27  30  33  36  39  42  45  48 
#   51  54  57  60  63  66  69  72  75  78  81  84  87  90  93  96  99]
```

{% hint style="warning" %}
Üst sınır dahil değil!
{% endhint %}
