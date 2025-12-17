# C++ Algoritmlari

C++ dagi ma’lumotlar tuzilmalari (vector, list, set va boshqalar) ma’lumotlarni saqlash va tartiblash uchun ishlatiladi.
Algoritmlar esa bu ma’lumotlar ustida **qidirish, tartiblash va o‘zgartirish** ishlarini bajaradi.

Algoritmlar `<algorithm>` kutubxonasi orqali ishlatiladi:

```cpp
#include <algorithm>
```

---

## 1. Tartiblash (Sorting)

Elementlarni tartiblash uchun **`sort()`** funksiyasi ishlatiladi.

```cpp
#include <vector>
#include <algorithm>
#include <iostream>
using namespace std;

int main() {
    vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};

    // Alfavit bo'yicha tartiblash
    sort(cars.begin(), cars.end());

    for (string car : cars) {
        cout << car << "\n";
    }
}
```

* Agar sonlar bo‘lsa, ularni raqamlar bo‘yicha tartiblaydi:

```cpp
vector<int> numbers = {1, 7, 3, 5, 9, 2};
sort(numbers.begin(), numbers.end());
```

* Teskari tartibda tartiblash uchun:

```cpp
sort(numbers.rbegin(), numbers.rend());
```

* Faqat ma’lum qismni tartiblash ham mumkin:

```cpp
sort(numbers.begin() + 3, numbers.end()); // 4-elementdan boshlab tartiblash
```

---

## 2. Qidirish (Searching)

* **`find()`** – berilgan qiymatni qidiradi:

```cpp
auto it = find(numbers.begin(), numbers.end(), 3);
```

* **`upper_bound()`** – berilgan qiymatdan katta birinchi elementni topadi (ma’lumot tartiblangan bo‘lishi kerak):

```cpp
sort(numbers.begin(), numbers.end());
auto it = upper_bound(numbers.begin(), numbers.end(), 5);
```

* Eng kichik va eng katta elementni topish:

```cpp
auto minIt = min_element(numbers.begin(), numbers.end());
auto maxIt = max_element(numbers.begin(), numbers.end());
```

---

## 3. O‘zgartirish (Modifying)

* Bir vectorni boshqasiga nusxalash:

```cpp
vector<int> copiedNumbers(6);
copy(numbers.begin(), numbers.end(), copiedNumbers.begin());
```

* Barcha elementlarni bir qiymat bilan to‘ldirish:

```cpp
vector<int> numbers(6);
fill(numbers.begin(), numbers.end(), 35);
```

---

## 4. Savol

**`sort()` funksiyasi nima qiladi?**

* Elementlarni standart bo‘yicha **o‘sish tartibida tartiblaydi** ✅
* Elementlarni kamayish tartibida tartiblaydi
* Ma’lum elementni qidiradi
* Elementlarni teskari qiladi

Bugunga Mavzular tugadi 😊

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
