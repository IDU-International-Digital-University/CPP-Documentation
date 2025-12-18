# Deque (C++ STL)

## Deque nima?

**Deque** — bu C++ tilidagi **ikki tomonlama navbat** (double-ended queue). U queue’ga o‘xshaydi, lekin ancha **moslashuvchan**:

* Elementlarni **boshidan ham, oxiridan ham** qo‘shish mumkin
* Elementlarni **boshidan ham, oxiridan ham** o‘chirish mumkin
* Elementlarga **index orqali murojaat qilish** mumkin

Ya’ni, deque — **vector + queue** imkoniyatlarini birlashtirgan data structure hisoblanadi.

---

## Qachon deque ishlatiladi?

Deque quyidagi holatlarda juda qulay:

* Boshidan ham, oxiridan ham tez ishlash kerak bo‘lsa
* Queue kabi ishlatish, lekin index access ham kerak bo‘lsa
* Sliding window algoritmlarida
* Performance muhim bo‘lgan real-time tizimlarda

---

## Deque’dan foydalanish

Deque ishlatish uchun `<deque>` header faylini qo‘shish kerak:

```cpp
#include <deque>
```

Agar `cout` ishlatilsa:

```cpp
#include <iostream>
using namespace std;
```

---

## Deque yaratish

### Bo‘sh deque yaratish

```cpp
deque<string> cars;
```

### Boshlang‘ich qiymatlar bilan yaratish

```cpp
deque<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};

for (string car : cars) {
    cout << car << "\n";
}
```

> ⚠️ Eslatma: Deque e’lon qilingandan keyin uning ma’lumot turi (`int`, `string` va hokazo) **o‘zgarmaydi**.

---

## Deque elementlariga murojaat qilish

Deque elementlari **0-indexed** hisoblanadi:

```cpp
cout << cars[0]; // Volvo
cout << cars[1]; // BMW
```

### front() va back()

```cpp
cout << cars.front(); // Birinchi element
cout << cars.back();  // Oxirgi element
```

### at() funksiyasi (xavfsizroq)

```cpp
cout << cars.at(1); // BMW
cout << cars.at(2); // Ford
```

Agar mavjud bo‘lmagan index ko‘rsatilsa:

```cpp
cout << cars.at(6); // out_of_range xato
```

---

## Deque elementlarini o‘zgartirish

### Index orqali

```cpp
cars[0] = "Opel";
```

### at() orqali (tavsiya etiladi)

```cpp
cars.at(0) = "Opel";
```

---

## Element qo‘shish

### push_front()

```cpp
cars.push_front("Tesla");
```

### push_back()

```cpp
cars.push_back("VW");
```

---

## Element o‘chirish

### pop_front()

```cpp
cars.pop_front();
```

### pop_back()

```cpp
cars.pop_back();
```

---

## Deque o‘lchami

### size()

```cpp
cout << cars.size();
```

---

## Deque bo‘shligini tekshirish

### empty()

```cpp
deque<string> cars;
cout << cars.empty(); // true
```

```cpp
deque<string> cars = {"Volvo", "BMW"};
cout << cars.empty(); // false
```

---

## Deque bo‘ylab yurish (iteration)

### Oddiy for loop

```cpp
for (int i = 0; i < cars.size(); i++) {
    cout << cars[i] << "\n";
}
```

### range-based for loop (tavsiya etiladi)

```cpp
for (string car : cars) {
    cout << car << "\n";
}
```

> 💡 Eslatma: Deque’ni **iterator** yordamida ham aylanib chiqish mumkin.

---

## Time Complexity (Vaqt murakkabligi)

| Amal         | Murakkablik |
| ------------ | ----------- |
| push_front() | O(1)        |
| push_back()  | O(1)        |
| pop_front()  | O(1)        |
| pop_back()   | O(1)        |
| Index access | O(1)        |

---

## Deque vs Vector vs Queue

* **Vector** — oxiridan tez, boshidan sekin
* **Queue** — FIFO, index yo‘q
* **Deque** — ikki tomondan tez + index mavjud

---

## Xulosa

* Deque — juda moslashuvchan data structure
* Boshidan ham, oxiridan ham tez ishlaydi
* Index orqali murojaat qilish mumkin
* Murakkab algoritmlar uchun juda qulay

Keyingi mavzu: [**Set (Unique elements)**](/docs/data_structures/sets.md)

---

#### Menu:
- [**C++ Vectors**](/docs/data_structures/vectors.md)
- [**C++ Lists**](/docs/data_structures/lists.md)
- [**C++ Stack**](/docs/data_structures/stacks.md)
- [**C++ Queue**](/docs/data_structures/queues.md)
- [**C++ Set**](/docs/data_structures/sets.md)
- [**C++ Map**](/docs/data_structures/maps.md)
- [**C++ Iterators**](/docs/data_structures/iterators.md)
- [**C++ Algorithms**](/docs/data_structures/algorithms.md)
