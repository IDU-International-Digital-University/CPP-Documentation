# Map (C++ STL)

## Map nima?

**Map** — bu C++ data structure bo‘lib, **key/value (kalit/qiymat) juftliklarini** saqlaydi.

* Elementlarga **faqat key orqali** murojaat qilinadi, index orqali yo‘q
* Har bir key **unique** (takrorlanmas)
* Elementlar **key bo‘yicha avtomatik tartiblanadi** (default: o‘sish tartibi)

```cpp
#include <map>
#include <iostream>
using namespace std;
```

---

## Map yaratish

### Bo‘sh map

```cpp
map<string, int> people;
```

### Boshlang‘ich qiymatlar bilan

```cpp
map<string, int> people = { {"John", 32}, {"Adele", 45}, {"Bo", 29} };
```

---

## Map elementlariga murojaat qilish

### Index yo‘q, key orqali

```cpp
cout << people["John"] << "\n";
cout << people.at("Adele") << "\n";
```

> .at() tavsiya qilinadi, chunki mavjud bo‘lmagan key xatolik beradi.

### Value o‘zgartirish

```cpp
people["John"] = 50;
people.at("John") = 50;
```

---

## Element qo‘shish

```cpp
people["Jenny"] = 22;
people.insert({"Liam", 24});
```

> Key unique bo‘lishi kerak. Duplicate key qo‘shish rad etiladi.

---

## Element o‘chirish

```cpp
people.erase("John"); // bitta element
people.clear();          // barcha elementlar
```

---

## Map o‘lchami

```cpp
cout << people.size();
```

## Bo‘shligini tekshirish

```cpp
cout << people.empty(); // 1 = bo‘sh, 0 = bo‘sh emas
```

### Key mavjudligini tekshirish

```cpp
cout << people.count("John"); // 1 = mavjud, 0 = yo‘q
```

---

## Map bo‘ylab yurish (iteration)

### range-based for loop

```cpp
for (auto person : people) {
    cout << person.first << " is: " << person.second << "\n";
}
```

* `first` → key
* `second` → value

### Kamayish tartibida

```cpp
map<string, int, greater<string>> people;
```

> Elementlar key bo‘yicha kamayish tartibida chiqariladi.

---

## Xulosa

* Map — **key/value** saqlash uchun
* Key unique va **avtomatik tartiblangan**
* Index orqali murojaat yo‘q, faqat key orqali
* `.insert()`, `[]`, `.erase()`, `.clear()`, `.size()`, `.empty()`, `.count()` funksiyalari mavjud
* Algoritmik masalalar va look-uplar uchun qulay

Keyingi mavzu: [**Iterators**](/data_structures/iterators.md)

---

#### Menu:
- [**C++ Vectors**](/data_structures/vectors.md)
- [**C++ Lists**](/data_structures/lists.md)
- [**C++ Stack**](/data_structures/stacks.md)
- [**C++ Queue**](/data_structures/queues.md)
- [**C++ Deque**](/data_structures/deques.md)
- [**C++ Set**](/data_structures/sets.md)
- [**C++ Map**](/data_structures/maps.md)
- [**C++ Iterators**](/data_structures/iterators.md)
- [**C++ Algorithms**](/data_structures/algorithms.md)
