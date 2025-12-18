# Queue (C++ STL)

## Queue nima?

**Queue** — bu C++ tilidagi ma’lumotlar tuzilmasi bo‘lib, elementlarni **FIFO** tamoyili asosida saqlaydi.

**FIFO (First In, First Out)** — birinchi qo‘shilgan element birinchi bo‘lib olinadi.

Tasavvur qilish uchun: **supermarketdagi navbat**ni o‘ylab ko‘ring 🛒

* Odamlar navbatning oxiriga turadi
* Birinchi kelgan odam birinchi bo‘lib xizmat oladi

Dasturlashda aynan shu tartib **Queue** deb ataladi.

---

## Queue xususiyatlari

* Elementlar **oxiridan (back)** qo‘shiladi
* Elementlar **boshidan (front)** o‘chiriladi
* Index orqali murojaat qilish **mavjud emas**
* Faqat `front` va `back` elementlar bilan ishlash mumkin

---

## Qachon queue ishlatiladi?

Queue quyidagi holatlarda juda foydali:

* Navbat asosida ishlaydigan tizimlar
* Printer queue
* Task / job scheduling
* BFS (Breadth First Search) algoritmi

---

## Queue’dan foydalanish

Queue ishlatish uchun `<queue>` header faylini qo‘shish kerak:

```cpp
#include <queue>
```

Agar `cout` ishlatilsa:

```cpp
#include <iostream>
using namespace std;
```

---

## Queue yaratish

```cpp
queue<string> cars;
```

> ⚠️ Eslatma: Queue e’lon qilingandan keyin uning ma’lumot turi (`int`, `string` va hokazo) **o‘zgarmaydi**.

> ⚠️ Muhim: Queue’ni vector kabi **boshlang‘ich qiymatlar bilan yaratib bo‘lmaydi** ❌

```cpp
// XATO
queue<string> cars = {"Volvo", "BMW"};
```

---

## Element qo‘shish — push()

Elementlar queue’ga **oxiridan (back)** qo‘shiladi:

```cpp
queue<string> cars;

cars.push("Volvo");
cars.push("BMW");
cars.push("Ford");
cars.push("Mazda");
```

Queue holati:

```
Volvo  ← front
BMW
Ford
Mazda  ← back
```

---

## Elementlarga murojaat qilish

Queue’da faqat **birinchi** va **oxirgi** elementlar bilan ishlash mumkin:

```cpp
cout << cars.front(); // Volvo (birinchi)
cout << cars.back();  // Mazda (oxirgi)
```

### Front va back elementlarni o‘zgartirish

```cpp
cars.front() = "Tesla";
cars.back()  = "VW";
```

---

## Element o‘chirish — pop()

`pop()` queue’dagi **birinchi elementni** o‘chiradi:

```cpp
cars.pop(); // Tesla o‘chiriladi

cout << cars.front(); // BMW
```

> ⚠️ Eslatma: `pop()` qiymat qaytarmaydi, faqat elementni o‘chiradi.

---

## Queue o‘lchami

### size()

Queue ichidagi elementlar sonini qaytaradi:

```cpp
cout << cars.size();
```

---

## Queue bo‘shligini tekshirish

### empty()

Queue bo‘sh bo‘lsa `true (1)`, aks holda `false (0)` qaytaradi:

```cpp
queue<string> cars;
cout << cars.empty(); // true
```

```cpp
cars.push("Volvo");
cout << cars.empty(); // false
```

---

## Time Complexity (Vaqt murakkabligi)

| Amal    | Murakkablik |
| ------- | ----------- |
| push()  | O(1)        |
| pop()   | O(1)        |
| front() | O(1)        |
| back()  | O(1)        |
| size()  | O(1)        |

---

## Queue va Stack farqi

* **Queue** — FIFO (First In, First Out)
* **Stack** — LIFO (Last In, First Out)

Ikkalasi ham real tizimlarda juda keng qo‘llaniladi.

---

## Xulosa

* Queue — navbat asosida ishlaydi
* Index mavjud emas
* Juda tez (O(1)) amallar
* Rejalashtirish va navbat tizimlari uchun ideal

Keyingi mavzu: [**Deque (Double-ended Queue)**](/CPP-Documentation/docs/data_structures/deques.html)

---

#### Menu:
- [**C++ Vectors**](/CPP-Documentation/docs/data_structures/vectors.html)
- [**C++ Stack**](/CPP-Documentation/docs/data_structures/stacks.html)
- [**C++ Queue**](/CPP-Documentation/docs/data_structures/queues.html)
- [**C++ Deque**](/CPP-Documentation/docs/data_structures/deques.html)
- [**C++ Set**](/CPP-Documentation/docs/data_structures/sets.html)
- [**C++ Map**](/CPP-Documentation/docs/data_structures/maps.html)
- [**C++ Iterators**](/CPP-Documentation/docs/data_structures/iterators.html)
- [**C++ Algorithms**](/CPP-Documentation/docs/data_structures/algorithms.html)
