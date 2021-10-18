# Password Generator

Aşağıdaki kod bloğu, 9. satırda belirtilen uzunlukta şifreler oluşturmaya yarar.

{% code title="passwordGenerator.py" %}
```python
import random

chars = "abcdefghijklmnopqrstuvwxyz"
chars += chars.upper()
nums = str(1234567890)
special_chars = "!@#$%^&*()_+"
chars += nums + special_chars

length = 16

password = "".join(random.sample(chars, length))
print(password)

```
{% endcode %}
