### APPROACH
The number of cubes needed for each level is calculated using the formula `i*(i+1)/2`. 

Starting from the first level, these cubes are added to the total. If adding the next level exceeds the available number of cubes `n`, the loop stops. 

The number of completely built levels is then printed.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;
    
    int height = 0;
    int total = 0;
    
    for(int i=1; ; i++) {
        int cubes = (i*(i+1))/2;
        
        if(total+cubes > n) break;

        total += cubes;
        height++;
    }
    
    cout << height << endl;
}
```
---

### SUBMISSION
<img width="480" height="238" alt="image" src="https://github.com/user-attachments/assets/421064dc-df87-4c06-8182-74784edf2f09" />
<img width="191" height="42" alt="image" src="https://github.com/user-attachments/assets/332d696f-2669-4351-9e63-3e3ae5fa012b" />
