### APPROACH
The expression contains numbers `1`, `2`, and `3` separated by `+` signs. First, a frequency array counts how many times each number appears. 

Then, the numbers are printed in increasing order according to their frequencies, with `+` signs between them. 

This produces the required sorted expression.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
	string s;
	cin >> s;
	
	vector<int> freq(4, 0);
	
	for(char ch : s) {
	    if(ch != '+') {
	        freq[ch - '0'] ++;
	    }
	}
	
	bool first = true;
	
	for(int i=1; i<=3; i++) {
	    while(freq[i]--) {
	        if(!first) cout << '+';
	        cout << i;
	        first = false;
	    }
	}
}
```

---

### SUBMISSION
<img width="533" height="317" alt="image" src="https://github.com/user-attachments/assets/1320247a-b9ce-42c1-9873-d4be7fae9140" />
<img width="213" height="46" alt="image" src="https://github.com/user-attachments/assets/d4c33e5d-6345-4dda-bc86-e04fe27ba02c" />
