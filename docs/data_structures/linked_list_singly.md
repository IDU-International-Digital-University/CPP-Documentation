# Singly Linked List

![Topic](https://img.shields.io/badge/Topic-SinglyLinkedList-blue)

---

## 📌 Kirish

**Singly Linked List** — bu **bir tomonlama bog‘langan ro‘yxat**.  
Har bir element (node) quyidagi tarkibga ega:  

- `data` — ma’lumot  
- `next` — keyingi elementga ko‘rsatkich (pointer)  

> Har bir node faqat **keyingi node** ga ulanadi.

---

## 🔁 Strukturasi

```
head -> [data|next] -> [data|next] -> ... -> NULL

```

---

## 🧩 Misol (C++)

```cpp
#include <iostream>
using namespace std;

struct Node {
    int data;
    Node* next;
};

int main() {
    Node* head = new Node{1, nullptr};
    head->next = new Node{2, nullptr};
    head->next->next = new Node{3, nullptr};

    Node* temp = head;
    while(temp != nullptr) {
        cout << temp->data << " ";
        temp = temp->next;
    }
}
```

**Output:**

```
1 2 3
```

---

## 🖼️ Image prompt

*"Illustrate a singly linked list with three nodes showing 'data' and 'next' pointers in a clean, educational style, easy for students to understand, colorful diagram"*

---

## ✅ Xulosa

* Oddiy struktura
* Qo‘shimcha element faqat oxiridan qo‘shiladi yoki boshidan
* Backward traversal yo‘q

---

➡️ Keyingi: [Doubly Linked List](linked_list_doubly.md)
