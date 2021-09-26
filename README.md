# Password Maker
---
### Why?
When the password policy has you down, this script has you covered. It generates a strong passphrase out of your OS's weak password library, I live for irony. Length in terms of words can be arbitrary, but 3 is strongly recommended by me.

### How?
Your OS probably has a dictionary file or more at `/usr/share/dict` ... and probably other directories, I'll get to that when I'm not the only one using this script. A random dictionary file is picked if there's more than one.

This script uses the bash varible `$RANDOM` to generate a number and pick words randomly from the list, also randomly appending the symbols in `./symbols` after the words. Symbols appear after words depending on whether `$RANDOM` is odd. 

### Installation
Run `./install`. Don't worry, It's just copying `pmk` to `/usr/local/bin`. I don't recommend this. Just run it from the working directory.

### Usage
```bash
pmk [NO_OF_WORDS] [MAX_NUM_LENGTH]
```
 - `NO_OF_WORDS` : Number of passphrase parts.
 - `MAX_NUM_LENGTH` : Number of digits on the prefix.

### Extra Credits
Create your own dict file. It's literally just a newline-separated list of alphanumeric characters.

### Disclaimer
Use MFA alongside this. Seriously. It can't be hard to brute force.
