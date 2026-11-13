### APPROACH
A king can move to at most 8 surrounding squares on a chessboard. The number of valid moves depends on its position:
- **Corner:** 3 moves.
- **Border (not a corner):** 5 moves.
- **Inside the board:** 8 moves.
  
A counter checks whether the position lies on a border. If it lies on both a row and a column border, it's a corner.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    char c, d;
    cin >> c >> d;

    int cnt = 0;
    if(c=='a' || c=='h') cnt++;
    if(d=='1' || d=='8') cnt++;

    if(cnt==2) cout << 3;
    else if(cnt==1) cout << 5;
    else cout << 8;
}
```
---

### SUBMISSION
<img width="478" height="182" alt="image" src="https://github.com/user-attachments/assets/c4f5b9f6-b74d-46f7-9431-f3ac7765b8ae" />
<img width="198" height="38" alt="image" src="https://github.com/user-attachments/assets/fc81d73f-e28e-4719-8388-a1cd805aaecc" />
