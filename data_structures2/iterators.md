# C++ Iterators

Iteratorlar ma'lumotlar tuzilmalaridagi (vector, list, set va hokazo) elementlarga murojaat qilish va ularni aylanib chiqish uchun ishlatiladi. "Iterator" deb atalishi shundan, chunki bu texnik atama "loop" qilish uchun ishlatiladi.

## Iteratorni ishlatish

Vector misolida:

```cpp
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};
    vector<string>::iterator it;

    for (it = cars.begin(); it != cars.end(); ++it) {
        cout << *it << "\n";
    }
    return 0;
}
```

* `begin()` birinchi elementni ko'rsatadi.
* `end()` oxirgi elementdan keyingi pozitsiyani ko'rsatadi.
* `*it` element qiymatini olish uchun ishlatiladi.
* `auto` kaliti turini avtomatik aniqlaydi, shuning uchun iteratordan foydalanish soddalashadi.

## For-each loop vs Iterator

* Agar elementlarni faqat o'qish kerak bo'lsa, for-each loop qulay:

```cpp
for (string car : cars) {
    cout << car << "\n";
}
```

* Agar elementlarni o'zgartirish, o'chirish yoki teskari tartibda aylanib chiqish kerak bo'lsa, iterator ishlatish kerak.

## Teskari aylanish

`rbegin()` va `rend()` funksiyalari yordamida:

```cpp
for (auto it = cars.rbegin(); it != cars.rend(); ++it) {
    cout << *it << "\n";
}
```

## Boshqa ma'lumotlar tuzilmalarida iteratsiya

Vector, list, deque, set, map iterators bilan ishlaydi. Stack va queue esa yo'q.

Map misoli:

```cpp
map<string,int> people = { {"John",32}, {"Adele",45}, {"Bo",29} };
for (auto it = people.begin(); it != people.end(); ++it) {
    cout << it->first << " is: " << it->second << "\n";
}
```

## Algorithm bilan ishlatish

Iteratorlar `sort()`, `find()` kabi algoritmlarda ham ishlatiladi:

```cpp
sort(cars.begin(), cars.end()); // alfavit bo'yicha tartiblash
sort(numbers.begin(), numbers.end()); // raqamlar bo'yicha tartiblash
sort(numbers.rbegin(), numbers.rend()); // teskari tartiblash
```

Iteratorlar STL ma'lumotlar tuzilmalarini qulay va samarali boshqarish imkonini beradi.

Keyingi mavzu: [**Algorithms**](/docs/data_structures/algorithms.md)

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
