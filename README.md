# Caesars-Cipher

One of the simplest and most widely known ciphers is a Caesar cipher, also known as a shift cipher. In a shift cipher the meanings of the letters are shifted by some set amount.

A common modern use is the ROT13 cipher, where the values of the letters are shifted by 13 places. Thus A ↔ N, B ↔ O and so on.

Write a function which takes a ROT13 encoded string as input and returns a decoded string.

All letters will be uppercase. Do not transform any non-alphabetic character (i.e. spaces, punctuation), but do pass them on.

## Demo






## Getting Started 🖥️

To use Caesars Cipher , follow these steps:

Download or copy the code from this repository.

Open the index.html file in a web browser.




## Technologies Used
- JavaScript
- HTML
- CSS


## Acknowledgments
This project was developed as an Certification task for FreeCodeCamp- Javascript and Data Structure Certification.


## Tests

rot13("SERR PBQR PNZC") should decode to the string FREE CODE CAMP

Passed:rot13("SERR CVMMN!") should decode to the string FREE PIZZA!

Passed:rot13("SERR YBIR?") should decode to the string FREE LOVE?

Passed:rot13("GUR DHVPX OEBJA SBK WHZCF BIRE GUR YNML QBT.") should decode to the string THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG.

## About Freecodecamp Certification

FreeCodeCamp Palindrome Checker - JavaScript Algorithms and Data Structures Projects

https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects/caesars-cipher

One of the simplest and most widely known ciphers is a Caesar cipher, also known as a shift cipher. In a shift cipher the meanings of the letters are shifted by some set amount.

A common modern use is the ROT13 cipher, where the values of the letters are shifted by 13 places. Thus A ↔ N, B ↔ O and so on.

Write a function which takes a ROT13 encoded string as input and returns a decoded string.

All letters will be uppercase. Do not transform any non-alphabetic character (i.e. spaces, punctuation), but do pass them on.



## Solution

function rot13(str) {
 return str.replace(/[A-Z]/g, L =>
    String.fromCharCode((L.charCodeAt(0) % 26) + 65)  
  ); 
}
rot13("SERR PBQR PNZC");

### Explanation
As you can notice, each number in the range of [65 - 90] maps to a unique number between [0 - 25].
You might have also noticed that each given number (e.g. 65) maps to another number (e.g. 13) which can be used as an offset value
(i.e. 65 + OFFSET) to get the ROT13 of the given number.

E.g. 65 maps to 13 which can be taken as an offset value and added to 65 to give 78.

    [A]  65 % 26 ⇔ 13 + 65 =  78 [N]
    
    [B]  66 % 26 ⇔ 14 + 65 =  79 [O]
    
    [C]  67 % 26 ⇔ 15 + 65 =  80 [P]
    
    [D]  68 % 26 ⇔ 16 + 65 =  81 [Q]
    
    [E]  69 % 26 ⇔ 17 + 65 =  82 [R]
    
    [F]  70 % 26 ⇔ 18 + 65 =  83 [S]
    
    [G]  71 % 26 ⇔ 19 + 65 =  84 [T]
    
    [H]  72 % 26 ⇔ 20 + 65 =  85 [U]
    
    [I]  73 % 26 ⇔ 21 + 65 =  86 [V]
    
    [J]  74 % 26 ⇔ 22 + 65 =  87 [W]
    
    [K]  75 % 26 ⇔ 23 + 65 =  88 [X]
    
    [L]  76 % 26 ⇔ 24 + 65 =  89 [Y]
    
    [M]  77 % 26 ⇔ 25 + 65 =  90 [Z]
    
    [N]  78 % 26 ⇔  0 + 65 =  65 [A]
    
    [O]  79 % 26 ⇔  1 + 65 =  66 [B]
    
    [P]  80 % 26 ⇔  2 + 65 =  67 [C]
    
    [Q]  81 % 26 ⇔  3 + 65 =  68 [D]
    
    [R]  82 % 26 ⇔  4 + 65 =  69 [E]
    
    [S]  83 % 26 ⇔  5 + 65 =  70 [F]
    
    [T]  84 % 26 ⇔  6 + 65 =  71 [G]
    
    [U]  85 % 26 ⇔  7 + 65 =  72 [H]
    
    [V]  86 % 26 ⇔  8 + 65 =  73 [I]
    
    [W]  87 % 26 ⇔  9 + 65 =  74 [J]
    
    [X]  88 % 26 ⇔ 10 + 65 =  75 [K]
    
    [Y]  89 % 26 ⇔ 11 + 65 =  76 [L]
    
    [Z]  90 % 26 ⇔ 12 + 65 =  77 [M]
