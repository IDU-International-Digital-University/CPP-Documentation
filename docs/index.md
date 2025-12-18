# C++ Data Structures and STL

## Kirish (Introduction)

Ushbu repository **C++ dasturlash tilidagi Data Structures (Ma’lumotlar tuzilmalari)** va **STL (Standard Template Library)** mavzularini tushunarli va amaliy tarzda o‘rganish uchun mo‘ljallangan.

Ma’lumotlar tuzilmalari — bu ma’lumotlarni xotirada saqlash va tartibli holda boshqarish usullaridir. Masalan, **array (massiv)** bitta o‘zgaruvchi ichida bir nechta elementlarni saqlash imkonini beradigan eng oddiy data structure hisoblanadi.

C++ tilida array’dan tashqari yana ko‘plab ma’lumotlar tuzilmalari mavjud bo‘lib, ularning aksariyati **STL (Standard Template Library)** tarkibiga kiradi. Har bir data structure ma’lumotlar bilan ishlashning turli holatlari uchun moslashtirilgan.

## C++ STL nima?

**STL (Standard Template Library)** — bu C++ tilidagi tayyor **data structures (containers)** va **algoritmlar** to‘plamidir. STL yordamida ma’lumotlarni samarali saqlash, qidirish, saralash va qayta ishlash mumkin.

Agar data structures ma’lumotlarni saqlash uchun xizmat qilsa, **algoritmlar** ushbu ma’lumotlar ustida turli amallarni bajarish uchun ishlatiladi (masalan: qidirish, saralash, o‘chirish).

To‘g‘ri tanlangan data structure va algoritm:

* Dastur tezroq ishlashini ta’minlaydi
* Katta hajmdagi ma’lumotlar bilan samarali ishlashga yordam beradi
* Kodni soddaroq va tushunarliroq qiladi

## Eng ko‘p ishlatiladigan STL Data Structures

| Data Structure | Tavsif                                                                                                                                             |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Vector**     | Massivga o‘xshash, lekin o‘lchami dinamik. Elementlar odatda oxiridan qo‘shiladi va o‘chiriladi. Index orqali murojaat qilish mumkin.              |
| **List**       | Ketma-ket bog‘langan elementlardan iborat. Elementlar boshidan va oxiridan qo‘shilishi/o‘chirilishi mumkin. Index orqali murojaat qilib bo‘lmaydi. |
| **Stack**      | LIFO (Last In, First Out) tamoyiliga asoslangan. Elementlar faqat yuqorisidan qo‘shiladi va olinadi.                                               |
| **Queue**      | FIFO (First In, First Out) tamoyiliga asoslangan. Elementlar oxiridan qo‘shilib, boshidan olinadi.                                                 |
| **Deque**      | Ikki tomonlama queue. Elementlarni boshidan ham, oxiridan ham qo‘shish va o‘chirish mumkin. Index orqali murojaat qilish mumkin.                   |
| **Set**        | Faqat noyob (unique) elementlarni saqlaydi. Index mavjud emas.                                                                                     |
| **Map**        | `key/value` (kalit/qiymat) juftliklarini saqlaydi. Elementlarga key orqali murojaat qilinadi.                                                      |

Qaysi data structure’ni tanlash — sizning vazifangizga bog‘liq.

## STL dan foydalanish

Har bir data structure’dan foydalanish uchun mos **header file** ni qo‘shish kerak:

```cpp
#include <vector>
#include <list>
#include <set>
#include <map>
#include <stack>
#include <queue>
```

### Vector misoli

```cpp
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};

    for (string car : cars) {
        cout << car << "\n";
    }
    return 0;
}
```

## STL ning asosiy tushunchalari

STL uchta asosiy komponentdan iborat:

* **Containers** — ma’lumotlarni saqlash uchun (vector, list, map, va hokazo)
* **Iterators** — container ichidagi elementlarga murojaat qilish uchun
* **Algorithms** — ma’lumotlar ustida amallar bajarish uchun (`sort()`, `find()` va boshqalar)

Kompyuter fanida **Data Structures va Algorithms** doimo birga ishlaydi. Data structure algoritmlarsiz foydasiz, algoritmlar esa data structure’siz ishlay olmaydi.

Keyingi bo‘limlarda har bir data structure alohida ko‘rib chiqilib, amaliy misollar bilan tushuntiriladi.
