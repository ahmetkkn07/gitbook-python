# Git Komutları

## Kullanıcı İşlemleri

### Kullanıcı Adını Ayarlama

```
git config --global user.name "Ahmet KÖKEN"
```

Commitlerde gözükecek kullanıcı adını ayarlar.

### E-posta Adresini Ayarlama

```
git config --global user.email "ahmetkkn07@gmail.com"
```

Commitleri yapacak hesabın e-posta adresini ayarlar.

### Cache Etkinleştirme

```
git config --global credential.helper cache
```

Kullanıcı adı ve şifreyi kaydederek her seferinde girilmesini engeller.

### Varsayılan Editörü Ayarlama

```
git config --global core.editor nano
```

Commit mesajı eklerken kullanılacak varsayılan editörü ayarlar.

## Repository İşlemleri

### Repository Oluşturma

```
git init
```

Bulunulan dizinde yeni bir git deposu oluşturmaya yarar.

### Dosyaları Geçiş Bölgesine Ekleme

```
git add .
```

Dizin içerisindeki tüm dosyaları ekler.

```
git add somefile.py
```

Herhangi bir dosyayı geçiş bölgesine ekler.

### Repository Durumunu Görüntüleme

```
git status
```

Repository içerisindeki dosyaların durumunu gösterir.

### Commit Etme

```
git commit -m "Tek satırlık commit mesajı"
```

Çift tırnak arasındaki mesaj ile commit etmeyi sağlar.

```
git commit
```

Varsayılan editörü açar ve commit mesajı girmemizi ister. Genellikle ilk satırda başlık kullanılır. Başlıktan sonra ikinci satır boş bırakılır. Üçüncü satırdan itibaren birden fazla satır şeklinde değişiklikler belirtilir.

### Commit Geçmişini Görüntüleme

```
git log
```

Terminalde geçmiş commitleri ve mesajlarını gösterir.

```
git log --oneline
```

Her commit için bir satırlık mesaj göstererek daha kompakt bir görünüm sağlar.

### Belirli Bir Commit Detayını Görüntüleme

```
git show 1af17e73721dbe0c40011b82ed4bb1a7dbe3ce29
```

Git log ile görüntülenen commitlerden herhangi birisinin detayını görüntülemek istersek kullanırız. Tam commit kodu yerine kısa hash kodu da kullanılabilir.







###
