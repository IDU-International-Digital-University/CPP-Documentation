# Tree (Daraxt)

![Topic](https://img.shields.io/badge/Topic-Tree-blue)

---

## 📌 Kirish

**Tree** — bu **hierarchical (ierarxik) data structure** bo‘lib, ma’lumotlar "node"lar ko‘rinishida saqlanadi.  

- Har bir node ma’lumot (`data`) va child node’lar ro‘yxatiga ega  
- Bitta node **root** deb ataladi (daraxtning bosh node’i)  
- Node’lar oxirigacha yetadigan yo‘llar **paths** deb ataladi  
- Node’lar **leaf (barg)** yoki **internal** node bo‘lishi mumkin

---

## 🔁 Tuzilishi

```

```
    Root
   /    \
Node1   Node2
/  \      \
```

Leaf1 Leaf2   Node3

````

---

## 🧩 Misol (C++)

```cpp
#include <iostream>
#include <vector>
using namespace std;

struct TreeNode {
    int data;
    vector<TreeNode*> children;
};

int main() {
    TreeNode* root = new TreeNode{1, {}};
    TreeNode* child1 = new TreeNode{2, {}};
    TreeNode* child2 = new TreeNode{3, {}};

    root->children.push_back(child1);
    root->children.push_back(child2);

    cout << "Root: " << root->data << endl;
    for(auto c : root->children)
        cout << "Child: " << c->data << endl;
}
````

**Output:**

```
Root: 1
Child: 2
Child: 3
```

---

## 🖼️ Image prompt

*"Draw a general tree with a root node and three children, hierarchical layout, colorful and clear diagram for students"*

---

## ✅ Xulosa

* Har bir node bir yoki bir nechta child’ga ega bo‘lishi mumkin
* Trees → graph’ning special turi
* Traversal: DFS, BFS, inorder/preorder/postorder

---

➡️ Keyingi: [Binary Search Tree](bst.md)
