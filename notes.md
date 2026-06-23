## File Handling in Python

```python
# Writing
with open('output.txt', 'w') as f:
    f.write('Hello, file!\n')
    f.write('Second line\n')

# Reading
with open('output.txt', 'r') as f:
    content = f.read()
    print(content)

# Reading line by line
with open('output.txt', 'r') as f:
    for line in f:
        print(line.strip())
```

Always use `with` statements — they handle closing automatically.

## Python Dictionary Practice

```python
# Word frequency counter
text = 'the cat sat on the mat the cat'
freq = {}
for word in text.split():
    freq[word] = freq.get(word, 0) + 1
print(freq)  # {'the': 3, 'cat': 2, 'sat': 1, 'on': 1, 'mat': 1}

# Using collections.Counter
from collections import Counter
print(Counter(text.split()))
```
