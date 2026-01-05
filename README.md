
# Caesar Cipher Decoder in C

This project implements a Caesar cipher decoder written in C.  
It reads an encrypted message from a file, computes a deterministic shift value based on a user-provided key, and decodes the ciphertext into readable plaintext.

The program demonstrates file I/O, string manipulation, bitwise operations, and modular arithmetic in C.

## Overview

The Caesar cipher is a classical substitution cipher where each lowercase letter is shifted by a fixed number of positions in the alphabet.

In this implementation:

- The encrypted text is read from a local file
- The decoding shift is derived from a user-provided key
- Only lowercase alphabetic characters are decoded
- Non-alphabet characters remain unchanged
- Shifting wraps around the alphabet using modular arithmetic

## How the Decoder Works

The decoding process follows three main steps:

1. Read the encrypted message from a file named cipher.txt
2. Prompt the user for a key string
3. Compute a shift value by applying a bitwise XOR across all characters in the key
4. Decode each lowercase letter by applying a circular right shift

The final decoded message is printed to standard output.

## Repository Contents

decode.c  
    Main program source file implementing file input, key handling, shift calculation, and decoding logic

cipher.txt  
    Input file containing the encrypted message

decode  
    Compiled executable (if built locally)

decode.o, decode.s, decode.i  
    Intermediate build artifacts (optional, compiler-generated)

execfile_contents.txt  
    Runtime inspection output (optional)

objectfile_contents.txt  
    Object file inspection output (optional)

myfortune.txt  
    Sample plaintext output (optional)

## Build Instructions

Compile the program using a standard C compiler:

    gcc decode.c -o decode

## Running the Program

Ensure cipher.txt exists in the current directory, then run:

    ./decode

You will be prompted to enter a key string.  
The program will then display both the original ciphertext and the decoded plaintext.

## Notes on Decoding Logic

- Only characters in the range a–z are shifted
- Shift values are always between 1 and 25
- The shift value is deterministic for a given key
- Decoding is performed in-place on the input buffer

## Version Control Recommendations

The following files are generated artifacts and should not be committed:

- decode
- decode.o
- decode.i
- decode.s

It is recommended to include these entries in a .gitignore file.

## License

This project is intended for educational and demonstration purposes.

