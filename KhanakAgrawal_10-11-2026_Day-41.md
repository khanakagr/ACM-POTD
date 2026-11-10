### APPROACH
First, the sum of all card values is calculated and divided by `n/2` to get the required sum for each pair. 

Then, two cards whose values add up to this required sum are paired together. 

Their original positions are printed, and the process continues until all cards are paired.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    vector<pair<int,int>> a(n);
    int sum=0;

    for(int i=0; i<n; i++) {
        cin >> a[i].first;
        a[i].second = i+1;
        sum += a[i].first;
    }

    sort(a.begin(), a.end());
    int target = 2*sum/n;
    int l=0, r=n-1;

    while(l<r) {
        cout << a[l].second << " " << a[r].second << endl;
        l++;
        r--;
    }
}
```
---

### SUBMISSION
<img width="434" height="287" alt="image" src="https://github.com/user-attachments/assets/5a320204-785f-4ac7-86f7-69efa8748e9d" />
<img width="190" height="41" alt="image" src="https://github.com/user-attachments/assets/9b57e27c-fc22-476c-bdaa-d018906b4deb" />
