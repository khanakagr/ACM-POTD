### APPROACH
The string is traversed to check for 7 or more consecutive identical characters. 

A counter `cnt` keeps track of the current consecutive sequence. 

If the current character is equal to the next character, increment `cnt`; otherwise, reset it to 1. 

If `cnt` reaches 7, print `YES` and stop. If no such sequence is found, print `NO`.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
	string x;
	cin >> x;
	int cnt=1;
	
	int n=x.size();
	
	for(int i=0;i<n;i++) {
	    if(x[i]==x[i+1]) {
	        cnt++;
	        if(cnt>=7) {
	            cout << "YES" << endl;
	            return 0;
	        }
	    } else {
	        cnt=1;
	    }
	}
	cout << "NO" << endl;
}
```
---

### SUBMISSION
<img width="481" height="258" alt="image" src="https://github.com/user-attachments/assets/408fb784-8a0e-49eb-bcb3-2a7d96288ab3" />
<img width="191" height="43" alt="image" src="https://github.com/user-attachments/assets/72205bea-f1d2-442f-abd7-514500092a52" />
