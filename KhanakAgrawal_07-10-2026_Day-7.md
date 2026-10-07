### APPROACH
I stored the time taken between each pair of consecutive cities in an array. Then, I took the starting city `a` and ending city `b`.

I started from `a` and kept moving towards `b`, adding the travel time between each pair of cities to `sum`. Once I reached `b`, `sum` gives the total travel time between the two cities.

Since there are `n` cities, there are `n-1` travel times between them.

---
### CODE
<img width="719" height="350" alt="image" src="https://github.com/user-attachments/assets/3c85fcc4-6788-46d0-8223-31040054d7c6" />
