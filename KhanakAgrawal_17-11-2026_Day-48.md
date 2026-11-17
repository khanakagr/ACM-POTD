### APPROACH
The goal is to pick matchboxes with the maximum number of matches while staying within the bag's capacity. 

Sort the containers in decreasing order of matches per box (`b`). Start picking boxes from the container with the highest value. 

Take as many as possible, then move to the next container until the bag is full. Keep adding the matches to the total answer.

---

### CODE (C++)
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, m;
    cin >> n >> m;

    vector<pair<int,int>> a(m);

    for(int i=0; i<m; i++) {
        cin >> a[i].first >> a[i].second;
    }

    sort(a.begin(), a.end(), [](pair<int,int> x, pair<int,int> y) {
        return x.second > y.second;
    });

    int ans = 0;

    for(int i=0; i<m; i++) {
        int take = min(n, a[i].first);

        ans += take*a[i].second;
        n -= take;

        if(n==0) break;
    }
    cout << ans;
}
```
---

### SUBMISSION
<img width="537" height="317" alt="image" src="https://github.com/user-attachments/assets/c55ac5d3-34ab-4e15-9ff6-56895b2c6ad0" />
<img width="195" height="42" alt="image" src="https://github.com/user-attachments/assets/454c8a13-fc9f-4077-84be-3db64dcd444d" />
