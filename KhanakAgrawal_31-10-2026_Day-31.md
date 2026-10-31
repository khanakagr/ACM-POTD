### APPROACH
The game has `n` levels, and each friend can pass certain levels. 

An array is used to mark the levels that either friend can pass. If every level from `1 to n` is marked, print `I become the guy`. Otherwise, print `Oh, my keyboard!`.

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    vector<int> levels(n+1, 0);

    int p;
    cin >> p;

    for(int i=0; i<p; i++) {
        int x;
        cin >> x;
        levels[x] = 1;
    }

    int q;
    cin >> q;

    for(int i=0; i<q; i++) {
        int x;
        cin >> x;
        levels[x] = 1;
    }

    for(int i=1; i<=n; i++) {
        if(levels[i]==0) {
            cout << "Oh, my keyboard!";
            return 0;
        }
    }

    cout << "I become the guy.";
}
```
---

### SUBMISSION
<img width="494" height="387" alt="image" src="https://github.com/user-attachments/assets/7ed860d5-2d8f-4499-8b5c-205f45b82a7e" />
<img width="192" height="44" alt="image" src="https://github.com/user-attachments/assets/b2e91612-b806-4343-8831-f28ab015c5a9" />
