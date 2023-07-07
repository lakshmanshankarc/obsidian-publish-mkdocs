# Bit Manipulation

[Python Bitwise Operators - GeeksforGeeks](https://www.geeksforgeeks.org/python-bitwise-operators/)

Page contains info about bit manipulation 

1. AND 
2. OR
3. XOR
4. NOR
5. N AND

## Bit wise AND (**`&`**):

And output true if both values are true

## Truth Table

$a * b$  

| A | B | A * B |
| --- | --- | --- |
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

## Code

```python
print( 1 and 0) #normal and
print( 1 & 0) # Bitwise and
```

- 

## Bit wise OR (**`|`**):

And output true if any of the values are true

## Truth Table

$a * b$  

| A | B | A * B |
| --- | --- | --- |
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

## Code

```python
print( 1 or 0) #normal and
print( 1 | 0) # Bitwise and
```

## Bit wise XOR (`^`):

$a ⊕ b$

Result is 1 if any of the value is one but not 2 of them

<aside>
💡 xor is a logical operation works on the bits rather like and or operaion

</aside>

## Truth Table

$a * b$  

| A | B | A * B |
| --- | --- | --- |
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

<aside>
💡 1 ^ even → will return 1+even

</aside>

<aside>
💡 1 ^ odd ⇒ will return 1 - odd

</aside>

## Code

```python
print( 1 ^ 2) # 3
print( 1 ^ 3) # 2
```

## Example

```python
1 ^ 3 = > 2

0000 0001 -> 1
0000 0011 -> 3
----------
0000 0010 -> 2
----------
```

## Bit wise NOT (`~`):

$$
! a 
$$

Result is 1 if any of the value is one but not 2 of them

<aside>
💡 xor is a logical operation works on the bits rather like and or operaion

</aside>

## Truth Table

$a * b$  

| A | B | A * B |
| --- | --- | --- |
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 0 |

<aside>
💡 1 ^ even → will return 1+even

</aside>

<aside>
💡 1 ^ odd ⇒ will return 1 - odd

</aside>

## Code

```python
print( !False) # True
```

<aside>
💡 Just << and >> are remaining which is left and right shift

</aside>

<i> helo </i>

