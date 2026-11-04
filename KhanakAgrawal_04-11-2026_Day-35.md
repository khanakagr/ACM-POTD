### APPROACH
A frequency array of size `26` is used to keep track of all the letters of the alphabet. 

Each character in the string is converted to lowercase, and its corresponding position in the array is updated. 

Finally, the array is checked to see if every letter has appeared at least once. If all `26` letters are present, print `YES`; otherwise, print `NO`.

---

### CODE (C++)
```
#include <iostream>
using namespace std;

int main() {
	long long n,idx=0;
	cin >> n;
	string str;
	cin >> str;
	
	int f[26]={0};
    for(int i=0;str[i]!='\0';i++) {
        char ch=tolower(str[i]);
        if(ch>='a' and ch<='z') {
            idx=ch-'a';
            f[idx]++;
        }
    }
    
	bool isPanagram=true;
	for(int i=0;i<26;i++) {
        if(f[i]==0) {
            isPanagram=false;
            break;
        } 
    }
    
    if(isPanagram) cout << "YES" << endl;
    else cout << "NO" << endl;
}
```
---

### SUBMISSION
<img width="454" height="315" alt="image" src="https://github.com/user-attachments/assets/36156840-1b2a-4a26-b56f-08cc9ef5a127" />
<img width="190" height="42" alt="image" src="https://github.com/user-attachments/assets/a2084aad-426c-4465-8544-c5c99b50c9ec" />
