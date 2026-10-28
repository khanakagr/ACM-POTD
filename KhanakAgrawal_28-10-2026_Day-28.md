### APPROACH
The given string contains lowercase letters, commas, spaces, and curly brackets. A frequency array of size 26 is used to track distinct letters. 

Each lowercase letter is mapped to an index using `ch - 'a'`. If that letter has not appeared before, its count is increased. 

Finally, the total number of distinct letters is printed.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    string s;
    getline(cin, s);

    vector<int> freq(26, 0);
    int cnt = 0;

    for(int i=0; i<s.length(); i++) {
        if(s[i]>='a' && s[i]<='z') {
            if(freq[s[i]-'a']==0) {
                freq[s[i]-'a']++;
                cnt++;
            }
        }
    }

    cout << cnt;
}
```
---

### SUBMISSION
<img width="544" height="268" alt="image" src="https://github.com/user-attachments/assets/96af45c5-2b00-4bbf-8f4a-8b5599d394b3" />
<img width="204" height="46" alt="image" src="https://github.com/user-attachments/assets/2ae542c5-ea9e-4a9f-84ef-39773cc7c624" />
