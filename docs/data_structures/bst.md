
# Binary Search Tree (BST)

![Topic](https://img.shields.io/badge/Topic-BST-red)

---

## 📌 Kirish

**BST** — bu daraxt (tree) tuzilmasi bo‘lib, har bir node quyidagilarni bajaradi:

- Left child < Parent  
- Right child > Parent  
- Duplicate element yo‘q

---

## 🔁 Strukturasi


```sh
   
   10
  /  \
 5   15
/ \   \

```

```
3   7   20
```

---

## 🧩 Misol (C++)

```cpp
#include <iostream>
using namespace std;

struct Node {
    int data;
    Node* left;
    Node* right;
};

Node* insert(Node* root, int value) {
    if(!root) return new Node{value, nullptr, nullptr};
    if(value < root->data) root->left = insert(root->left, value);
    else root->right = insert(root->right, value);
    return root;
}

void inorder(Node* root) {
    if(root) {
        inorder(root->left);
        cout << root->data << " ";
        inorder(root->right);
    }
}

int main() {
    Node* root = nullptr;
    root = insert(root, 10);
    insert(root, 5);
    insert(root, 15);
    insert(root, 3);
    insert(root, 7);
    insert(root, 20);

    inorder(root); // 3 5 7 10 15 20
}
```

---

## 🖼️ Image prompt

*"Draw a binary search tree with nodes labeled with integers, showing left < parent < right, clear and colorful diagram for students"*

---

## ✅ Xulosa

* Tez qidirish, o‘chirish, qo‘shish
* Balanced bo‘lsa O(log n) samarali
* Traversal: inorder, preorder, postorder

---

➡️ Keyingi: [DFS](dfs.md)
