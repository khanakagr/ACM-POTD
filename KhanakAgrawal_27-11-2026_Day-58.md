### APPROACH
Start from the first sector and check every position in the road. If a sector contains a `.` (no rock), update the current position. 

If it contains a `#`, check whether the distance from the last safe position is greater than `k`. 

If it is, Ksusha cannot jump over the rocks, so print `NO`. Otherwise, continue checking. If the last sector is reachable, print `YES`.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, k;
    cin >> n >> k;

    string s;
    cin >> s;

    int pos = 0;

    for(int i=0; i<n; i++) {
        if(s[i]=='.') pos = i;

        if(i-pos>=k && s[i]=='#') {
            cout << "NO";
            return 0;
        }
    }
    cout << "YES";
}
```
---

### SUBMISSION
<img width="545" height="253" alt="image" src="https://github.com/user-attachments/assets/729e2f52-a69f-41ac-8811-83390d2e35e7" />
<img width="191" height="44" alt="image" src="https://github.com/user-attachments/assets/baab8235-51f0-4757-908e-f86e5f4a0572" />
