### APPROACH
The nth hexagonal number is calculated using the given formula `(2n^2-n)`. 

Take `n` as input, substitute it into the formula, and print the result.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    int ans = 2*n*n-n;

    cout << ans;
}
```

### Befunge
```&::*2*\-.@```

---

### SUBMISSION
<img width="536" height="479" alt="image" src="https://github.com/user-attachments/assets/f664c065-e89b-4242-a6fb-4e6142006a3f" />
<img width="644" height="38" alt="image" src="https://github.com/user-attachments/assets/aef8be22-1b48-4cca-814b-df3fd2c6566f" />
<img width="191" height="41" alt="image" src="https://github.com/user-attachments/assets/97213614-0514-4435-93bd-799e36c4c355" />
