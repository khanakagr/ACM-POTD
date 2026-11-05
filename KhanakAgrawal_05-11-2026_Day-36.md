### APPROACH
The total cost of buying `w` bananas is calculated using the formula `k*w*(w+1)/2`, since the price increases with each banana. 

The amount the soldier needs to borrow is the total cost minus the money he already has (`n`). 

If he has enough money, the answer is `0`. Finally, the required amount is printed.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
	long long k, n, w;
	cin >> k >> n >> w;
	
	long long total = k*w*(w+1)/2;

    cout << max(0LL, total-n) << endl;
}
```
---

### SUBMISSION
<img width="496" height="135" alt="image" src="https://github.com/user-attachments/assets/1a104979-8ea5-4fda-b4f4-e97a866fea45" />
<img width="190" height="42" alt="image" src="https://github.com/user-attachments/assets/22d5b64e-f9db-47a4-b4a6-78a9705ad9ee" />
