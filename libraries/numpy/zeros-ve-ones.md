# zeros ve ones

Her elemanı sıfır veya birlerden oluşan bir numpy dizisi oluşturmak için kullanılır.

### zeros

```python
import numpy as np


x = np.zeros(10)
print(x)
# [0.  0.  0.  0.  0.  0.  0.  0.  0.  0.]
```

```python
import numpy as np


x = np.zeros((3,3))
print(x)
# [[0.  0.  0.] 
#  [0.  0.  0.] 
#  [0.  0.  0.]])
```

{% hint style="info" %}
numpy kütüphanesi, daha doğru hesaplama yapmak için integer değerlerimizi floata çevirerek depoluyor. Yukarıdaki kod bloklarında "0." ve "1." şeklindeki gösterim bunu ifade etmektedir.
{% endhint %}

### ones

```python
import numpy as np


x = np.ones(10)
print(x)
# [1.  1.  1.  1.  1.  1.  1.  1.  1.  1.]
```

```python
import numpy as np


x = np.ones((3,3,3))
print(x)
# [[[1.  1., 1.] 
#   [1.  1.  1.] 
#   [1.  1.  1.]] 
#
#  [[1.  1.  1.] 
#   [1.  1.  1.] 
#   [1.  1.  1.]] 
#
#  [[1.  1.  1.] 
#   [1.  1.  1.] 
#   [1.  1.  1.]]])
```
