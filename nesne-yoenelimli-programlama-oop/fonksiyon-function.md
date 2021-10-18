# Fonksiyon (function)

Fonksiyon, sadece çağrıldığı zaman çalışan kod parçasıdır. Fonksiyonu veri gönderilip geriye veriye alınabilir. Gönderilen veriye parametre, dönen değere return data denir. Aşağıda basit bir fonksiyon tanımı görülmektedir.

{% tabs %}
{% tab title="Kod" %}
```python
def func1():
    print("Hello World!")
    
func1()
```
{% endtab %}

{% tab title="Çıktı" %}
Hello World!
{% endtab %}
{% endtabs %}

def anahtar kelimesi ile fonksiyon tanımlanır. Fonksiyon bloğu içerisinde yapılacak işlemler gerçekleştirilir. fonksiyon_adı() şekllinde ise fonksiyon çağrılır.

{% hint style="success" %}
Bir fonksiyon birden fazla çalıştırılabilir. Bu sebeple programlarımızda aynı kod birden fazla tekrar ediyorsa, o bloğu fonksiyon haline getirip her seferinde çağırırız.
{% endhint %}

### Parametre ve Return

Bazı fonksiyonlarda dışarıdan veri almaya, bazılarında veri döndürmeye, bazılarında ise her ikisine ihtiyaç duyarız. Eğer fonksiyon dışarıdan değer alacaksa fonksiyona parametre göndeririz. Parametre sayısı bir tane olabileceği gibi birden fazla da olabilir. Ayrıca gönderilen parametre herhangi bir nesne olabilir. Fonksiyondan dışarıya değer almamız gerekiyorsa da return anahtar kelimesi ile o veriyi geri göndeririz.

{% tabs %}
{% tab title="Kod" %}
```python
def greet(name):
    return f"Hi {name}"
    
print(greet("Ahmet"))
```
{% endtab %}

{% tab title="Çıktı" %}
Hi Ahmet
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
Fonskiyonun herhangi bir yerinde return anahtar kelimesi çalışırsa fonksiyon sonlanır ve program akışı, fonksiyonun çağrıldığı yere geri döner.
{% endhint %}

{% hint style="info" %}
Fonksiyondan birden fazla değer döndürmek gerektiğinde birden fazla return kullanılamaz. Eğer birden fazla veri döndürmek istersek liste \[] veya tuple () veri yapısını kullanırız. Yaygın olarak tuple veri yapısı tercih edilir.
{% endhint %}
