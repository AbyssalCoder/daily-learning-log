## 2026-06-04

Practiced Dictionary Practice with some exercises.

This will be useful for the upcoming project.

## 2026-06-04

Spent some time studying Claude Code today.

Understanding the 'why' behind this made everything clearer.


<!-- fixed typo -->

## Factorial

```python
# Iterative
def factorial_iter(n):
    result = 1
    for i in range(2, n + 1):
        result *= i
    return result

# Recursive
def factorial_rec(n):
    return 1 if n <= 1 else n * factorial_rec(n - 1)

print(factorial_iter(5))  # 120
```

## Exception Handling

```python
def safe_divide(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        print('Cannot divide by zero!')
        return None
    except TypeError as e:
        print(f'Type error: {e}')
        return None
    finally:
        print('Division attempted.')

print(safe_divide(10, 3))
print(safe_divide(10, 0))
```

`finally` always runs — useful for cleanup.


<!-- fixed typo -->


<!-- fixed typo -->

## 2026-07-21

Practiced Factorial with some exercises.

The comparison between approaches was really helpful.

## Palindrome Check

```python
def is_palindrome(s):
    s = s.lower().replace(' ', '')
    return s == s[::-1]

print(is_palindrome('racecar'))  # True
print(is_palindrome('hello'))    # False
```

Slicing `[::-1]` reverses the string in one step.

## 2026-08-08

Deep dive into File Handling.

The hands-on practice made the theory click.

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
