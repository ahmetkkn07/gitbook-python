# rand, randn ve randint

Rastgele sayılar oluşturmaya yarayan fonksiyonlardır.

### rand

0 ile 1 arasında **\[0, 1)** istenen adet kadar rastgele sayı oluşturur.

```python
import numpy as np


x = np.random.rand(5)
print(x)
# [0.31801013  0.43973085  0.44581445  0.67724802  0.41159006]
```

### randn

0 etrafında negatif ve pozitif değerlerle, normal dağılıma (Gaussian  Distribution) göre değerler oluşturur.

```python
import numpy as np


x = np.random.randn(10)
print(x)
# [-1.67155361  0.5474927  -1.07769193  0.14089541  0.63481647,
#   0.30553815  -1.1648442  -0.18526607  1.97819333  -0.24172663]


y = np.random.randn(3, 4)
print(y)
# [[ 1.33262386  -0.88922967  -0.07056098  0.27340112]
#  [ 1.00664965  -0.68443807   0.43801295  -0.35874714]
#  [-0.19289416  -0.42746963  -1.80435223  0.02751727]]
```

### randint

Alt sınır ve üst sınır arasında **\[alt, üst)** rastgele tam sayı oluşturur. İstersek kaç sayı istediğimizi de belirtebiliriz.

```python
import numpy as np


x = np.random.randint(0,10)
print(x)
# 3


y = np.random.randint(1,10,5)
print(y)
# [7  9  6  1  5]
```

