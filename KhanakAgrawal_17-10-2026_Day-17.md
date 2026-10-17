### APPROACH
The task is to find how many additional horseshoes need to be bought so that all four horseshoes have different colors.

The four colors are stored in an array. If any colors are repeated, only one horseshoe of that color is needed, so the repeated ones must be replaced. The easiest way is to count the distinct colors and subtract that count from 4.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int a[4], cnt = 0;
    cin >> a[0] >> a[1] >> a[2] >> a[3];

    for(int i=0; i<4; i++) {
        bool same = false;
        for(int j=0; j<i; j++) {
            if(a[i] == a[j]) {
                same = true;
                break;
            }
        }
        if(same) cnt++;
    }
    cout << cnt << endl;
}
```

---

### SUBMISSION
<img width="628" height="244" alt="image" src="https://github.com/user-attachments/assets/b1588723-f20e-42e9-a1dc-9107e2d02811" />
