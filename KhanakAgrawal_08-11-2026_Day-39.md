### APPROACH
The task is to find the last two digits of `5^n`. 

Since `n` is always greater than or equal to `2`, the last two digits of every such power are always `25`. 

Therefore, there is no need to calculate the power. Simply print `25`.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    long long n;
    cin >> n;

    cout << 25;
}
```
---

### SUBMISSION
<img width="589" height="113" alt="image" src="https://github.com/user-attachments/assets/ae9860bd-45e9-48b1-953c-a64d2a51a758" />
<img width="191" height="40" alt="image" src="https://github.com/user-attachments/assets/e3314d94-0bc1-48e3-9036-a98bd4f3b25c" />
