### APPROACH
Each leaf is identified by two things: its tree species and its color. If both are the same as an already counted leaf, it should not be counted again.

Store each pair of strings in a `set`. Since a set only stores unique elements, its size at the end gives the number of distinct leaves.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, m;
    cin >> n >> m;

    vector<int> a(n);
    for(int i=0; i<n; i++) cin >> a[i];

    sort(a.begin(), a.end());

    int sum = 0;
    for(int i=0; i<m; i++) {
        if(a[i]<0) sum += -a[i];
        else break;
    }

    cout << sum;
}
```
---

### SUBMISSION
<img width="591" height="203" alt="image" src="https://github.com/user-attachments/assets/cb58b7ae-9524-4795-a94c-6eae901265ae" />
<img width="193" height="43" alt="image" src="https://github.com/user-attachments/assets/6260f431-2aa0-40aa-8e33-6db4578bcfb6" />
