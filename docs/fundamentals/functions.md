# C++ Functions

![Topic](https://img.shields.io/badge/Topic-Functions-blue)
![Level](https://img.shields.io/badge/Level-Beginner--Intermediate-green)

---

## 📌 Kirish

Funksiya — bu **ma’lum bir vazifani bajaruvchi kod bloki**.  
Funksiyalar yordamida:

- kodni takror yozmaslik
- dastur tuzilishini toza qilish
- katta muammolarni kichik qismlarga bo‘lish

mumkin.

C++ da funksiyalar **professional dasturlashning asosi** hisoblanadi.

---

## 🧱 Funksiya sintaksisi

```cpp
return_type function_name(parameters) {
    // function body
    return value;
}
````

### Misol:

```cpp
int add(int a, int b) {
    return a + b;
}
```

---

## ▶️ Funksiyani chaqirish

```cpp
int result = add(3, 5);
cout << result; // 8
```

---

## 🔢 Return type

| Return type | Tavsif                 |
| ----------- | ---------------------- |
| `int`       | Butun son qaytaradi    |
| `double`    | O‘nli son              |
| `void`      | Hech narsa qaytarmaydi |
| `bool`      | true / false           |

### `void` funksiya misoli

```cpp
void sayHello() {
    cout << "Hello C++";
}
```

---

## 📥 Parametrlar va argumentlar

```cpp
void greet(string name) {
    cout << "Hello " << name;
}

greet("Akrom");
```

* **parameter** → funksiya ichida
* **argument** → funksiya chaqirilganda

---

## 🔁 Default parameters

```cpp
void printAge(int age = 18) {
    cout << age;
}

printAge();    // 18
printAge(21);  // 21
```

---

## 🔄 Function Overloading

Bir xil nomli, lekin **har xil parametrli** funksiyalar.

```cpp
int sum(int a, int b) {
    return a + b;
}

double sum(double a, double b) {
    return a + b;
}
```

👉 C++ o‘zi mos funksiyani tanlaydi.

---

## 📍 Pass by Value vs Reference

### Pass by Value (nusxa)

```cpp
void change(int x) {
    x = 10;
}
```

### Pass by Reference (asl qiymat)

```cpp
void change(int &x) {
    x = 10;
}
```

👉 **Reference** real o‘zgaruvchini o‘zgartiradi.

---

## 🧠 Inline Functions

```cpp
inline int square(int x) {
    return x * x;
}
```

👉 Kichik funksiyalar uchun tezroq ishlaydi.

---

## ⚠️ Eng ko‘p uchraydigan xatolar

❌ Return unutish
❌ Type mos kelmasligi
❌ Parametr tartibini adashtirish

---

## 🧠 Xulosa

Funksiyalar:

* kodni qisqartiradi
* mantiqiy qiladi
* qayta ishlatiladi

C++ da **toza kod** funksiyalarsiz bo‘lmaydi.

---

➡️ Keyingi mavzu: **Recursion**

