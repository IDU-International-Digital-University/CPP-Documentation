
# C++ Recursion

![Topic](https://img.shields.io/badge/Topic-Recursion-purple)
![Level](https://img.shields.io/badge/Level-Intermediate-yellow)

---

## 📌 Kirish

**Rekursiya** — bu funksiya **o‘zini o‘zi chaqirishi**.

U quyidagi holatlarda juda foydali:
- matematik masalalar
- daraxtlar (trees)
- qidiruv algoritmlari
- bo‘linib yechiladigan muammolar

---

## 🔁 Rekursiyaning 2 ta asosiy qismi

1️⃣ **Base case** — to‘xtash sharti  
2️⃣ **Recursive case** — funksiya o‘zini chaqiradi  

❗ Base case bo‘lmasa — **infinite loop** bo‘ladi.

---

## 📐 Oddiy misol

```cpp
void countDown(int n) {
    if (n == 0)
        return;

    cout << n << endl;
    countDown(n - 1);
}
````

### Ishlash tartibi:

```
countDown(3)
→ 3
→ 2
→ 1
→ stop
```

---

## 🧮 Factorial (klassik misol)

```cpp
int factorial(int n) {
    if (n == 1)
        return 1;

    return n * factorial(n - 1);
}
```

```cpp
factorial(5)
// 5 * 4 * 3 * 2 * 1 = 120
```

---

## 🔢 Fibonacci sonlari

```cpp
int fib(int n) {
    if (n <= 1)
        return n;

    return fib(n - 1) + fib(n - 2);
}
```

---

## 🧠 Call Stack qanday ishlaydi?

Har bir funksiya chaqiruvi:

* stack ga joylanadi
* tugagach stack dan chiqadi

👉 Rekursiya stack’ni tez to‘ldirishi mumkin.

---

## ⚠️ Rekursiya kamchiliklari

❌ Sekin ishlashi
❌ Stack overflow xavfi
❌ Ko‘p xotira ishlatadi

---

## ✅ Qachon rekursiya ishlatish kerak?

✔ Daraxtlar
✔ DFS
✔ Divide & Conquer
✔ Matematik formulalar

❌ Oddiy loop bo‘lsa — `for` ishlatish yaxshiroq

---

## 🔄 Rekursiya vs Loop

| Rekursiya             | Loop            |
| --------------------- | --------------- |
| Oson tushuniladi      | Tezroq          |
| Ko‘proq xotira        | Kam xotira      |
| Murakkab strukturalar | Oddiy vazifalar |

---

## 🧠 Xulosa

Rekursiya:

* kuchli texnika
* lekin ehtiyot bilan ishlatiladi

Yaxshi dasturchi:
👉 qachon rekursiya
👉 qachon loop ishlatishni biladi

---

➡️ Keyingi mavzu: **Arrays & Pointers**
