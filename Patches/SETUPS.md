### Premium icon lock

Show gray lock for premium only icons.

```
004AA730 | 50           | PUSH EAX
004AA731 | 56           | PUSH ESI
004AA732 | 8B4D 08      | MOV ECX, DWORD PTR SS:[EBP + 8]
004AA735 | 84C9         | TEST CL, CL
004AA737 | 8D41 03      | LEA EAX, DWORD PTR DS:[ECX + 3]
004AA73A | B9 01000000  | MOV ECX, 1
004AA73F | 0F44C1       | CMOVE EAX, ECX
004AA742 | 894424 10    | MOV DWORD PTR SS:[ESP + 10], EAX
004AA746 | E8 05A30100  | CALL meltdown.4C4A50
004AA74B | 8BC8         | MOV ECX, EAX
004AA74D | E8 6EA80100  | CALL meltdown.4C4FC0
004AA752 | 3C 00        | CMP AL, 0
004AA754 | 74 03        | JE meltdown.4AA759
004AA756 | C2 0800      | RET 8
004AA759 | 83C4 04      | ADD ESP, 4
004AA75C | E8 EF760400  | CALL meltdown.4F1E50
004AA761 | 8BC8         | MOV ECX, EAX
004AA763 | E8 18160500  | CALL meltdown.4FBD80
004AA768 | 3C 01        | CMP AL, 1
004AA76A | 74 0C        | JE meltdown.4AA778
004AA76C | 6A 13        | PUSH 13
004AA76E | 68 C4226900  | PUSH meltdown.6922C4
004AA773 | E9 B40B0800  | JMP meltdown.52B32C
004AA778 | 6A 0F        | PUSH F
004AA77A | 68 50326900  | PUSH meltdown.693250
004AA77F | E9 A80B0800  | JMP meltdown.52B32C
....
0052B318 | E8 13F4F7FF  | CALL meltdown.4AA730
```