### APPROACH
The highest bid is found along with its position in the array. Then, the highest bid among the remaining participants is found as the price the winner has to pay. 

Finally, the winner's 1-based index and the second-highest bid are printed.

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

    int maxi = a[0], pos = 0;

    for(int i=1; i<n; i++) {
        if(a[i]>maxi) {
            maxi = a[i];
            pos = i;
        }
    }

    int second = 0;

    for(int i=0; i<n; i++) {
        if(i!=pos && a[i]>second) second = a[i];
    }

    cout << pos+1 << " " << second;
}
```

---

### SUBMISSION
<img width="504" height="347" alt="image" src="https://github.com/user-attachments/assets/ec86248e-47f8-4c1b-a327-748b99a45b2c" />
<img width="208" height="45" alt="image" src="https://github.com/user-attachments/assets/d2a015a6-7502-4d0f-acdf-648c3f50c41f" />
