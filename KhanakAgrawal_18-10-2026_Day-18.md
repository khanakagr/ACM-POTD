### APPROACH
The task is to find how many stones need to be removed so that no two adjacent stones have the same color.

So, we can go through the string and compare each stone with the one immediately after it. If both have the same color, increase the count because one of them needs to be removed. Finally, print the total count.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, cnt = 0;
    string s;
    cin >> n >> s;

    for(int i=0; i<n-1; i++) {
        if(s[i] == s[i+1]) cnt++;
    }
    cout << cnt << endl;
}

```

---

### SUBMISSION
<img width="554" height="189" alt="image" src="https://github.com/user-attachments/assets/1352ae98-6bc9-41c0-9a5f-80359b691694" />
<img width="215" height="45" alt="image" src="https://github.com/user-attachments/assets/c4d85d15-43c8-47e7-b6b9-2b9134fc8001" />
