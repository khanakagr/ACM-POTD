### APPROACH
There are 4 sticks, and any 3 of them can be selected to form a triangle. Check all possible combinations of 3 sticks.

For each combination:
- If the sum of the two smaller sides is greater than the largest side, a proper triangle can be formed.
- If the sum is equal to the largest side, a degenerate triangle (segment) can be formed.
  
If any combination forms a proper triangle, print `TRIANGLE`. Otherwise, if any combination forms a degenerate triangle, print `SEGMENT`. If neither is possible, print `IMPOSSIBLE`.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int a[4];

    for(int i=0; i<4; i++) cin >> a[i];

    bool triangle = false, segment = false;

    for(int i=0; i<4; i++) {
        for(int j=i+1; j<4; j++) {
            for(int k=j+1; k<4; k++) {
                int x = a[i], y = a[j], z = a[k];

                if(x>y) swap(x, y);
                if(y>z) swap(y, z);
                if(x>y) swap(x, y);

                if(x+y>z) triangle = true;
                else if(x+y==z) segment = true;
            }
        }
    }

    if(triangle) cout << "TRIANGLE";
    else if(segment) cout << "SEGMENT";
    else cout << "IMPOSSIBLE";
}
```
---

### SUBMISSION
<img width="473" height="308" alt="image" src="https://github.com/user-attachments/assets/349a20d1-44a4-4d28-8bfe-307cfc0e50de" />
<img width="191" height="43" alt="image" src="https://github.com/user-attachments/assets/826894d3-cdee-4a2e-b22f-20474948e6a9" />
