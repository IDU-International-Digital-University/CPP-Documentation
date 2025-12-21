# Doubly Linked List

![Topic](https://img.shields.io/badge/Topic-DoublyLinkedList-green)

---

## 📌 Kirish

**Doubly Linked List** — ikki tomonlama bog‘langan ro‘yxat.  
Har bir node:

- `data` — ma’lumot  
- `next` — keyingi elementga pointer  
- `prev` — oldingi elementga pointer  

---

## 🔁 Strukturasi

```

NULL <- [data|prev|next] <-> [data|prev|next] <-> [data|prev|next] -> NULL

```

---

## 🧩 Misol (C++)

```cpp
#include <iostream>
using namespace std;

struct Node {
    int data;
    Node* prev;
    Node* next;
};

int main() {
    Node* head = new Node{1, nullptr, nullptr};
    Node* second = new Node{2, head, nullptr};
    head->next = second;
    Node* third = new Node{3, second, nullptr};
    second->next = third;

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

*"Draw a doubly linked list with three nodes, showing 'data', 'next', and 'prev' pointers, arrows in both directions, clean diagram for students"*

---

## ✅ Xulosa

* Oldinga va orqaga yurish mumkin
* Qo‘shimcha xotira talab qiladi (prev pointer)
* Murakkabroq lekin qulayroq traversals

---

➡️ Keyingi: [Circular Linked List](linked_list_circular.md)
