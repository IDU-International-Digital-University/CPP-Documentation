# Stack (C++ STL)

## Stack nima?

**Stack** — bu C++ tilidagi ma’lumotlar tuzilmasi bo‘lib, elementlarni **LIFO** tamoyili asosida saqlaydi.

**LIFO (Last In, First Out)** — oxirgi qo‘shilgan element birinchi bo‘lib olinadi.

Tasavvur qilish uchun: **pankeyklar (blinchiklar) uyumi**ni o‘ylab ko‘ring 🍽️

* Pankeyk faqat tepadan qo‘shiladi
* Pankeyk faqat tepadan olinadi
* Oxirgi qo‘shilgan pankeyk — birinchi olinadi

Dasturlashda aynan shu tamoyil **Stack** deb ataladi.

---

## Stack xususiyatlari

* Elementlar **faqat tepadan (top)** qo‘shiladi
* Elementlar **faqat tepadan (top)** o‘chiriladi
* Index orqali murojaat qilish **mavjud emas**
* Faqat eng yuqori (top) element bilan ishlash mumkin

---

## Qachon stack ishlatiladi?

Stack quyidagi holatlarda juda foydali:

* Funksiya chaqiruvlari (call stack)
* Undo / Redo mexanizmlari
* Qavslarni tekshirish ((), {}, [])
* Backtracking algoritmlari

---

## Stack’dan foydalanish

Stack ishlatish uchun `<stack>` header faylini qo‘shish kerak:

```cpp
#include <stack>
```

Agar `cout` ishlatilsa:

```cpp
#include <iostream>
using namespace std;
```

---

## Stack yaratish

```cpp
stack<string> cars;
```

> ⚠️ Eslatma: Stack e’lon qilingandan keyin uning ma’lumot turi (`int`, `string` va hokazo) **o‘zgarmaydi**.

> ⚠️ Muhim: Stack’ni vector kabi **boshlang‘ich qiymatlar bilan yaratib bo‘lmaydi** ❌

```cpp
// XATO
stack<string> cars = {"Volvo", "BMW"};
```

---

## Element qo‘shish — push()

Elementlar stack’ga **faqat tepadan** qo‘shiladi:

```cpp
stack<string> cars;

cars.push("Volvo");
cars.push("BMW");
cars.push("Ford");
cars.push("Mazda");
```

Stack holati:

```
Mazda  ← top
Ford
BMW
Volvo
```

---

## Top elementga murojaat qilish — top()

Stack’da faqat **eng yuqori element** bilan ishlash mumkin:

```cpp
cout << cars.top(); // Mazda
```

### Top elementni o‘zgartirish

```cpp
cars.top() = "Tesla";
cout << cars.top(); // Tesla
```

---

## Element o‘chirish — pop()

`pop()` oxirgi qo‘shilgan elementni olib tashlaydi:

```cpp
cars.pop(); // Tesla o‘chiriladi

cout << cars.top(); // Ford
```

> ⚠️ Eslatma: `pop()` hech narsa qaytarmaydi, faqat elementni o‘chiradi.

---

## Stack o‘lchami

### size()

Stack ichidagi elementlar sonini qaytaradi:

```cpp
cout << cars.size();
```

---

## Stack bo‘shligini tekshirish

### empty()

Stack bo‘sh bo‘lsa `true (1)`, aks holda `false (0)` qaytaradi:

```cpp
stack<string> cars;
cout << cars.empty(); // true
```

```cpp
cars.push("Volvo");
cout << cars.empty(); // false
```

---

## Time Complexity (Vaqt murakkabligi)

| Amal   | Murakkablik |
| ------ | ----------- |
| push() | O(1)        |
| pop()  | O(1)        |
| top()  | O(1)        |
| size() | O(1)        |

---

## Stack va Queue farqi

* **Stack** — LIFO (Last In, First Out)
* **Queue** — FIFO (First In, First Out)

Stack va Queue ko‘pincha birga o‘rganiladi.

---

## Xulosa

* Stack — LIFO asosida ishlaydi
* Faqat top element bilan ishlash mumkin
* Juda tez (O(1))
* Algoritmlar va real tizimlarda keng qo‘llaniladi

Keyingi mavzu: [**Queue (FIFO)**](/docs/data_structures/queues.md)

---

#### Menu:
- [**C++ Vectors**](/docs/data_structures/vectors.md)
- [**C++ Lists**](/docs/data_structures/lists.md)
- [**C++ Stack**](/docs/data_structures/stacks.md)
- [**C++ Queue**](/docs/data_structures/queues.md)
- [**C++ Deque**](/docs/data_structures/deques.md)
- [**C++ Set**](/docs/data_structures/sets.md)
- [**C++ Map**](/docs/data_structures/maps.md)
- [**C++ Iterators**](/docs/data_structures/iterators.md)
- [**C++ Algorithms**](/docs/data_structures/algorithms.md)
