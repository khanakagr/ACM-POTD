### APPROACH
The string contains `A` for Anton's wins and `D` for Danik's wins. 

Count the occurrences of both characters while traversing the string. 

Compare the two counts and print `Anton`, `Danik`, or `Friendship` depending on who won more games.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;
    string s;
    cin >> s;

    int a=0, d=0;
    for(int i=0; i<n; i++) {
        if(s[i]=='A') a++;
        else d++;
    }

    if(a>d) cout << "Anton";
    else if(d>a) cout << "Danik";
    else cout << "Friendship";
}
```
---

### SUBMISSION
<img width="481" height="215" alt="image" src="https://github.com/user-attachments/assets/4f5a378a-040f-4d41-8c85-f9ea50069f8e" />
<img width="189" height="42" alt="image" src="https://github.com/user-attachments/assets/a998a4ad-f46f-4fdd-bc1e-30517def2460" />
