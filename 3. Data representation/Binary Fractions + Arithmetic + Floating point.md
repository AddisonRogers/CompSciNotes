
# Binary Arithmetic


## Binary Addition

> [!NOTE] Really
> If you don’t know how to do binary addition you are already kinda screwed.

Binary addition may have an error when you are trying to save a byte that is more than 8 bits. This is known as an overflow error.

## Binary Multiplication

Binary multiplication is fairly easy as long as you consider it correctly.
![[Pasted image 20220510234143.png]]`center`

## Twos Complement

Negatives in binary is impossible unless you have a signed binary value. Signed binary value means that the maximum a positive value could be is 127 as instead of 255 you minus 128 for the end bit. This end bit will be used as to indicate if it is positive or negative.

> [!NOTE] Example
> For example:
> <u>**1**</u>0000000 = - 128
> <u>**0**</u>1111111 = 127

To get different negative values in binary you can either use twos complement and flip the bits + 1, or you can treat the rest of the values in the string as positive and add numbers to -128 until you get the value you want.

## Subtraction in Binary

Binary subtraction should be treated the same as binary addition but with the negative value. If there is overflow then chop off the 9th bit as it is a positive integer, however if there is no overflow it is a negative number.

# Binary Fractions

![[Pasted image 20220510235144.png]]`center`
This occurs because fractional values are negative powers of 2.
| Place Value        | 2^2 | 2^1 | 2^0 | 2^-1 | 2^-2 | 2^-3 |
| ------------------ | --- | --- | --- | ---- | ---- | ---- |
| Decimal Equivalent | 4   | 2   | 1   | 0.5  | 0.25 | 0.125     |

## Fixed Point and Floating Point

Fixed point binary numbers like : 0001.0101 Have a pre-determined number of bits before and after the point. This makes fixed point numbers easier to process but they cannot represent the range or accuracy of numbers that may be required and you may result in rounding errors.

Floating point numbers however are made out of 3 sections.
![[Pasted image 20220510235834.png]]`center`

The sign bit is the same for subtraction indicating if the end number is positive or negative and then the Mantissa is what gets multiplied by $10^3$, 3 here used as that’s what the exponent is.

> [!Caution] Negatives also occur for the Exponent
> If the exponent for example is 1011 then it would be -3.

## Normalisation

Normalisation is the process of moving the binary point of a floating point number to provide the maximum level of precision for a given number of bits. This is achieved by ensuring that the first digit after the binary point is a significant digit.

> [!Example] In normalised floating point form
> A positive number has a sign bit of 0 and the next digit is always 1.

## Rounding and Relative Errors.

As you cannot have perfect decimals (1/3) then you will always occur with errors. To measure the errors impact on our calculation we can calculate the relative error.  If the actual error is $x$ and the correct value of measurement is $m$  then we can do $(x/m) *100$ which gives us the relative error.