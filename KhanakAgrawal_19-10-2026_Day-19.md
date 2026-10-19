### APPROACH
The task is to find the smallest year greater than the given year where all four digits are different. Starting from the next year, each year is checked by extracting its four digits and comparing them. 

If all the digits are distinct, that year is printed; otherwise, the search continues with the next year.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int y;
    cin >> y;

    while(true) {
        y++;

        int a = y/1000;
        int b = (y/100)%10;
        int c = (y/10)% 10;
        int d = y%10;

        if(a!=b && a!=c && a!=d && b!=c && b!=d && c!=d) {
            cout << y;
            break;
        }
    }
}
```

---

### SUBMISSION
<img width="525" height="269" alt="image" src="https://github.com/user-attachments/assets/dce77b7f-0351-4700-93c6-7b2db389efc4" />
<img width="214" height="47" alt="image" src="https://github.com/user-attachments/assets/b6e04b47-a2d2-4029-8afe-8bc61d1210de" />

