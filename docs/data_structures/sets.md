# Set (C++ STL)

## Set nima?

**Set** — bu C++ tilidagi data structure bo‘lib, **unique (takrorlanmas) elementlarni** saqlaydi.

* Elementlar **avtomatik tartiblanadi** (default: o‘sish tartibi)
* Takroriy qiymatlar **rad etiladi**
* Elementlarni qo‘shish yoki o‘chirish mumkin, lekin mavjud qiymatni o‘zgartirish **mumkin emas**
* Index orqali murojaat qilish **yo‘q**, chunki tartib avtomatik hisoblanadi

```cpp
#include <set>
#include <iostream>
using namespace std;
```

---

## Set yaratish

```cpp
set<string> cars;
```

### Boshlang‘ich qiymatlar bilan

```cpp
set<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (string car : cars) {
    cout << car << "\n";
}
```

**Natija:**

```
BMW
Ford
Mazda
Volvo
```

> Elementlar avtomatik alfabet tartibida chiqadi.

### Integer set misoli

```cpp
set<int> numbers = {1, 7, 3, 2, 5, 9};
for (int num : numbers) {
    cout << num << "\n";
}
```

**Natija:** 1 2 3 5 7 9

---

## Setni kamayish tartibida yaratish

```cpp
set<int, greater<int>> numbers = {1, 7, 3, 2, 5, 9};
for (int num : numbers) {
    cout << num << "\n";
}
```

**Natija:** 9 7 5 3 2 1

---

## Unique elements

```cpp
set<string> cars = {"Volvo", "BMW", "Ford", "BMW", "Mazda"};
for (string car : cars) {
    cout << car << "\n";
}
```

**Natija:** BMW Ford Mazda Volvo

> Takroriy elementlar avtomatik rad etiladi.

---

## Element qo‘shish

```cpp
cars.insert("Tesla");
cars.insert("VW");
cars.insert("Toyota");
cars.insert("Audi");
```

## Element o‘chirish

```cpp
cars.erase("Volvo");
cars.erase("Mazda");
```

### Hammasini o‘chirish

```cpp
cars.clear();
```

---

## Set o‘lchami

```cpp
cout << cars.size(); // elementlar soni
```

## Bo‘shligini tekshirish

```cpp
cout << cars.empty(); // 1 = bo‘sh, 0 = bo‘sh emas
```

---

## Set bo‘ylab yurish (iteration)

```cpp
for (string car : cars) {
    cout << car << "\n";
}
```

> Eslatma: Iterator yordamida ham yurish mumkin.

---

## Xulosa

* Set — faqat **unique elementlar** saqlaydi
* Avtomatik **tartiblanadi**
* Index yo‘q, lekin elementlarni qo‘shish va o‘chirish tez
* Algoritmlar va matematik hisob-kitoblar uchun qulay

Keyingi mavzu: [**Map (STL)**](/docs/data_structures/maps.md)

---

#### Menu:
- [**C++ Vectors**](/docs/data_structures/vectors.md)
- [**C++ Stack**](/docs/data_structures/stacks.md)
- [**C++ Queue**](/docs/data_structures/queues.md)
- [**C++ Deque**](/docs/data_structures/deques.md)
- [**C++ Set**](/docs/data_structures/sets.md)
- [**C++ Map**](/docs/data_structures/maps.md)
- [**C++ Iterators**](/docs/data_structures/iterators.md)
- [**C++ Algorithms**](/docs/data_structures/algorithms.md)
