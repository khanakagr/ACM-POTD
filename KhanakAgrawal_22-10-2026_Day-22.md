### APPROACH
The goal is to place the maximum number of coders on an `n X n` chessboard so that no two coders attack each other. Since a coder attacks only the cells directly above, below, left, and right, coders can be placed in alternating cells like a checkerboard.

For each cell, if the sum of its row and column indices is even, place a `C`; otherwise, place a `.`. Finally, print the total number of coders and the board.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    int cnt = 0;
    for(int i=0; i<n; i++) {
        for(int j=0; j<n; j++) {
            if((i+j)%2 == 0) cnt++;
        }
    }

    cout << cnt << endl;

    for(int i=0; i<n; i++) {
        for(int j=0; j<n; j++) {
            if((i+j)%2 == 0) cout << 'C';
            else cout << '.';
        }
        cout << endl;
    }
}
```

---

### SUBMISSION
<img width="488" height="305" alt="image" src="https://github.com/user-attachments/assets/82f7e958-38f4-426f-9794-244a41bcebc7" />
<img width="209" height="47" alt="image" src="https://github.com/user-attachments/assets/97f02b00-49bb-4d79-8922-104d068fd8b0" />
