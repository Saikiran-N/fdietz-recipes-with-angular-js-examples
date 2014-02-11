# Logarithms and Bits

A single bit is capable of expressing two quantities--0 and 1. In binary, these can represent the numbers 0 and 1. With two bits, we can express the numbers 0, 1, 2, and 3 with the binary expressions `00`, `01`, `10`, and `11` respectively. Notice that each bit is capable of containing one value--on or off (1 or 0), and that in the case where we use two bits to express a value, the first bit represents the presence of a 2, and the second bit represents the presence of a 1. Added together, these bits are capable of expressing the numbers 0-3. Binary expresses values in base 2, where decimal expresses values in base 10. In decimal, we think of the number 1,000 as expressing 1 one thousand, 0 hundreds, 0 tens, and 0 ones. Base two works the same way, except with powers of two instead of powers of 10. `1110`, in binary, expresses the value 14, where the first position represents `2**3`, the second position `2**2`, the third position `2**1`, and the fourth position `2**0` (1). If we add the values with a `1` in that position, we get the number 14. 

How many bits `w` do we need to represent any one of `n` different possibilities, be it one of `n` items or the integers from 1 to `n`? The key observation is that we need at least `n` different bit patterns. Since the number of bit patterns doubles as you add each bit, we need at least w = log<sub>2</sub>n bits. For instance, if we want to express the numbers 1-4, we need w = log<sub>2</sub>4 (2 bits). 2 bits provides us with exactly four distinct bit patterns, allowing us to represent each of the four values. Those familiar with binary will likely notice, however, that we actually need _3_ bits to represent the number 4, since the 0th bit represents 2<sup>0</sup>, the 1st bit represents 2<sup>1</sup>, and we can't make 4 out of 2 + 1. That's true; the point we're trying to make here is that we are given 4 bit patterns with 2 bits, and that we _could_, under some other system, represent the number 4 this way. Supposing we wanted to actually represent the number 4 on the binary system we actually use, we'd need the ability to represent at least _5_ possibilities, since 0 is our first possibility. Adding one more bit gets us 2<sup>3</sup>=8 values, allowing us to represent the numbers 0-7.