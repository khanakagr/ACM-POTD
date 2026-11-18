### APPROACH
A number is called almost prime if it has exactly two distinct prime factors. Traverse all numbers from `2` to `n` and count how many distinct prime numbers divide each number. If the count is exactly 2, increase the answer.

For example:
- 6 = 2 × 3 → Almost prime
- 12 = 2 × 2 × 3 → Almost prime (two distinct prime factors)
- 8 = 2 × 2 × 2 → Not almost prime

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    int ans=0;

    for(int i=2; i<=n; i++) {
        int x=i, cnt=0;

        for(int j=2; j<=x; j++) {
            if(x%j==0) {
                cnt++;

                while(x%j==0) x /= j;
            }
        }

        if(cnt==2) ans++;
    }
    cout << ans;
}
```
---

### SUBMISSION
<img width="530" height="481" alt="image" src="https://github.com/user-attachments/assets/f189f2c6-3e10-4760-b588-97b8a7d8826b" />

I was facing problem while submitting as it was showing "Please complete the anti-bot verification" message again and again, and wasn't getting submitted.
