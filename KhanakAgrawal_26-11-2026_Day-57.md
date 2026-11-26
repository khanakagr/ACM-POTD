### APPROACH
Initially, all 9 lights are ON (1). For every cell, check whether its number of presses is odd. If it is odd, toggle that light and its adjacent lights (up, down, left and right). 

Use boundary conditions to make sure only valid positions are toggled. Finally, print the resulting 3×3 matrix.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int a[3][3], b[3][3];

    for(int i=0; i<3; i++) {
        for(int j=0; j<3; j++) {
            cin >> a[i][j];
            b[i][j] = 1;
        }
    }

    for(int i=0; i<3; i++) {
        for(int j=0; j<3; j++) {
            if(a[i][j]%2==1) {
                b[i][j] = 1-b[i][j];

                if(i>0) b[i-1][j] = 1-b[i-1][j];
                if(i<2) b[i+1][j] = 1-b[i+1][j];
                if(j>0) b[i][j-1] = 1-b[i][j-1];
                if(j<2) b[i][j+1] = 1-b[i][j+1];
            }
        }
    }

    for(int i=0; i<3; i++) {
        for(int j=0; j<3; j++) {
            cout << b[i][j];
        }
        cout << endl;
    }
}
```
---

### SUBMISSION
<img width="457" height="353" alt="image" src="https://github.com/user-attachments/assets/f9287d93-0064-4fc7-99da-3c5623cac803" />
<img width="191" height="41" alt="image" src="https://github.com/user-attachments/assets/e3446546-fb33-4f76-8f0f-08a4a925f49c" />
