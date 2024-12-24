### README - BenimSinifim Sınıfı

#### Amaç
Bu Python kodu, bir sınıf (`class`) tanımlayarak nesne tabanlı programlama (OOP) konseptlerini basit bir şekilde göstermeyi amaçlamaktadır. Kod, bir nesneye ait özelliklerin (`attribute`) nasıl atanabileceğini, değiştirilebileceğini ve silinebileceğini açıklayan bir örnek sunmaktadır.

---

### **Kod Açıklaması**

#### **Sınıf Tanımı**
`BenimSinifim` adlı bir sınıf tanımlanmıştır. Bu sınıfın iki ana işlevi vardır:
1. **Özellik Tanımlama:** Sınıf, `name` (isim) ve `age` (yaş) özelliklerine sahiptir.
2. **Davranış Belirleme:** Sınıfa ait `kendiFunc` ve `__str__` isimli iki metot bulunmaktadır.

---

#### **Metotlar**
1. **`__init__` Metodu:**  
   Sınıfın kurucu metodudur. `name` ve `age` değerlerini alarak nesneye atar.  
   **Kullanım:**  
   ```python
   p1 = BenimSinifim("Berk", 20)
   ```

2. **`kendiFunc` Metodu:**  
   Nesneye ait `name` özelliğini kullanarak bir mesaj yazdırır.  
   **Kullanım:**  
   ```python
   p1.kendiFunc()
   ```

3. **`__str__` Metodu:**  
   Nesne yazdırıldığında ekrana `name` ve `age` değerlerini döner.  
   **Kullanım:**  
   ```python
   print(p1)
   ```

---

#### **Özelliklerin Güncellenmesi**
Sınıfa ait özellikler, nesne oluşturulduktan sonra da değiştirilebilir:  
```python
p1.age = 15
```

---

#### **Özellik ve Nesne Silme**
Python'un `del` komutu ile nesneye veya nesnenin özelliklerine ait referanslar silinebilir:  
```python
del p1.age  # Sadece age özelliğini siler
del p1      # p1 nesnesini tamamen siler
```

---

#### **Hata Durumları**
Kodun sonunda, `p1` nesnesi ve `p1.age` özelliği silindikten sonra tekrar erişilmeye çalışılmaktadır:  
```python
print(p1.age)  # Hata verir, çünkü age özelliği silinmiştir
p1.kendiFunc()  # Hata verir, çünkü p1 nesnesi silinmiştir
```
Bu durum, `AttributeError` veya `NameError` hatalarına yol açar.

---

### **Kodun Çalıştırılması**
1. Python yüklü bir bilgisayarda dosyayı çalıştırın.
2. `print` ve `del` işlemlerinden sonra hata almayı bekleyin. Hatalar bilinçli olarak gösterilmek istenmiştir.

---

### **Geliştirme Notları**
- Silme işlemi öncesi bir kontrol mekanizması eklenebilir.
- Kullanıcı hatalarını daha anlamlı bir şekilde ele almak için try-except blokları kullanılabilir. 

Bu kod, temel sınıf yapısını anlamak için bir başlangıç noktasıdır.
