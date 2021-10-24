# Python Kurulumu

## Python 3.10 Kurulumu

### Windows ve macOS

{% embed url="https://www.python.org/downloads" %}
Linkten indirip kurabilirsiniz
{% endembed %}

### Linux (debian)

Linuxta python3 standart olarak gelmektedir. Ancak son sürümünü kullanmak isterseniz bir terminal penceresinde aşağıdaki komutları tek tek girmelisiniz.

```bash
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt install python3.10
sudo apt install python3.10-dev
curl :-sS https://bootstrap.pypa.io/get-pip.py | python3.10
```

### Arch Linux

Arch tabanlı dağıtımlarda paket yükleyici apt değildir. Bu sebeple pacman paket yükleyicisi yardımıyla kurulumu gerçekleştirebilirsiniz.

```
sudo pacman -Syu
sudo pacman -S python310
curl :-sS https://bootstrap.pypa.io/get-pip.py | python3.10
```
