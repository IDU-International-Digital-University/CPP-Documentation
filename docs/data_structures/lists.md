# List (C++ STL)

## List nima?

**List** — bu C++ tilidagi **bog‘langan ro‘yxat (linked list)** bo‘lib, bir xil turdagi bir nechta elementlarni saqlaydi va **dinamik o‘lchamga ega**.

List vector’ga o‘xshash, lekin ular orasida **ikki muhim farq** mavjud:

1. List’da elementlarni **boshidan ham, oxiridan ham** tez qo‘shish va o‘chirish mumkin.
2. List **index orqali murojaatni qo‘llab-quvvatlamaydi**, ya’ni `cars[0]` kabi murojaat qilib bo‘lmaydi.

Shu sababli list ko‘proq elementlar tez-tez qo‘shilib/o‘chiriladigan holatlarda ishlatiladi.

---

## Qachon list ishlatiladi?

List quyidagi vaziyatlarda qulay:

* Elementlarni boshidan va oxiridan tez o‘zgartirish kerak bo‘lsa
* Ma’lumotlar tez-tez qo‘shilib/o‘chirilsa
* Index orqali murojaat qilish muhim bo‘lmasa

Agar tez index access kerak bo‘lsa — **vector**, agar tez qo‘shish/o‘chirish kerak bo‘lsa — **list** tanlanadi.

---

## List’dan foydalanish

List ishlatish uchun `<list>` header faylini qo‘shish kerak:

```cpp
#include <list>
```

Agar `cout` ishlatilsa:

```cpp
#include <iostream>
using namespace std;
```

---

## List yaratish

### Bo‘sh list yaratish

```cpp
list<string> cars;
```

### Boshlang‘ich qiymatlar bilan yaratish

```cpp
list<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};

for (string car : cars) {
    cout << car << "\n";
}
```

> ⚠️ Eslatma: List e’lon qilingandan keyin uning ma’lumot turi (`int`, `string` va hokazo) **o‘zgarmaydi**.

---

## List elementlariga murojaat qilish

List’da **index mavjud emas**, shuning uchun elementlarga `[]` orqali murojaat qilib bo‘lmaydi.

Ammo birinchi va oxirgi elementlarni olish mumkin:

```cpp
cout << cars.front(); // Birinchi element
cout << cars.back();  // Oxirgi element
```

---

## List elementlarini o‘zgartirish

`.front()` va `.back()` orqali birinchi va oxirgi element qiymatini o‘zgartirish mumkin:

```cpp
cars.front() = "Opel";
cars.back()  = "Toyota";
```

---

## Element qo‘shish

### push_front()

List boshiga element qo‘shadi:

```cpp
cars.push_front("Tesla");
```

### push_back()

List oxiriga element qo‘shadi:

```cpp
cars.push_back("VW");
```

---

## Element o‘chirish

### pop_front()

List boshidan elementni o‘chiradi:

```cpp
cars.pop_front();
```

### pop_back()

List oxiridan elementni o‘chiradi:

```cpp
cars.pop_back();
```

---

## List o‘lchami

### size()

List ichidagi elementlar sonini qaytaradi:

```cpp
cout << cars.size();
```

---

## List bo‘shligini tekshirish

### empty()

List bo‘sh bo‘lsa `true`, aks holda `false` qaytaradi:

```cpp
list<string> cars;
cout << cars.empty(); // true (1)
```

```cpp
list<string> cars = {"Volvo", "BMW"};
cout << cars.empty(); // false (0)
```

---

## List bo‘ylab yurish (iteration)

List’da index bo‘lmagani uchun oddiy `for` loop ishlamaydi ❌

### Noto‘g‘ri usul (ishlamaydi)

```cpp
for (int i = 0; i < cars.size(); i++) {
    cout << cars[i]; // XATO
}
```

### To‘g‘ri usul — range-based for loop

```cpp
for (string car : cars) {
    cout << car << "\n";
}
```

> 💡 Eslatma: List’ni **iterator** yordamida ham aylanib chiqish mumkin (keyingi bo‘limlarda o‘rganiladi).

---

## Time Complexity (Vaqt murakkabligi)

| Amal                        | Murakkablik |
| --------------------------- | ----------- |
| Boshidan qo‘shish/o‘chirish | O(1)        |
| Oxiridan qo‘shish/o‘chirish | O(1)        |
| Index orqali murojaat       | Mavjud emas |
| Qidirish                    | O(n)        |

---

## Xulosa

* List — bog‘langan ro‘yxat
* Index orqali murojaat yo‘q
* Boshidan va oxiridan juda tez ishlaydi
* Tez-tez qo‘shish/o‘chirish talab qilinganda ideal

Keyingi mavzu: [**Stack (LIFO)**](/data_structures/stacks.md)
