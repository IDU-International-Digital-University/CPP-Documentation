# Linear Search Algorithm

## Linear Search nima?

**Linear Search (chiziqli qidiruv)** — bu elementni **boshidan oxirigacha ketma-ket tekshirib** topadigan eng **oddiy qidiruv algoritmi**.

Bu algoritm:
- massiv (array)
- vector
- list  
kabi barcha ma’lumot tuzilmalarida ishlaydi.

---

## Qachon ishlaydi?

Linear Search:
- **tartiblangan (sorted)** data’da ham
- **tartiblanmagan (unsorted)** data’da ham  
ishlaydi.

❗ Shuning uchun u **eng universal**, lekin **eng sekin** algoritmlardan biridir.

---

## Qanday ishlaydi? (Oddiy tushuntirish)

1. Birinchi elementdan boshlaydi
2. Har bir elementni qidirilayotgan qiymat bilan solishtiradi
3. Agar teng bo‘lsa → **topildi**
4. Oxirigacha yetib borib topilmasa → **yo‘q**

---

## Vizual misol 👀

```text
Massiv: [4, 7, 1, 9, 3]
Target: 9

4 ❌
7 ❌
1 ❌
9 ✅  → Topildi

```

---

## Oddiy C++ misol

```cpp
#include <iostream>
using namespace std;

int linearSearch(int arr[], int size, int target) {
    for (int i = 0; i < size; i++) {
        if (arr[i] == target)
            return i;
    }
    return -1;
}

int main() {
    int arr[] = {4, 7, 1, 9, 3};

    int index = linearSearch(arr, 5, 9);
    cout << index; // 3
}
```

---

## Vector bilan Linear Search

```cpp
#include <vector>
#include <iostream>
using namespace std;

int main() {
    vector<int> numbers = {10, 20, 30, 40};

    int target = 30;
    bool found = false;

    for (int num : numbers) {
        if (num == target) {
            found = true;
            break;
        }
    }

    cout << found; // 1 (true)
}
```

---

## Real hayot misoli 🌍

🎒 **Sumkadan kalit qidirish**:

* sumkani ochasan
* har bir narsani tekshirasan
* kalit topilguncha davom etasan

Bu — **Linear Search**.

---

## STL bilan Linear Search

C++ da `find()` funksiyasi bor:

```cpp
#include <algorithm>
#include <vector>

vector<int> numbers = {4, 7, 1, 9, 3};

auto it = find(numbers.begin(), numbers.end(), 9);

if (it != numbers.end()) {
    cout << "Topildi";
}
```

---

## Afzalliklari ✅

* Juda oddiy
* Har qanday data’da ishlaydi
* Qo‘shimcha shart yo‘q

---

## Kamchiliklari ❌

* Katta massivlarda sekin ishlaydi
* Har doim oxirigacha tekshirishi mumkin

---

## Time Complexity (Vaqt murakkabligi)

| Holat      | Murakkablik |
| ---------- | ----------- |
| Best case  | O(1)        |
| Worst case | O(n)        |
| Average    | O(n)        |

---

## Linear Search vs Binary Search

| Xususiyat            | Linear    | Binary   |
| -------------------- | --------- | -------- |
| Data sorted bo‘lishi | ❌         | ✅        |
| Tezligi              | Sekin     | Juda tez |
| Murakkablik          | O(n)      | O(log n) |
| Ishlatish osonligi   | Juda oson | O‘rtacha |

---

## Qachon Linear Search ishlatish kerak?

✅ Agar:

* massiv kichik bo‘lsa
* data tartiblanmagan bo‘lsa
* oddiy yechim kerak bo‘lsa

❌ Agar:

* massiv juda katta bo‘lsa
* tezlik muhim bo‘lsa

---

## Xulosa 🧠

Linear Search:

* o‘rganish uchun ideal
* barcha qidiruv algoritmlarining asosi
* keyinchalik Binary Search’ni tushunishni osonlashtiradi

👉 Har bir dasturchi buni bilishi shart 💪
