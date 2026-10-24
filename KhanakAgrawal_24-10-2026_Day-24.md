### APPROACH
The password is checked for four conditions: its length must be at least 5 characters, and it must contain at least one uppercase letter, one lowercase letter, and one digit. 

A loop checks each character and updates the corresponding flags. If all four conditions are satisfied, print Correct; otherwise, print Too weak.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    string s;
    cin >> s;

    bool upper = false, lower = false, digit = false;

    for(int i=0; i<s.length(); i++) {
        if(s[i]>='A' && s[i]<='Z') upper = true;
        else if(s[i]>='a' && s[i]<='z') lower = true;
        else if(s[i]>='0' && s[i]<='9') digit = true;
    }

    if(s.length()>=5 && upper && lower && digit) cout << "Correct";
    else cout << "Too weak";
}
```
---

### SUBMISSION
<img width="578" height="233" alt="image" src="https://github.com/user-attachments/assets/ad07c371-d52c-49d7-baf0-e64aacde0c80" />
<img width="209" height="44" alt="image" src="https://github.com/user-attachments/assets/629cfa4f-2839-44ed-bb83-da07526ce0bd" />
