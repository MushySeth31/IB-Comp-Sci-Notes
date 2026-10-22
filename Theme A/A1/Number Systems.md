# Number Systems
#### A way of writing numbers using specific symbols or digits.

### Types of Number Systems:
- Decimal
- Binary
- Hexadecimal

---

## Decimal
Number system with base value of 10, ranging from 0-9. This is what humans use.

#### Example:
$42_{10}$

#### Expanded:
$(4 \times 10^1) + (2 \times 10^0)$

#### Decimals work in powers of 10.

---

## Binary
Number system with base value of 2, ranging from 0-1. This is what computers use to store, process, and transmit data.

#### Example:
$1011_2$

#### Expanded:
$(1 \times 2^3) + (0 \times 2^2) + (1 \times 2^1) + (1 \times 2^0)$

$= 8 + 0 + 2 + 1$

$= 11_{10}$

#### Binary work in powers of 2.

Binary is used in computers because hardware (transistors) only have two stable states:
- 1 -> High voltage
- 0 -> Low voltage

This links to:
- Logic gates (AND, OR, NOT)
- CPU operations
- Memory storage

Bit converstion:
- 1 bit = 0 or 1
- 1 nibble = 4 bits
- 1 byte = 2 nibbles = 8 bits

---

## Hexadecimal
Number system with base value of 16, ranging from 0-15. Hex is a shortcut for binary.

Digits from 10-15 are represented as A-F:
- A = 10
- B = 11
- C = 12
- D = 13
- E = 14
- F = 15

#### Example:
$FF_{16}$

#### Expanded:
$(15 \times 16^1) + (15 \times 16^0)$

$= 15 \times 16 + 15 \times 1$

$= 240 + 15$

$= 255_{10}$

#### Hexadecimal works in powers of 16.

Hexadecimal is used because as binary gets long, it becomes hard to read. Binary is grouped into 4 bits (1 nibble) and converted into hex.

#### Example:
$1111000010101101_2$

Group into 4 bits:

$1111 0000 1010 1101$

Convert each group:

| Binary | Hex |
|----------|----------|
| 1111   | F   |
| 0000   | 0   |
| 1010   | A   |
| 1101   | D   |

So:

$1111000010101101_2 = F0AD_{16}$

----
