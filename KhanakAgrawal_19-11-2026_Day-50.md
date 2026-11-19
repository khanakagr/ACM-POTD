### APPROACH
Sort the prices in increasing order so that the most negative prices come first. 

Since only negative-priced TVs help earn money, select at most `m` of them, starting from the smallest values. 

Add their absolute values to the answer. Stop when a non-negative price is encountered.

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
<img width="446" height="224" alt="image" src="https://github.com/user-attachments/assets/b9b131f9-14e2-464a-ac44-481f13fb721d" />
<img width="194" height="46" alt="image" src="https://github.com/user-attachments/assets/67bb3264-d028-474d-9b52-9b64d8a5a899" />
