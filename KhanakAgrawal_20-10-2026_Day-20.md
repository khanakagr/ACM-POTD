### APPROACH
The first character of the word is converted to uppercase using toupper(), while the remaining characters stay unchanged. The modified word is then printed.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
	string s;
	cin >> s;
	
	s[0] = toupper(s[0]);
	
	cout << s << endl;
	return 0;
}
```

---

### SUBMISSION
<img width="547" height="164" alt="image" src="https://github.com/user-attachments/assets/9538505b-c122-45b9-881f-6ef6f201c5b0" />
<img width="210" height="45" alt="image" src="https://github.com/user-attachments/assets/daef1f07-86c4-43af-9b87-210762bcca4f" />
