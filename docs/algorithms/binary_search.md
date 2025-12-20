# Binary Search Algorithm

## Binary Search nima?

**Binary Search (Ikkilik qidiruv)** — bu **faqat tartiblangan (sorted)** ma’lumotlarda ishlaydigan **tez va samarali** qidiruv algoritmidir.

Agar ma’lumotlar tartiblangan bo‘lsa, Binary Search:
- elementni juda tez topadi
- Linear Search’dan ancha tez ishlaydi

---

## Muhim shart ❗

> **Binary Search faqat SORTED (tartiblangan) massivda ishlaydi**

Masalan:
```text
✅ To‘g‘ri:   [1, 3, 5, 7, 9, 11]
❌ Noto‘g‘ri: [7, 1, 9, 3, 5]
```

Agar data tartiblanmagan bo‘lsa — **oldin sort qilish kerak**.

---

## Qanday ishlaydi? (Oddiy tushuntirish)

1. Massivning **o‘rtasidagi element** olinadi
2. Qidirilayotgan qiymat bilan solishtiriladi
3. Agar:

   * teng bo‘lsa → topildi
   * kichik bo‘lsa → chap tomondan qidiriladi
   * katta bo‘lsa → o‘ng tomondan qidiriladi
4. Shu jarayon element topilguncha yoki qidiruv oralig‘i tugaguncha davom etadi

---

## Vizual misol 👀

```text
Massiv: [1, 3, 5, 7, 9, 11]
Target: 7

1-qadam: middle = 5
5 < 7 → o‘ng tomonga o‘tamiz

2-qadam: middle = 7
Topildi ✅
```

---

## Oddiy C++ misol (while loop bilan)

```cpp
#include <iostream>
using namespace std;

int binarySearch(int arr[], int size, int target) {
    int left = 0;
    int right = size - 1;

    while (left <= right) {
        int mid = left + (right - left) / 2;

        if (arr[mid] == target)
            return mid;

        if (arr[mid] < target)
            left = mid + 1;
        else
            right = mid - 1;
    }

    return -1; // topilmasa
}

int main() {
    int arr[] = {1, 3, 5, 7, 9, 11};
    int index = binarySearch(arr, 6, 7);

    cout << index; // 3
}
```

---

## Binary Search qanday ishlaydi (real hayot misoli)

📖 **Lug‘at (dictionary)** misoli:

* Agar “apple” so‘zini qidirsang:

  * boshidan o‘qimaysan
  * o‘rtasidan ochasan
  * keyin chap yoki o‘ng tomonga o‘tasan

Bu aynan **Binary Search** printsipi.

---

## STL bilan Binary Search (C++ da)

C++ da tayyor funksiyalar bor:

### 1️⃣ `binary_search()`

```cpp
#include <algorithm>
#include <vector>

vector<int> numbers = {1, 3, 5, 7, 9};

bool found = binary_search(numbers.begin(), numbers.end(), 7);
```

📌 **true / false** qaytaradi

---

### 2️⃣ `lower_bound()` (juda muhim 🔥)

```cpp
auto it = lower_bound(numbers.begin(), numbers.end(), 7);

if (it != numbers.end())
    cout << *it;
```

* Qidirilgan qiymatga **teng yoki undan katta** birinchi elementni qaytaradi
* Competitive programming va interviewlarda ko‘p ishlatiladi

---

## Afzalliklari ✅

* Juda tez ishlaydi
* Katta massivlar uchun ideal
* Logarithmic murakkablik

---

## Kamchiliklari ❌

* Faqat sorted data’da ishlaydi
* Oldin sort qilish kerak bo‘lishi mumkin

---

## Time Complexity (Vaqt murakkabligi)

| Holat      | Murakkablik |
| ---------- | ----------- |
| Best case  | O(1)        |
| Worst case | O(log n)    |
| Average    | O(log n)    |

---

## Linear Search vs Binary Search

| Xususiyat            | Linear | Binary   |
| -------------------- | ------ | -------- |
| Data sorted bo‘lishi | ❌      | ✅        |
| Tezligi              | Sekin  | Juda tez |
| Murakkablik          | O(n)   | O(log n) |

---

## Qachon Binary Search ishlatish kerak?

✅ Agar:

* ma’lumotlar sorted bo‘lsa
* katta massiv bo‘lsa
* tez qidiruv kerak bo‘lsa

❌ Agar:

* data tartiblanmagan bo‘lsa
* juda kichik massiv bo‘lsa

---

## Xulosa 🧠

Binary Search — bu:

* **oddiy**
* **tez**
* **interview’larda juda muhim**

Agar Binary Search’ni yaxshi tushunsang:
➡️ `lower_bound`
➡️ `upper_bound`
➡️ interval search’lar oson bo‘ladi 🚀
