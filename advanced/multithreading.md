# multithreading

Multithreading, bir işlemcide birden fazla işlemin yapılmasıdır. Asenskron programlama için kullanılır.

Multithread bir programın çalışması tek bir process üzerinden sağlanırken, bu process üzerinde birden fazla işlem parçacığı çalışmaktadır. Process üzerinde çalışan bu çoklu işlem parçacıkları, asenkron olarak farklı görevleri yerine getirmek için kullanılırlar. Bu sayede birbirlerini beklemesi gerekmeyen işlemlerin, tek bir process üzerinde asenkron olarak gerçekleştirilmeleri sağlanır ve performans arttırılmış olur.

Bir Python programında Main thread bulunur ve bütün işlemler bu thread üzerinden yürütülür. threading modulü yardımıyla biz thread oluşturabilir ve bu threadlere iş verebiliriz.

### Senkron Çalışma

Aşağıda senkron çalışmaya bir örnek verilmiştir. Bütün işlemler tek bir thread üzerinden yürütülmekte ve bir işlemin başlaması için diğer işlemin bitmesi gerekmektedir. Yani işlemler sıralı olarak yapılır.

{% tabs %}
{% tab title="Kod" %}
```python
import time


def useless_function(seconds):
    print(f'Waiting for {seconds} second(s)', end="\n")
    time.sleep(seconds)
    print(f'Done Waiting {seconds}  second(s)')


start = time.perf_counter()

useless_function(1)
useless_function(2)

end = time.perf_counter()

print(f'Finished in {round(end-start, 2)} second(s)')
```
{% endtab %}

{% tab title="Çıktı" %}
Waiting for 1 second(s)

Done Waiting 1 second(s)

Waiting for 2 second(s)

Done Waiting 2 second(s)

Finished in 3.0 second(s)
{% endtab %}
{% endtabs %}

Görüldüğü üzere yukarıda program 3 saniyede sonlanmıştır. Çünkü fonksiyon ikinci kez çağrılmadan önce birinci işlemin tamamlanması beklenmiştir.

### Asenkron Çalışma

Aşağıda ise asenkron çalışmaya bir örnek verilmiştir. Burada threading modülü yardımıyla, Main threadin yanı sıra iki yeni thread oluşturulmuştur. Bu sayede bir threadin yaptığı işlem kesintiye uğradığı zaman context switching işlemi ile diğer threadin işlemleri yürütülür. Bu çeşit programlama genelde I/O işlemleri gibi bekleme gereken kısımlarda kullanılır.

{% tabs %}
{% tab title="Kod" %}
```python
import threading
import time


def useless_function(seconds):
    print(f'Waiting for {seconds} second(s)', end="\n")
    time.sleep(seconds)
    print(f'Done Waiting {seconds}  second(s)')


start = time.perf_counter()

t1 = threading.Thread(target=useless_function, args=[1])
t1.start()

t2 = threading.Thread(target=useless_function, args=[2])
t2.start()

print(f'Active Threads: {threading.active_count()}')

t2.join()

end = time.perf_counter()

print(f'Finished in {round(end-start, 2)} second(s)')

```
{% endtab %}

{% tab title="Çıktı" %}
Waiting for 1 second(s)

Waiting for 2 second(s)

Active Threads: 3

Done Waiting 1 second(s)

Done Waiting 2 second(s)

Finished in 2.0 second(s)
{% endtab %}
{% endtabs %}

Görüldüğü üzere program 2 saniyede tamamlanmıştır. Çünkü fonksiyon birinci kez çağrıldığında 1 saniyelik uykuya geçince işlem sırası diğer threade gelir. Bu thread de 2 saniyelk uykuya geçtiğinde program birinci threade döner. Birinci thread tamamlandığında sıra tekrar ikinci threade geçer. Bu da tamamlandığında program sonlanır.

21\. satırda bulunan join işlemi, bu threaddeki işlemin bitmesini beklemek için kullanılır. Eğer join işlemi yapılmazsa program 0 saniyede sonlarır ve arkaplanda threadler işlerine devam eder. Ancak bu tip bir durum genelde istenmez. (Program sonlandığında tüm threadlerin bitmiş olması beklenir.)

{% hint style="danger" %}
Eğer threadlerde kesintiye girecek süre bulunmazsa program senkron gibi davranır ve diğer threadler araya giremediği için bu threadin işleminin bitmesi beklenir.
{% endhint %}

Eğer threadlerden herhangi birisinde while True döngüsü varsa bu döngüde kesintiye girecek bir I/O işlemi olduğundan emin olun. Eğer yoksa bir sleep kullanmanız gerekebilir.

{% hint style="warning" %}
Multithreading, aynı andan bir fazla işlemci çekirdeğini kullanmak için değildir. Bunun için multiprocessing konusuna bakınız.
{% endhint %}
