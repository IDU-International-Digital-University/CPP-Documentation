# Circular Linked List

![Topic](https://img.shields.io/badge/Topic-CircularLinkedList-orange)

---

## 📌 Kirish

**Circular Linked List** — node’lar **oxirgi node boshga ulanadi**.  
- **Singly circular**: oxirgi node `head` ga ulanadi  
- **Doubly circular**: oxirgi node `head` ga ulanadi va backward ham mumkin

---

## 🔁 Strukturasi (Singly)

```
head -> [1|next] -> [2|next] -> [3|next] -+
^---------------------------------+

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
    Node* second = new Node{2, nullptr};
    Node* third = new Node{3, nullptr};

    head->next = second;
    second->next = third;
    third->next = head; // circular

    Node* temp = head;
    int count = 0;
    while(count < 6) { // print 2 cycles
        cout << temp->data << " ";
        temp = temp->next;
        count++;
    }
}
```

**Output:**

```
1 2 3 1 2 3
```

---

## 🖼️ Image prompt

*"Illustrate a circular singly linked list with arrows from last node to head, clean educational diagram, easy to understand"*

---

## ✅ Xulosa

* Oxirgi element boshga ulanadi
* Foydali: musiqiy playlist, round robin
* Traversalda diqqat: infinite loop xavfi

---

➡️ Keyingi: [Binary Search Tree](bst.md)
