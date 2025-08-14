## 💡 Computer Mathematics (OBJ 1.7)

This section covers binary and decimal conversions, which are fundamental for understanding IP addressing. The maximum value for an 8-bit binary number (all 1s) is 255. This is why IPv4 octets range from 0-255.

✅ **Decimal (Base-10) vs. Binary (Base-2)**
- **Decimal (Base-10):** How humans count (0-9 per digit).
- **Binary (Base-2):** How computers count (0 or 1 per digit).
  - Computers understand "on" (1) or "off" (0).
  - IPv4 addresses, though displayed in decimal, are processed by computers in binary.

✅ **Binary to Decimal Conversion**
- **Concept:** Each binary digit (bit) represents a power of 2.
- **Conversion Table (8-bit Octet):**
  `128 | 64 | 32 | 16 | 8 | 4 | 2 | 1`
- **Process:**
  - 1. Write the binary number under the conversion table, aligning from right to left.
  - 2. Add the decimal values from the top row where there is a `1` in the binary number.
- **Example:** Binary `10010110`
  `128 | 64 | 32 | 16 | 8 | 4 | 2 | 1`
  `  1 |  0 |  0 |  1 | 0 | 1 | 1 | 0`
  `128 + 16 + 4 + 2 = 150`

✅ **Decimal to Binary Conversion**
- **Concept:** Repeatedly subtract the largest possible power of 2 from the decimal number.
- **Process:**
  - 1. Start with the decimal number.
  - 2. From left to right (128 down to 1), ask: "Can I subtract this power of 2 from my current number?"
  - 3. If **Yes**: Place a `1` under that power of 2, and subtract the value from your current number.
  - 4. If **No**: Place a `0` under that power of 2, and keep your current number.
  - 5. Continue until you reach the `1`'s place.
- **Example:** Convert Decimal `167` to Binary
  - `167 - 128 = 39` (Place `1` under 128)
  - `39 - 64` (No) (Place `0` under 64)
  - `39 - 32 = 7` (Place `1` under 32)
  - `7 - 16` (No) (Place `0` under 16)
  - `7 - 8` (No) (Place `0` under 8)
  - `7 - 4 = 3` (Place `1` under 4)
  - `3 - 2 = 1` (Place `1` under 2)
  - `1 - 1 = 0` (Place `1` under 1)
  - Result: `10100111`

✅ **Verification**
- To check your work, perform the reverse conversion. If converting decimal to binary, convert the resulting binary back to decimal. If the numbers match, your conversion is correct.
- Example: `10100111` (binary) = `128 + 32 + 4 + 2 + 1 = 167` (decimal). Correct!