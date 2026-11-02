### APPROACH
The given expression follows a pattern where every two consecutive numbers cancel each other partially:
- `-1 + 2 = 1`
- `-3 + 4 = 1`
- `-5 + 6 = 1`
  
So, if `n` is even, the answer is simply `n/2`.

If `n` is odd, the last number remains negative, so the answer becomes `-(n+1)/2`.

This allows the answer to be calculated directly without using a loop.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    long long n;
    cin >> n;

    if(n%2==0) cout << n/2;
    else cout << -(n+1)/2;
}
```
---

### SUBMISSION
<img width="500" height="127" alt="image" src="https://github.com/user-attachments/assets/ffa5b67d-c976-4bad-bac5-17e527a7884c" />
<img width="185" height="37" alt="image" src="https://github.com/user-attachments/assets/f2e2568f-98cd-46b3-88d4-1c49c05a4eab" />
