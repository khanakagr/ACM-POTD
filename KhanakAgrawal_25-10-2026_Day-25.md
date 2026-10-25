### APPROACH
The apple numbers liked by Arthur and Alexander are stored in separate vectors. Each apple from 1 to n is checked against Arthur's list. 

If Arthur likes it, 1 is printed; otherwise, 2 is printed, assigning the apple to Alexander. 

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
	int n, a, b;
	cin >> n >> a >> b;
	
	vector<int> arthur(a), alexander(b);
	
	for(int i=0; i<a; i++) cin >> arthur[i];
	for(int i=0; i<b; i++) cin >> alexander[i];
	
	for(int i=1; i<=n; i++) {
	    if(find(arthur.begin(), arthur.end(), i) != arthur.end()) cout << 1 << " ";
      else cout << 2 << " ";
	}
}
```
---

### SUBMISSION
<img width="635" height="218" alt="image" src="https://github.com/user-attachments/assets/f74188bf-0602-449c-a987-7ac170c2d5ce" />
<img width="217" height="47" alt="image" src="https://github.com/user-attachments/assets/5a2bb8d9-a57e-4721-8453-99f2bf65cb54" />
