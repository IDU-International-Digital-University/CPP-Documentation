# Depth-First Search (DFS)

![Topic](https://img.shields.io/badge/Topic-DFS-purple)

---

## 📌 Kirish

**DFS** — bu grafni **chuqurlik bo‘yicha** kezish algoritmi.  

- Stack (yoki recursion) yordamida ishlaydi  
- Har bir vertex faqat bir marta tashrif qilinadi

---

## 🔁 Ishlash printsipi

1. Start node tanlanadi  
2. Har bir qo‘shni vertexga chuqur kiriladi  
3. Backtrack qilish kerak bo‘lsa, oldingi node ga qaytiladi  

---

## 🧩 Misol (C++)

```cpp
#include <bits/stdc++.h>
using namespace std;

void dfs(int v, vector<int> adj[], vector<bool>& visited) {
    visited[v] = true;
    cout << v << " ";
    for(int u : adj[v])
        if(!visited[u])
            dfs(u, adj, visited);
}

int main() {
    int n = 5;
    vector<int> adj[n];
    adj[0] = {1, 2};
    adj[1] = {0, 3};
    adj[2] = {0, 4};
    adj[3] = {1};
    adj[4] = {2};

    vector<bool> visited(n, false);
    dfs(0, adj, visited);
}
````

---

## 🖼️ Image prompt

*"Draw a depth-first search traversal on a simple graph with 5 nodes, arrows showing traversal order, educational style"*

---

## ✅ Xulosa

* DFS: recursion yoki stack
* Chuqurlik bo‘yicha elementlarni tekshiradi
* Tez-tez tree va graph algoritmlarida ishlatiladi

---

➡️ Keyingi: [BFS](bfs.md)
