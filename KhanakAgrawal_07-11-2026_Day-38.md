### APPROACH
A frequency array of size m+1 is used to keep track of which bulbs can be turned on. 

For each button, the bulbs connected to it are marked as 1 in the array. After checking all buttons, the array is traversed from 1 to m. 

If any bulb is still unmarked, print NO; otherwise, print `YES`.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, m;
    cin >> n >> m;

    vector<int> a(m+1, 0);

    for(int i=0; i<n; i++) {
        int x;
        cin >> x;

        for(int j=0; j<x; j++) {
            int y;
            cin >> y;
            a[y] = 1;
        }
    }

    for(int i=1; i<=m; i++) {
        if(a[i]==0) {
            cout << "NO";
            return 0;
        }
    }

    cout << "YES";

    return 0;
}
```
---

### SUBMISSION
<img width="431" height="336" alt="image" src="https://github.com/user-attachments/assets/e3673554-54a4-4542-a522-1e9116d80a18" />
<img width="193" height="44" alt="image" src="https://github.com/user-attachments/assets/5729533d-7fd7-4616-8dec-89b628510ffc" />
