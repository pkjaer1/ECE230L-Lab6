# Number Theory: Addition

In this lab you've learned the basics of number theory as it relates to addition.

## Rubric

| Item | Description | Value |
| ---- | ----------- | ----- |
| Summary Answers | Your writings about what you learned in this lab. | 25% |
| Question 1 | Your answers to the question | 25% |
| Question 2 | Your answers to the question | 25% |
| Question 3 | Your answers to the question | 25% |

## Lab Summary
In this lab, we created a representation of a light switch, a single bit adder, and a two-bit full adder in Vivado. The top file creates instances of the light switch and one bit adder, and links 2 full adders together to create a 2-bit adder. The light switch uses an XOR gate, so the light turns on when exactly one of the two switches is flipped.

## Lab Questions

### 1 - How might you add more than two bits together?
You can add more than two bits together by using a full adder. By doing this you can connect multiple full adders together to add bigger binary numbers. The carry out of each full adder goes into the carry in of the next one, starting with the least significant bit. This is called a ripple-carry adder, and it’s how the 2-bit adder in this lab is built.

### 2 - What is the importance of the XOR gate in an adder?
The XOR gate is important because it gives you the sum of the two bits being added. In a basic adder, the XOR gate is used for the sum, while the AND gate is used to find the carry. XOR is 1 only when the two bits are different, which matches binary addition (0+0=0, 0+1=1, and 1+1=0 with a carry). The full adder uses XOR twice to include the carry in.

### 3 - What is the largest number a two bit adder can handle? What happens when you go over?
The largest number a two bit adder can handle is six. This is the largest sum: each input can be at most 3 (binary 11), and 3 + 3 = 6 (binary 110). That needs three output bits, which is why the second full adder has a carry out. When the sum goes over what two bits can hold, the carry out catches the extra bit, so nothing is lost. If you ignored the carry out and only looked at the two sum bits, the result would wrap around and be wrong. For example, 3 + 1 = 4 (100) would show up as 00. This is called overflow.
