# Ex-4 Rail-Fence-Program

### Name: Manickam Subbu
### Reg No: 212223060147

# IMPLEMENTATION OF RAIL FENCE – ROW & COLUMN TRANSFORMATION TECHNIQUE

# AIM:

# To write a C program to implement the rail fence transposition technique

# DESCRIPTION:

In the rail fence cipher, the plain text is written downwards and diagonally on successive "rails" of an imaginary fence, then moving up when we reach the bottom rail. When we reach the top rail, the message is written downwards again until the whole plaintext is written out. The message is then read off in rows.

# ALGORITHM:

STEP-1: Read the Plain text.
STEP-2: Arrange the plain text in row columnar matrix format.
STEP-3: Now read the keyword depending on the number of columns of the plain text.
STEP-4: Arrange the characters of the keyword in sorted order and the corresponding columns of the plain text.
STEP-5: Read the characters row wise or column wise in the former order to get the cipher text.

# PROGRAM
```
def rail_fence_encrypt(message, rails):
    fence = ['' for _ in range(rails)]

    row = 0
    direction = 1

    print("Original Message:", message)

    for ch in message:
        fence[row] += ch

        row += direction

        if row == rails - 1 or row == 0:
            direction = -direction

    encrypted = ''.join(fence)

    print("Rails used:", rails)

    print("Encrypted text:", encrypted)

message = input("Enter a Secret Message: ")
rails = int(input("Enter number of rails: "))

rail_fence_encrypt(message, rails)
```


# OUTPUT
<img width="1919" height="798" alt="image" src="https://github.com/user-attachments/assets/7088a6bc-f7a4-4c70-a7e7-67866bbed918" />

         

# RESULT
         The program is executed successfully
