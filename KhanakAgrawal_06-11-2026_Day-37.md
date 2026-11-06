### APPROACH
The maximum number of days Vasya can wear different coloured socks is the minimum of the two sock counts. These socks are used first, one of each colour per day. 

After that, only one colour remains, so the remaining socks are used to calculate the number of days he can wear matching socks by dividing their count by `2`. 

Finally, both answers are printed.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
	int a,b,diff=0,same=0;
	cin >> a >> b;
	
	diff=min(a,b);
	a-=diff;
	b-=diff;
	
	if(a>0) same=a/2;
	else if(b>0) same=b/2;

	cout << diff << " " << same << endl;
}
```
---

### SUBMISSION
<img width="485" height="188" alt="image" src="https://github.com/user-attachments/assets/d8ca2423-d08a-4a38-8a3a-9aa98ab19812" />
<img width="187" height="39" alt="image" src="https://github.com/user-attachments/assets/3492e003-2728-4159-baa8-545c5fcafb79" />
