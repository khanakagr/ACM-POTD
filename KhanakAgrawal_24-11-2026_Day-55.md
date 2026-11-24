### APPROACH
Each square has its bottom-left corner at `(0,0)` and its top-right corner at `(a[i],a[i])`. Sort the side lengths in decreasing order so that the largest square comes first.

If `k` is greater than `n`, print `-1` because there aren't enough squares. Otherwise, choose the point `(a[k-1], 0)`.

This point belongs to the `k` largest squares but not to any smaller square, so it belongs to exactly `k` squares.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, k;
    cin >> n >> k;

    vector<int> a(n);

    for(int i=0; i<n; i++) cin >> a[i];

    sort(a.begin(), a.end(), greater<int>());

    if(k>n) cout << -1;
    else cout << a[k-1] << " 0";
}
```
---

### SUBMISSION
<img width="446" height="190" alt="image" src="https://github.com/user-attachments/assets/ae8f49e7-eb5c-4977-94ab-d78719687fc3" />
<img width="190" height="44" alt="image" src="https://github.com/user-attachments/assets/2f192dea-6b5e-4f03-b023-6bd99847973a" />
