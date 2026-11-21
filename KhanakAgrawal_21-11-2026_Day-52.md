### APPROACH
The array contains only numbers 1, 2, and 3. Count the frequency of each number using a frequency array. 

To make all elements equal, keep the number that occurs the most and replace all the others. 

Therefore, subtract the maximum frequency from `n` to get the minimum number of replacements.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    int a[4] = {0};

    for(int i=0; i<n; i++) {
        int x;
        cin >> x;
        a[x]++;
    }

    int maxi = max(a[1], max(a[2], a[3]));

    cout << n-maxi;
}
```
---

### SUBMISSION
<img width="461" height="214" alt="image" src="https://github.com/user-attachments/assets/78cc6d85-affa-4666-b0a0-69bf0d42bd08" />
<img width="191" height="41" alt="image" src="https://github.com/user-attachments/assets/324ffc63-f3f5-4f91-9d08-694b548bc7c1" />
