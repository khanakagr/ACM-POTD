### APPROACH
The pattern alternates between `I hate` and `I love`, starting with `I hate`. A loop runs from `1` to `n`. 

After each phrase, `that` is printed if it is not the last layer; otherwise, `it` is printed to complete the sentence.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    for(int i=1; i<=n; i++) {
        if(i%2==1) cout << "I hate";
        else cout << "I love";

        if(i==n) cout << " it";
        else cout << " that ";
    }
}
```
---

### SUBMISSION
<img width="449" height="179" alt="image" src="https://github.com/user-attachments/assets/0ae23d40-b9c6-416e-b3c7-1c1f304d979b" />
<img width="191" height="40" alt="image" src="https://github.com/user-attachments/assets/fe2c564e-e5a1-46e0-b764-148631f8d0bb" />
