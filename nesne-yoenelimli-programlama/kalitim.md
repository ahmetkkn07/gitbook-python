---
description: Inheritance
---

# Kalıtım

Kalıtım, metotları ve değikenlerini başka bir sınıftan miras alan bir sınıf tanımlamamızı sağlar.

Üst sınıf (parent class, super class), temel sınıf (base class) olarak da adlandırılan, miras alınan sınıftır.

Alt sınıf (child class), türetilmiş sınıf olarak da adlandırılan başka bir sınıftan miras alan sınıftır.

```python
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    print(self.firstname, self.lastname)
    

person1 = Person("John", "Doe")
person1.printname()


class Student(Person):
  def __init__(self, fname, lname, year):
    super().__init__(fname, lname)
    self.graduationyear = year

student1 = Student("Mike", "Olsen", 2019)
student1.printname()

```

Yukarıda bir kalıtım örneği verilmiştir. Burada base sınıf, Person sınıfıdır. Student isimli sınıf, Person sınıfının tüm özellk ve metotlarını miras almıştır. Miras alan sınıf, kendi metot ve değişkenlerini de tanımlayabilir. Bu sayede basse sınıfın daha özelleşmiş bir örneği oluşturulur.
