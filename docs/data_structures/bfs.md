# 6️⃣ `bfs.md` (Breadth-First Search)

```md
# Breadth-First Search (BFS)

![Topic](https://img.shields.io/badge/Topic-BFS-orange)

---

## 📌 Kirish

**BFS** — bu grafni **kenglik bo‘yicha** kezish algoritmi.  

- Queue yordamida ishlaydi  
- Har bir vertex faqat bir marta tashrif qilinadi

---

## 🔁 Ishlash printsipi

1. Start node → Queue ga qo‘yiladi  
2. Queue dan node olinadi, tashrif qilinadi  
3. Qo‘shni vertexlar Queue ga qo‘yiladi  

---

## 🧩 Misol (C++)

```cpp
#include <bits/stdc++.h>
using namespace std;

void bfs(int start, vector<int> adj[], int n) {
    vector<bool> visited(n, false);
    queue<int> q;
    visited[start] = true;
    q.push(start);

    while(!q.empty()) {
        int v = q.front(); q.pop();
        cout << v << " ";
        for(int u : adj[v])
            if(!visited[u]) {
                visited[u] = true;
                q.push(u);
            }
    }
}

int main() {
    int n = 5;
    vector<int> adj[n];
    adj[0] = {1, 2};
    adj[1] = {0, 3};
    adj[2] = {0, 4};
    adj[3] = {1};
    adj[4] = {2};

    bfs(0, adj, n);
}
````

---

## 🖼️ Image prompt

*"Draw a breadth-first search traversal on a simple graph with 5 nodes, arrows showing order, clear educational diagram"*

---

## ✅ Xulosa

* BFS: queue asosida
* Kenglik bo‘yicha traversal
* Tree va graph muammolarida tez-tez ishlatiladi

---

➡️ Keyingi: [Graph](graph.md)