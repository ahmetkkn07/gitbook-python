# array

Python listesinden numpy dizileri oluşturmaya yarar.

```python
import numpy as np


arr = np.array([1, 2, 3, 4, 5])
print(arr)
# [1  2  3  4  5]
```

Numpy dizileri çok boyutlu dizilerde indekslemeyi kolaylaştırır. Aşağıda bunun bir örneği verilmiştir.

{% tabs %}
{% tab title="Python List" %}
```python
my_list = [[10, 20, 30],
           [40, 50, 60],
           [70, 80, 90]]
           
print(my_list[1][2])
# 60

```
{% endtab %}

{% tab title="Numpy Array" %}
```python
import numpy as np


arr = np.array([[10, 20, 30],
                [40, 50, 60],
                [70, 80, 90]])
                
print(arr[1,2])
# 60

```
{% endtab %}
{% endtabs %}
