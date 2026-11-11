### APPROACH
The array is traversed to find the longest continuous strictly increasing subarray. 

A variable `cnt` keeps track of the current increasing sequence, while `maxi` stores the maximum length found so far. 

If the current element is greater than the previous one, `cnt` is increased; otherwise, it is reset to 1. Finally, `maxi` is printed.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    vector<int> a(n);

    for(int i=0; i<n; i++) cin >> a[i];

    int cnt = 1, maxi = 1;
    for(int i=1; i<n; i++) {
        if(a[i]>a[i-1]) cnt++;
        else cnt = 1;

        maxi = max(maxi, cnt);
    }
    cout << maxi;
}
```
---

### SUBMISSION
<img width="500" height="224" alt="image" src="https://github.com/user-attachments/assets/56ee7e99-cb36-4b07-84c0-ea1691439f8d" />
<img width="190" height="43" alt="image" src="https://github.com/user-attachments/assets/e2188e09-80fd-4680-93f0-67087ca96ad0" />
