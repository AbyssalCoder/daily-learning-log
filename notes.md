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

## Binary Search

```python
def binary_search(arr, target):
    lo, hi = 0, len(arr) - 1
    while lo <= hi:
        mid = (lo + hi) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            lo = mid + 1
        else:
            hi = mid - 1
    return -1

sorted_arr = [1, 3, 5, 7, 9, 11]
print(binary_search(sorted_arr, 7))  # 3
```

Requires sorted input. Time complexity: O(log n).

## Bolt.new — Full-Stack App Generator

Browser-based AI that generates and deploys full-stack apps.

### Strengths
- Generates complete projects (frontend + backend)
- Deploys instantly
- Uses WebContainers (runs Node.js in browser)
- Great for prototyping

### Limitations
- Can struggle with complex requirements
- Limited backend options
- Code quality varies

## Git Rebase

Rebase replays your commits on top of another branch.

```bash
git checkout feature
git rebase main
```

### Merge vs Rebase
| Merge                  | Rebase                  |
|------------------------|-------------------------|
| Creates merge commit   | Linear history          |
| Preserves history      | Rewrites commit hashes  |
| Safe for shared branch | Only for local branches |

**Golden rule:** Never rebase commits that have been pushed to a shared branch.

## UDP — User Datagram Protocol

- **Connectionless** — no handshake
- **Unreliable** — no delivery guarantee
- **Fast** — minimal overhead

### Use cases
- Video streaming
- Online gaming
- DNS queries
- VoIP

### TCP vs UDP
| Feature      | TCP          | UDP          |
|-------------|-------------|-------------|
| Connection   | Yes          | No           |
| Reliability  | Guaranteed   | Best effort  |
| Speed        | Slower       | Faster       |
| Ordering     | Yes          | No           |

## REST API Principles

1. **Client-Server** separation
2. **Stateless** — each request carries all needed info
3. **Uniform Interface** — standard HTTP methods
4. **Resource-based** — URIs identify resources

### Example endpoints
```
GET    /api/users          # List users
GET    /api/users/42       # Get user 42
POST   /api/users          # Create user
PUT    /api/users/42       # Replace user 42
DELETE /api/users/42       # Delete user 42
```

Always use nouns for resources, not verbs.

## Linear Search

```python
def linear_search(arr, target):
    for i, val in enumerate(arr):
        if val == target:
            return i
    return -1

nums = [4, 2, 7, 1, 9]
print(linear_search(nums, 7))  # 2
print(linear_search(nums, 5))  # -1
```

Time complexity: O(n). Works on unsorted arrays.
