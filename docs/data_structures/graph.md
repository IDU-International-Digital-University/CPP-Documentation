# Graph

![Topic](https://img.shields.io/badge/Topic-Graph-red)

---

## 📌 Kirish

**Graph (Graf)** — bu **vertexlar (node) va edges (bog‘lanishlar)** dan iborat tuzilma.  

- **Directed**: yo‘nalish bor  
- **Undirected**: yo‘nalish yo‘q  
- **Weighted**: har bir edge og‘irlikka ega  
- **Unweighted**: edge og‘irligi yo‘q

---

## 🔁 Misol (C++)

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n = 5;
    vector<int> adj[n];

    // Undirected graph
    adj[0] = {1, 2};
    adj[1] = {0, 3};
    adj[2] = {0, 4};
    adj[3] = {1};
    adj[4] = {2};

    for(int i=0;i<n;i++){
        cout << i << ": ";
        for(int v: adj[i])
            cout << v << " ";
        cout << endl;
    }
}
````

---

## 🖼️ Image prompt

*"Draw a simple undirected graph with 5 nodes and edges connecting them, clear and colorful diagram for students"*

---

## ✅ Xulosa

* Graph → vertices + edges
* DFS / BFS bilan ishlatiladi
* Directed / Undirected, Weighted / Unweighted tushunchalari

---

➡️ Keyingi: [End of Data Structures Fundamentals]

