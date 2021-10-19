# seed

Rastgele oluşan her sayı grubuiçin bir seed tanımlıdır. Eğer her üretimde aynı rastgele sayıların üretilmesini istersek seed komutunu kullanırız.

```python
import numpy as np


np.random.seed(2021)

x = np.random.randint(0, 10, 5)
print(x)
# [4 5 9 0 6]
```

{% hint style="info" %}
Yukarıdaki kodu kendiniz çalıştırmayı denerseniz yine aynı rastgele sayılar üretilecektir.
{% endhint %}
