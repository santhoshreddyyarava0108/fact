# fact
ORG 100h

MOV AH, 01h
INT 21h
SUB AL, '0'
MOV CL, AL
MOV AL, 1

FactorialLoop:
    MUL CL
    DEC CL
    JNZ FactorialLoop

ADD AL, '0'
MOV DL, AL
MOV AH, 02h
INT 21h

MOV AH, 4Ch
INT 21h
