### APPROACH
The sequence is arranged with all odd numbers first, followed by all even numbers.

First, calculate the number of odd numbers, which is `(n+1)/2`.
- If `k` is less than or equal to the number of odd numbers, the answer is the kth odd number, calculated as `2*k-1`.
- Otherwise, the answer is the kth even number after the odd numbers, calculated as `2*(k-(n+1)/2)`.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    long long n, k;
    cin >> n >> k;

    long long mid = (n+1)/2;

    if(k<=mid) cout << 2*k-1;
    else cout << 2*(k-mid);
}
```
---

### SUBMISSION
<img width="461" height="143" alt="Screenshot 2026-11-28 210555" src="https://github.com/user-attachments/assets/62230ef7-dd24-46b1-85a5-a9cca9fe72dc" />
<img width="194" height="45" alt="image" src="https://github.com/user-attachments/assets/7e1a0c24-2f62-473d-a002-80a4f455a1fd" />
