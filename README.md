# XOR solver

Dead easy.

```python
from xor import xor_solver

# Initialise the solver with the set of characters used to write the plaintext.
x = xor_solver(string.printable)

# Run to spit out a list of (key, plaintext) pairs.
solutions = x.solve(

	"fd3cebb2e009e5a0f537c6bcef38ef85ee24f8bcff14e5b9eb38e3bbe6", #Your ciphertext
	4,                                                            #Your key length
	is_hex=True                                                   #Flag to interpret hex digits as hex.

)

#Show key-value pairs
print solutions

assert("flag{YoungLithePutridDolphin}" in [s[1] for s in solutions])

```
