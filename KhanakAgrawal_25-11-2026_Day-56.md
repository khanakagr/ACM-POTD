### APPROACH
For each pair of numbers, repeatedly subtract the smaller number from the larger one until one of them becomes zero. Count the number of operations performed.

Instead of subtracting one by one, use division to perform multiple subtractions at once. If `a` is greater than `b`, add a/b to the count and update `a` to `a%b`. Do the same when `b` is greater than `a`. Repeat until one number becomes zero.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    while(n--) {
        long long a, b;
        cin >> a >> b;

        long long cnt = 0;

        while(a>0 && b>0) {
            if(a>b) {
                cnt += a/b;
                a = a%b;
            } else {
                cnt += b/a;
                b = b%a;
            }
        }
        cout << cnt << endl;
    }
}
```
---

### SUBMISSION
<img width="460" height="281" alt="image" src="https://github.com/user-attachments/assets/c9c74240-a861-4053-95dd-25e23dde13ec" />
<img width="193" height="44" alt="image" src="https://github.com/user-attachments/assets/5e6de807-e6e1-4c81-b519-bfaccb6eaf41" />
