# LEETCODE-Arrays-75
---

## Example 1

```
nums = [2, 0, 2, 1, 1, 0]
low = 0, mid = 0, high = 5
```

| Step | Action                               | low | mid | high | Array |
| :--: | :----------------------------------- | :-: | :-: | :--: | :---- |
|   1  | nums\[mid]=2 → swap mid↔high, high-- |     |     |      |       |

```
                      | 0   | 0   | 4    | [0, 0, 2, 1, 1, **2**]        |
```

\| 2    | nums\[mid]=0 → swap low↔mid, low++, mid++
\| 1   | 1   | 4    | \[**0**, 0, 2, 1, 1, 2]        |
\| 3    | nums\[mid]=0 → swap low↔mid, low++, mid++
\| 2   | 2   | 4    | \[0, **0**, 2, 1, 1, 2]        |
\| 4    | nums\[mid]=2 → swap mid↔high, high--
\| 2   | 2   | 3    | \[0, 0, **1**, 1, **2**, 2]    |
\| 5    | nums\[mid]=1 → mid++
\| 2   | 3   | 3    | \[0, 0, 1, **1**, 2, 2]       |
\| 6    | nums\[mid]=1 → mid++
\| 2   | 4   | 3    | \[0, 0, 1, 1, 2, 2]           |
|Done | mid (4) > high (3)        |     |     |      | \[0, 0, 1, 1, 2, 2]           |

Sorted result: `[0, 0, 1, 1, 2, 2]`

---

## Example 2

```
nums = [1, 2, 0]
low = 0, mid = 0, high = 2
```

| Step | Action                               | low | mid | high | Array          |
| :--: | :----------------------------------- | :-: | :-: | :--: | :------------- |
|   1  | nums\[mid]=1 → mid++                 |  0  |  1  |   2  | \[**1**, 2, 0] |
|   2  | nums\[mid]=2 → swap mid↔high, high-- |     |     |      |                |

```
                      | 0   | 1   | 1    | [1, **0**, **2**]       |
```

\| 3    | nums\[mid]=0 → swap low↔mid, low++, mid++
\| 1   | 2   | 1    | \[**0**, **1**, 2]       |
|Done | mid (2) > high (1)        |     |     |      | \[0, 1, 2]               |

Sorted result: `[0, 1, 2]`

---
