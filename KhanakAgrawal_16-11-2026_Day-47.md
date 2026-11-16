### APPROACH
Traverse the array from left to right and check whether each element is strictly greater than the previous one. 

If it is not, calculate how many times `d` must be added to make it greater. 

Add those moves to the answer and update the current element so that the next element can be checked against its updated value.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, d;
    cin >> n >> d;

    vector<int> a(n);

    for(int i=0; i<n; i++) cin >> a[i];

    int cnt = 0;

    for(int i=1; i<n; i++) {
        if(a[i]<=a[i-1]) {
            int x = (a[i-1]-a[i])/d + 1;

            cnt += x;
            a[i] += x*d;
        }
    }
    cout << cnt;
}
```
---

### SUBMISSION
<img width="478" height="261" alt="image" src="https://github.com/user-attachments/assets/0299e367-779c-4894-bb31-6e2def225285" />
<img width="194" height="41" alt="image" src="https://github.com/user-attachments/assets/74e29d2f-8bbe-41f8-8031-eb1c8bec4b50" />
