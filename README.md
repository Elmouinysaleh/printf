# printf
0x11. C - printf alx team project

#### Authorized functions and macros

------------


write (man 2 write)
malloc (man 3 malloc)
free (man 3 free)
va_start (man 3 va_start)
va_end (man 3 va_end)
va_copy (man 3 va_copy)
va_arg (man 3 va_arg)

------------

**Prototype:** int _printf(const char *format, ...);
**Use - General:** _printf("format string", var1, var2, ...);


**The flag characters**

|**Flag**| Description  |
|--|--|
|**#**| For **o** conversions the first character of the output string is made zero (by prefixing a 0 if it was not zero already).  For **x** and **X** conversions, a nonzero result has the string "**0x**" or "**0X**" respectively added. |
|**0**| (Not implemented yet) The  value should be zero padded. For **d**, **i**, **o**, **u**, **x**, and **X** the converted value is padded on the left with zeros. If the 0 and **-** flags both appear,the **0** flag is ignored. If a precision is given with a numeric conversion, the **0** flag is ignored.|
|**-**|(Minus sign, not implemented yet) The converted value is to be left adjusted on the field boundary, (Default is right justification) and  padded  with  blanks  in  the right rather than on the left with blanks or zeros. This flag overrides **0** if both are given.|
|' '| (Blank Space) The argument is padded with a single blank space before a positive number or empty string produced by a signed conversion.|
|**+**| A sign (+ or -) should always be placed before a number produced with a signed conversion.  By default, only negative numbers have this sign.|


**The precision**

 An  optional  precision,  in  the  form  of a period ('.')  followed by an optional decimal digit string.  A negative precision is taken  as  if  the precision were omitted.  This gives the minimum number of digits to appear for d, i, o, u, x, and X conversions,  or the  maximum  number of characters to be printed from a string for s and S conversions. A character * can be used instead of a  decimal string. In this case, an argument passed to the function will be taken as the precision value.

    printf("%.3d", num);

  or

    printf("%.*d", precision, num);
    
**The length modifiers**

|Modifier| Description |
|--|--|
|**l**| An integer conversion to a **long int** or **unsigned long int** argument.  |
|**h**| An integer conversion to a **short int** or **unsigned short int** argument. |

**The conversion specifier**

|Specifier| Description |
|--|--|
|**d, i**|The argument **int** is converted to a signed decimal notation. If precision is present,it gives the minimum number of digits that must appear; if the converted value requires fewer digits, then it is padded with zeros on the left. Default precision is 1.|
|**o, u, x, X**|The argument is converted to unsigned octal (**o**), unsigned decimal (**u**), or unsigned hexamedical (**x** and **X**) notation. The letters abcdef are used for x conversion and the letters ABCDEF are used for X conversion. If precision is present, it will give  the  minimum  number  of  digits  that  must appear; if the converted value requires fewer digits, then it will be padded with zeros. By default the precision is 1.  |
|**c**|The  int argument is converted to an unsigned char and the resulting character is written. The representation of characters is based off the ASCII coding.|
|**s**|The argument received is expected to be a pointer type char * to an array of characters.  Characters from this array are printed up  to  (but  not including) a null byte  (**'\0'**).  If precision is specified, then this will determine how many characters are taken into account for printing.|
|**p**|A void * pointer argument is printed as hexadecimal in lower caps representing an adress in memory.|
|**%**|A  ' **%** ' character is written and no conversion is made. The specification is as follows: **%%**. |
|**b**|The argument is converted to an unsigned int value and then operated to get its binary representation (base 2).|
|**S**| The  argument  received  is expected to be a pointer type char * to an array of characters.  Characters from this array are printed up to (but not including) a null byte  ('\0').  Non printable characters (0 < ASCII value < 32 or >= 127) are printed this way: \x, followed by  the  ASCII  code value in hexadecimal (upper case - always 2 characters). |
|**r**|The  argument received is expected to be a pointer type char * to an array of characters.  Characters from this array are printed in reverse order up to (but not including) a null byte  ('\0').  |
|**R**|The argument received is expected to be a pointer type char * to an array of characters.  Characters from this array  are  encoded  to  ROT13  and printed in order up to (but not including a null byte  ('\0').  |




## Tasks required for this project


------------

0. ### I am not going anywhere. You can print that wherever you want to. I'm here and I am a Spur for life1.  I am not going anywhere. You can print that wherever you want to. I'm here and I am a Spur for life. 
Write a function that produces output according to a format.
Handle the following conversion specifiers:
- c
- s
- %

1. ### Education is when you read the fine print. Experience is what you get if you dont
Handle the following conversion specifiers:
- d
- i

2. ###### With a face like mine, I do better in print
Handle the following conversion specifiers:
- b

3. ###### What one has not experienced, one will never understand in print
Handle the following conversion specifiers:
- u
- x
- o
- x
- X

4. ###### Nothing in fine print is ever good news
Use a local buffer of 1024 chars in order to call write as little as possible.

5. ###### My weakness is wearing too much leopard print
- S : prints the string.
- Non printable characters (0 < ASCII value < 32 or >= 127) are printed this way: \x, followed by the ASCII code value in hexadecimal (upper case - always 2 characters).

6. ###### How is the world ruled and led to war? Diplomats lie to journalists and believe these lies when they see them in print
Handle the following conversion specifier: p

7. ###### The big print gives and the small print takes away
Handle the following flag characters for non-custom conversion specifiers:
- ´+´
- space
- ´#´ 

8. ###### Sarcasm is lost in print
Handle the following length modifiers for non-custom conversion specifiers:
- l
- h
Conversion specifiers to handle: d, i, u, o, x, X

9. ###### Print some money and give it to us for the rain forests
Handle the field width for non-custom conversion specifiers.

10. ###### The negative is the equivalent of the composer's score, and the print the performance
Handle the precision for non-custom conversion specifiers.

11. ###### It's depressing when you're still around and your albums are out of print
Handle the 0 flag character for non-custom conversion specifiers.

12. ###### Every time that I wanted to give up, if I saw an interesting textile, print what ever, suddenly I would see a collection
Handle the - flag character for non-custom conversion specifiers.

13. ###### Print is the sharpest and the strongest weapon of our party
Handle the following custom conversion specifier:
 - r : prints the reversed string

14. ###### [The flood of print has turned reading into a process of gulping rather than savoring] 
Handle the following custom conversion specifier:
- R: prints the rot13'ed string

15. ###### *
All the above options work well together.
