### APPROACH
The string is decoded by checking each character from left to right. If the character is `.`, it represents `0`. If it is `-`, the next character is checked: `.` represents `1`, while `-` represents `2`.

After decoding a two-character symbol, `i` is increased to skip the character that has already been used.


---

### CODE
<img width="646" height="212" alt="image" src="https://github.com/user-attachments/assets/e1a71c49-e150-49c5-9ef0-d706daee66c5" />
