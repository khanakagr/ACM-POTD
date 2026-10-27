### APPROACH
The sum of all episode numbers from 1 to n is calculated using the formula `n*(n+1)/2`. Each episode number present in the input is subtracted from this sum. 

The remaining value gives the number of the missing episode. `long long` is used to avoid integer overflow when calculating the sum.  

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    long long n;
    cin >> n;

    long long sum = n*(n+1)/2;

    for(int i=0; i<n-1; i++) {
        long long x;
        cin >> x;
        sum -= x;
    }
    cout << sum;
}
```
---

### SUBMISSION
<img width="487" height="212" alt="image" src="https://github.com/user-attachments/assets/5664745a-0f3d-4fd1-ac81-d1b9a1110374" />
<img width="215" height="44" alt="image" src="https://github.com/user-attachments/assets/43b3ea8d-f2dc-44a6-a7bc-584df34a3fd0" />
