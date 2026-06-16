## Array Traversal Patterns

```python
arr = [10, 20, 30, 40, 50]

# Forward
for val in arr:
    print(val)

# With index
for i, val in enumerate(arr):
    print(f'Index {i}: {val}')

# Reverse
for val in reversed(arr):
    print(val)
```

## Sieve of Eratosthenes

```python
def sieve(limit):
    is_prime = [True] * (limit + 1)
    is_prime[0] = is_prime[1] = False
    for i in range(2, int(limit**0.5) + 1):
        if is_prime[i]:
            for j in range(i*i, limit + 1, i):
                is_prime[j] = False
    return [i for i, v in enumerate(is_prime) if v]

print(sieve(100))
```

Efficient for generating all primes up to a limit. Runs in O(n log log n).
