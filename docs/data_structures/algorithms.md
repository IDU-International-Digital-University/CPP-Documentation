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
- [**C++ Vectors**](/docs/data_structures/vectors.html)
- [**C++ Stack**](/docs/data_structures/stacks.html)
- [**C++ Queue**](/docs/data_structures/queues.html)
- [**C++ Deque**](/docs/data_structures/deques.html)
- [**C++ Set**](/docs/data_structures/sets.html)
- [**C++ Map**](/docs/data_structures/maps.html)
- [**C++ Iterators**](/docs/data_structures/iterators.html)
- [**C++ Algorithms**](/docs/data_structures/algorithms.html)
