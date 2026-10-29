### APPROACH
The pattern is divided into three parts: the upper half, the middle row, and the lower half. 

In the upper half, the number of `*` decreases while the number of `D` increases by 2 in each row. 

The middle row contains only `D`. 

In the lower half, the number of `*` increases while the number of `D` decreases by 2 in each row, forming a symmetrical diamond pattern.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
	int n;
	cin >> n;
	
	for(int i=0; i<n/2; i++) {
        for(int j=0; j<n/2-i; j++) cout << '*';
        for(int j=0; j<2*i+1; j++) cout << 'D';
        for(int j=0; j<n/2-i; j++) cout << '*';
        cout << endl;
    }
    
    for(int j=0; j<n; j++) cout << 'D';
    cout << endl;

    for(int i=0; i<n/2; i++) {
        for(int j=0; j<i+1; j++) cout << '*';
        for(int j=0; j<n-2*(i+1); j++) cout << 'D';
        for(int j=0; j<i+1; j++) cout << '*';
        cout << endl;
    }
}

```
---

### SUBMISSION
<img width="592" height="305" alt="image" src="https://github.com/user-attachments/assets/3f7db836-3575-48ab-a83f-8589ef558311" />
<img width="212" height="45" alt="image" src="https://github.com/user-attachments/assets/e461a5f0-14e8-4e66-bb1d-f04c1f0965ee" />

