# C++ Syntax and Data Types

![Topic](https://img.shields.io/badge/Topic-C%2B%2B%20Basics-blue)
![Level](https://img.shields.io/badge/Level-Beginner-green)

---

## 📌 Kirish

Bu bo‘limda **C++ dasturlash tilining sintaksisi** va **asosiy ma’lumot turlari (data types)** bilan tanishamiz.

Sintaksis — bu:
- C++ da **qanday yozish kerak**
- qaysi qoidalar asosida kod ishlashi

Agar sintaksis va data types yaxshi o‘zlashtirilsa:
- xatolar (errors) kamayadi
- kod tushunarli bo‘ladi
- keyingi mavzular osonroq o‘rganiladi

---

## 🧱 C++ dastur tuzilishi

Oddiy C++ dastur tuzilishi quyidagicha:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello C++" << endl;
    return 0;
}
````

### Asosiy qismlar

| Qism                  | Tavsif                |
| --------------------- | --------------------- |
| `#include`            | Kutubxonani ulash     |
| `using namespace std` | `std` ni qisqartirish |
| `int main()`          | Dastur boshlanishi    |
| `{ }`                 | Kod bloklari          |
| `;`                   | Buyruq tugashi        |

---

## ✍️ Kommentlar (Comments)

Kommentlar kodni tushuntirish uchun ishlatiladi va **kompilyator tomonidan o‘qilmaydi**.

```cpp
// Bu bir qatorli komment

/*
   Bu ko‘p qatorli komment
*/
```

👉 Yaxshi komment — yaxshi kod belgisi.

---

## 📦 O‘zgaruvchilar (Variables)

O‘zgaruvchi — bu **xotirada saqlanadigan qiymat**.

### Sintaksis:

```cpp
data_type variable_name = value;
```

### Misol:

```cpp
int age = 20;
double price = 15.5;
char grade = 'A';
```

---

## 🔢 Asosiy Data Types

### 1️⃣ Butun sonlar

```cpp
int x = 10;
long y = 100000;
short z = 5;
```

| Type    | Hajmi    | Tavsif               |
| ------- | -------- | -------------------- |
| `int`   | 4 byte   | Eng ko‘p ishlatiladi |
| `short` | 2 byte   | Kichik sonlar        |
| `long`  | 4/8 byte | Katta sonlar         |

---

### 2️⃣ O‘nli sonlar (Floating point)

```cpp
float pi = 3.14f;
double salary = 4500.75;
```

| Type     | Aniqlik |
| -------- | ------- |
| `float`  | Kam     |
| `double` | Yuqori  |

👉 Amaliyotda ko‘proq `double` ishlatiladi.

---

### 3️⃣ Belgilar (Character)

```cpp
char letter = 'A';
```

❗ `char` **bitta belgi** saqlaydi va **' '** bilan yoziladi.

---

### 4️⃣ Mantiqiy (Boolean)

```cpp
bool isPassed = true;
bool isFailed = false;
```

`bool` faqat:

* `true`
* `false`

qiymatlarni oladi.

---

## 🧵 String (Matn)

C++ da matn bilan ishlash uchun `string` ishlatiladi.

```cpp
#include <string>

string name = "Akrom";
```

👉 `string` — STL qismi.

---

## 🔁 Konstantalar (Constants)

Qiymati o‘zgarmaydigan o‘zgaruvchilar.

```cpp
const double PI = 3.14159;
```

❗ `PI` keyin o‘zgartirilmaydi.

---

## 🔄 Type Casting

Bir data type’ni boshqasiga o‘tkazish.

```cpp
int x = 10;
double y = (double)x;
```

Yoki zamonaviy usul:

```cpp
double y = static_cast<double>(x);
```

---

## 📥 Input / Output

### Input (`cin`)

```cpp
int age;
cin >> age;
```

### Output (`cout`)

```cpp
cout << "Age: " << age << endl;
```

---

## ⚠️ Eng ko‘p uchraydigan xatolar

❌ Semicolon unutish:

```cpp
int x = 5   // xato
```

❌ Noto‘g‘ri type:

```cpp
int x = 3.5; // ma’lumot yo‘qoladi
```

❌ `char` noto‘g‘ri yozish:

```cpp
char c = "A"; // xato
```

---

## 🧠 Xulosa

Bu bo‘limda siz:

* C++ sintaksisini
* asosiy data types’ni
* input/output’ni

o‘rgandingiz.

Bu bilimlar **butun C++** uchun juda muhim.
