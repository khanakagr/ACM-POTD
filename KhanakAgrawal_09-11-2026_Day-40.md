### APPROACH
The goal is to find the smallest multiple of `k` that is greater than `n`. 

Integer division `n/k` gives the number of complete multiples of `k` within `n`. 

Adding `1` and multiplying by `k` gives the next multiple.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    long long n, k;
    cin >> n >> k;

    cout << (n/k+1)*k;
}
```
---

### SUBMISSION
<img width="514" height="116" alt="image" src="https://github.com/user-attachments/assets/c4e485b1-f8bc-45c9-b4a5-4992496ce04e" />
<img width="190" height="39" alt="image" src="https://github.com/user-attachments/assets/2ecbf64d-c326-4a06-9a6f-22c1803459b6" />
