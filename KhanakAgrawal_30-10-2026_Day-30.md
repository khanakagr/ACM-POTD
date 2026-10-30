### APPROACH
For each room, the number of people currently staying and the room's total capacity are taken as input. If the room has at least 2 empty spaces, the count is increased. 

Finally, the total number of rooms with enough space for George and Alex is printed.

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    int cnt = 0;

    for(int i=0; i<n; i++) {
        int p, q;
        cin >> p >> q;
        if(q-p >= 2) cnt++;
    }

    cout << cnt;
}
```
---

### SUBMISSION
<img width="589" height="228" alt="image" src="https://github.com/user-attachments/assets/40f7a44e-81c9-478e-ad21-8a2bc005c952" />
<img width="210" height="47" alt="image" src="https://github.com/user-attachments/assets/a2d72209-80e5-42e5-a0d3-ef9c6f6a1394" />
