EECS 349 HW3 Drew Heald

1. Solution: replace all instances of PUSH 402160 with PUSH 402129 in assembly, and all instances of PUSH 402169 with PUSH 402134
2. Sets name to be uppercase

Compares EAX and EBX
EAX set when name is set to uppercase
EAX = add hex value of each ASCII character together, XOR by 5678 (101011001111000)
EBX = sum of each (value in serial * 10), XOR by 1234 (1001000110100)
Must equal each other

aaa -> AAA -> 195 sum (decimal sum of ASCII characters) -> 11000011 binary -> XOR with 5678 (101011001111000) -> 55bb hex
55bb -> XOR by 1234 (1001000110100) -> 448f hex -> convert to decimal

DREW -> 306 -> 132 hex -> XOR 5678h -> 574ah -> XOR 1234h -> 457eh -> 17790
Take name -> Uppercase name -> sum of the ASCII values of the name -> hex value of sum -> XOR with 5678h -> XOR that with 1234h -> convert that hex to decimal and you have your serial number