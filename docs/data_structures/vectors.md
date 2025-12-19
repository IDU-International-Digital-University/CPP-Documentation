# Vector (C++ STL)

## Vector nima?

**Vector** — bu C++ tilidagi **dinamik massiv** (resizable array). U oddiy array (massiv) kabi bir xil turdagi bir nechta elementlarni saqlaydi, lekin asosiy ustunligi shundaki, vector o‘lchami dastur ishlashi davomida **avtomatik ravishda o‘zgarishi** mumkin.

Ya’ni:

* Array’da o‘lcham oldindan belgilanadi va o‘zgarmaydi
* Vector’da esa element qo‘shish yoki o‘chirish mumkin

Shu sababli, real loyihalarda ko‘pincha array o‘rniga **vector** ishlatiladi.

---

## Qachon vector ishlatiladi?

Vector quyidagi holatlarda juda qulay:

* Elementlar soni oldindan aniq bo‘lmaganda
* Ma’lumotlar ketma-ket saqlanishi kerak bo‘lsa
* Index orqali tez murojaat qilish kerak bo‘lsa
* Oxiridan tez qo‘shish/o‘chirish talab qilinsa

---

## Vector’dan foydalanish

Vector ishlatish uchun `<vector>` header faylini qo‘shish kerak:

```cpp
#include <vector>
```

Agar `cout` ishlatilsa:

```cpp
#include <iostream>
using namespace std;
```

---

## Vector yaratish

### Bo‘sh vector yaratish

```cpp
vector<int> numbers;
```

Bu yerda `numbers` — butun sonlardan iborat bo‘sh vector.

### Boshlang‘ich qiymatlar bilan yaratish

```cpp
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};
```

> ⚠️ Eslatma: Vector e’lon qilingandan keyin uning ma’lumot turi (`int`, `string` va hokazo) **o‘zgarmaydi**.

---

## Vector elementlariga murojaat qilish

Vector elementlari **0-indexed**, ya’ni birinchi element indexi `0` bo‘ladi.

```cpp
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};

cout << cars[0]; // Volvo
cout << cars[1]; // BMW
```

### at() funksiyasi

`.at()` funksiyasi elementga **xavfsizroq** murojaat qilish imkonini beradi:

```cpp
cout << cars.at(2); // Ford
```

Agar mavjud bo‘lmagan index ko‘rsatilsa, dastur xato (exception) chiqaradi:

```cpp
cout << cars.at(6); // out_of_range xato
```

Shu sababli `.at()` funksiyasi `[]` ga nisbatan ishonchliroq hisoblanadi.

---

## front() va back()

Vector’ning birinchi va oxirgi elementlarini olish uchun:

```cpp
cout << cars.front(); // Birinchi element
cout << cars.back();  // Oxirgi element
```

---

## Element qo‘shish va o‘chirish

### push_back()

Vector oxiriga element qo‘shadi:

```cpp
vector<int> nums;
nums.push_back(10);
nums.push_back(20);
nums.push_back(30);
```

### pop_back()

Vector oxiridan elementni o‘chiradi:

```cpp
nums.pop_back(); // 30 o‘chiriladi
```

---

## Vector o‘lchami

### size()

Vector ichidagi elementlar sonini qaytaradi:

```cpp
cout << nums.size();
```

### empty()

Vector bo‘sh yoki yo‘qligini tekshiradi:

```cpp
if (nums.empty()) {
    cout << "Vector bo‘sh";
}
```

---

## Vector bo‘ylab yurish (iteration)

### range-based for loop

```cpp
for (int x : nums) {
    cout << x << " ";
}
```

### oddiy for loop

```cpp
for (int i = 0; i < nums.size(); i++) {
    cout << nums[i] << " ";
}
```

---

## Time Complexity (Vaqt murakkabligi)

| Amal                          | Murakkablik   |
| ----------------------------- | ------------- |
| Index orqali murojaat         | O(1)          |
| Oxiridan qo‘shish (push_back) | O(1) (odatda) |
| Oxiridan o‘chirish (pop_back) | O(1)          |
| O‘rtadan qo‘shish/o‘chirish   | O(n)          |

---

## Xulosa

* Vector — C++ dagi eng ko‘p ishlatiladigan data structure
* Dinamik o‘lchamga ega
* Index orqali tez ishlaydi
* Katta loyihalar uchun juda qulay

Keyingi mavzu: [**List (Linked List)**](./lists.md)
