<div align="center">

## Swap 2 ints without using a 3rd variable


</div>

### Description

Swap two integers without using a 3rd variable!
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Junaidulla](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/junaidulla.md)
**Level**          |Intermediate
**User Rating**    |4.5 (27 globes from 6 users)
**Compatibility**  |Java \(JDK 1\.1\), Java \(JDK 1\.2\)
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__2-57.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/junaidulla-swap-2-ints-without-using-a-3rd-variable__2-3800/archive/master.zip)





### Source Code


<b>Swap Two ints Without Using a Third Variable</b><br>
Here's an old trick from C, which carries over to <br>Java. If you have two ints a and b whose <br>values you want to swap, the obvious way to <br>do so is with a third, temporary variable: <br>
int c = a;<br>
a = b;<br>
b = c;<br>
It can be done without a temporary variable, <br>however, using Java's bitwise xor operator ^: <br>
a = a^b;<br>
b = a^b;<br>
a = a^b;<br>
The operator ^ produces a new int, each of whose <br>bits is the result of xor-ing the two <br>corresponding bits from the operands (1 if <br>the bits are different, 0 otherwise). To see why the trick works, consider the single-bit case <br>of a=1 and b=0. <br>
a = a^b = 1 xor 0 = 1<br>
b = a^b = 1 xor 0 = 1<br>
a = a^b = 1 xor 1 = 0<br>
Even though you initially overwrite the value of <br>a, no information is lost; its encoding <br>simply changes. In the case of larger (multi-bit)<br> numbers, each pair of bits will be swapped <br>in the same way, and so the entire int values are swapped. <br>
Finally, the swapping code can be made even more <br>succinct:
<br>
a ^= b ^= a ^= b;<br>

