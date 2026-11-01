### APPROACH
The given number `n` needs to be written as the sum of two composite numbers. If `n` is even, print `4` and `n-4`. If `n` is odd, print `9` and `n-9`. 

Both numbers are composite, and their sum is always `n`.

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;
 
    if(n%2==0) cout << 4 << " " << n-4;
    else cout << 9 << " " << n-9;
}
```
---

### SUBMISSION
<img width="515" height="125" alt="image" src="https://github.com/user-attachments/assets/1b58f147-e2c8-489d-8d5f-d6ab2789c6fe" />
<img width="188" height="41" alt="image" src="https://github.com/user-attachments/assets/72811597-4594-4474-9813-267bfcc113a3" />
