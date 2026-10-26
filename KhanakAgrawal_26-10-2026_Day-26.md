### APPROACH
The mugs are sorted in increasing order so that the largest volume comes last. Since there are `n-1` friends, only `n-1` mugs need to be poured into the cup. 

Therefore, the largest mug is excluded, and the sum of the remaining volumes is calculated. 

If the sum is less than or equal to the cup's capacity `s`, print `YES`; otherwise, print `NO`.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, s;
    cin >> n >> s;
    
    vector<int> a(n);
    
    for(int i=0; i<n; i++) cin >> a[i];
    sort(a.begin(), a.end());
    
    int sum = 0;
    
    for(int i=0; i<n-1; i++) {
        sum += a[i];
    }
    
    if(sum <= s) cout << "YES" << endl;
    else cout << "NO" << endl;
}
```
---

### SUBMISSION
<img width="540" height="273" alt="image" src="https://github.com/user-attachments/assets/8d594f72-e9f8-46e9-9015-29e9a71db9a3" />
<img width="211" height="47" alt="image" src="https://github.com/user-attachments/assets/c93f92b9-3a04-4d72-bdde-e8d650f56ddd" />

