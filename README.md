# Lab-Exercise---1---Caesar-Cipher
## AIM:
To encrypt and decrypt the given message by using Ceaser Cipher encryption algorithm.

## ALGORITHM:
1 Design of Caeser Cipher algorithnm
2 Implementation using C or pyhton code
3 In Ceaser Cipher each letter in the plaintext is replaced by a letter some fixed number of positions down the alphabet.
4 For example, with a left shift of 3, D would be replaced by A, E would become B, and so on.
5 The encryption can also be represented using modular arithmetic by first transforming the letters into numbers, according to the scheme, A = 0, B = 1, Z = 25.
6 Encryption of a letter x by a shift n can be described mathematically as, En(x) = (x + n) mod26
7 Decryption is performed similarly, Dn (x)=(x - n) mod26

## CODE:
```
def caesae_cipher(text,shift):
  result=""
  for char in text:
    if char.isupper():
      result+=chr((ord(char)-ord('A')+shift)%26+ord('A'))
    elif char.islower():
      result+=chr((ord(char)-ord('A')+shift)%26+ord('a'))
    else:
      result+=char
  return result
choice = input("Encrypt or decrypt? (e/d): ").lower()
message=input("Enter your message: ")
shift=int(input("Enter shift value: "))%26
if choice == "d":
  shift=-shift
elif choice!= "e":
  print("Invalid Choice.")
else:
  print("Result:", caesar_cipher(message,shift))
  raise SystemExit
print("Result:", caesar_cipher(message,shift))
```

## OUTPUT:


## RESULT:
The program is executed successfully.

