; You may customize this and other start-up templates;
; The location of this template is c:\emu8086\inc\0_com_template.txt

org 100h

; multi-segment executable file template.
ORG 100H



.data segment
  
C DB 0H
SBOXINDEX DW 0

SBOX DB         063H,   07cH,   077H,   07bH,   0f2H,   06bH,   06fH,   0c5H,   030H,   001H,   067H,   02bH,   0feH,   0d7H,   0abH,   076H
     DB         0caH,   082H,   0c9H,   07dH,   0faH,   059H,   047H,   0f0H,   0adH,   0d4H,   0a2H,   0afH,   09cH,   0a4H,   072H,   0c0H
     DB         0b7H,   0fdH,   093H,   026H,   036H,   03fH,   0f7H,   0ccH,   034H,   0a5H,   0e5H,   0f1H,   071H,   0d8H,   031H,   015H
     DB         004H,   0c7H,   023H,   0c3H,   018H,   096H,   005H,   09aH,   007H,   012H,   080H,   0e2H,   0ebH,   027H,   0b2H,   075H
     DB         009H,   083H,   02cH,   01aH,   01bH,   06eH,   05aH,   0a0H,   052H,   03bH,   0d6H,   0b3H,   029H,   0e3H,   02fH,   084H
     DB         053H,   0d1H,   000H,   0edH,   020H,   0fcH,   0b1H,   05bH,   06aH,   0cbH,   0beH,   039H,   04aH,   04cH,   058H,   0cfH
     DB         0d0H,   0efH,   0aaH,   0fbH,   043H,   04dH,   033H,   085H,   045H,   0f9H,   02H,    07fH,   050H,   03cH,   09fH,   0a8H
     DB         051H,   0a3H,   040H,   8fH,    92H,    9dH,    38H,    0f5H,   0bcH,   0b6H,   0daH,   21H,    10H,    0ffH,   0f3H,   0d2H
     DB         0cdH,   0cH,    013H,   0ecH,   5fH,    97H,    44H,    17H,    0c4H,   0a7H,   7eH,    3dH,    64H,    5dH,    19H,    73H
     DB         060H,   081H,   4fH,    0dcH,   22H,    2aH,    90H,    88H,    46H,    0eeH,   0b8H,   14H,    0deH,   5eH,    0bH,    0dbH
     DB         0e0H,   032H,   3aH,    0aH,    49H,    06H,    24H,    5cH,    0c2H,   0d3H,   0acH,   62H,    91H,    95H,    0e4H,   79H
     DB         0e7H,   0c8H,   37H,    6dH,    8dH,    0d5H,   4eH,    0a9H,   6cH,    56H,    0f4H,   0eaH,   65H,    7aH,    0aeH,   08H
     DB         0baH,   078H,   25H,    2eH,    1cH,    0a6H,   0b4H,   0c6H,   0e8H,   0ddH,   74H,    1fH,    4bH,    0bdH,   8bH,    8aH
     DB         070H,   03eH,   0b5H,   66H,    48H,    03H,    0f6H,   0eH,    61H,    35H,    57H,    0b9H,   86H,    0c1H,   1dH,    9eH
     DB         0e1H,   0f8H,   98H,    11H,    69H,    0d9H,   8eH,    94H,    9bH,    1eH,    87H,    0e9H,   0ceH,   55H,    28H,    0dfH       
     DB         08cH,   0a1H,   89H,    0dH,    0bfH,   0e6H,   42H,    68H,    41H,    99H,    2dH,    0fH,    0b0H,   54H,    0bbH,   16H

ONETWOTHREE DB      02H,    03H,    01H,    01H
            DB      01H,    02H,    03H,    01H
            DB      01H,    01H,    02H,    03H   
            DB      03H,    01H,    01H,    02H

RCON    DB      01H,    00H,    00H,    00H
        DB      02H,    00H,    00H,    00H
        DB      04H,    00H,    00H,    00H
        DB      08H,    00H,    00H,    00H
        DB      10H,    00H,    00H,    00H
        DB      20H,    00H,    00H,    00H
        DB      40H,    00H,    00H,    00H
        DB      80H,    00H,    00H,    00H
        DB      1BH,    00H,    00H,    00H
        DB      36H,    00H,    00H,    00H


ORGDATA DB      00H,    00H,    00H,    00H
        DB      00H,    00H,    00H,    00H
        DB      00H,    00H,    00H,    00H
        DB      00H,    00H,    00H,    00H   

DATAPOSTMIXCOL  DB      32H,    88H,    31H,    0E0H
                DB      43H,    5AH,    31H,    37H
                DB      0F6H,   30H,    98H,    07H
                DB      0A8H,   8DH,    0A2H,   34H           
            

CKEY     DB      2BH,    28H,    0ABH,   09H
         DB      7EH,    0AEH,   0F7H,   0CFH
         DB      15H,    0D2H,   15H,    4FH
         DB      16H,    0A6H,   88H,    3CH

RKEY1   DB      0A0H,    88H,    23H,    2AH
        DB      0FAH,    54H,    0A3H,    6CH
        DB      0FEH,    2CH,    39H,    76H
        DB      17H,    0B1H,    39H,    05H

RKEY2   DB      0F2H,    7AH,    59H,    73H
        DB      0C2H,    96H,    35H,    59H
        DB      95H,    0B9H,    80H,    0F6H
        DB      0F2H,    43H,    7AH,    7FH

RKEY3   DB      3DH,    47H,    1EH,    6DH
        DB      80H,    16H,    23H,    7AH
        DB      47H,    0FEH,    7EH,    88H
        DB      7DH,    3EH,    44H,    3BH
       
RKEY4   DB      0EFH,    0A8H,    0B6H,    0DBH
        DB      44H,    52H,    71H,    0BH
        DB      0A5H,    5BH,    25H,    0ADH
        DB      41H,    7FH,    3BH,    00H       


RKEY5   DB      0D4H,    7CH,    0CAH,    11H
        DB      0D1H,    83H,    0F2H,    0F9H
        DB      0C6H,    9DH,    0B8H,    15H
        DB      0F8H,    87H,    0BCH,    0BCH
       
RKEY6   DB      06DH,    11H,    0DBH,    0CAH
        DB      88H,    0BH,    0F9H,    00H
        DB      0A3H,    3EH,    86H,    93H
        DB      7AH,    0FDH,    41H,    0FDH
       
RKEY7   DB      4EH,    5FH,    84H,    4EH
        DB      54H,    5FH,    0A6H,    0A6H
        DB      0F7H,    0C9H,  04FH,    0DCH
        DB      0EH,    0F3H,    0B2H,    4FH
       
RKEY8   DB      0EAH,    0B5H,    31H,    7FH
        DB      0D2H,    8DH,    2BH,    8DH
        DB      73H,    0BAH,    0F5H,    29H
        DB      21H,    0D2H,    60H,    2FH
       
RKEY9   DB      0ACH,    19H,    28H,    57H
        DB      77H,    0FAH,    0D1H,    5CH
        DB      66H,    0DCH,    29H,    00H
        DB      0F3H,    21H,    41H,    6EH
       
       
RKEYA   DB      0D0H,    0C9H,    0E1H,    0B6H
        DB      14H,    0EEH,    3FH,    63H
        DB      0F9H,    25H,    0CH,    0CH
        DB      0A8H,    89H,    0C8H,    0A6H    
        
        
COUNTER DB 1           
 
ends

.stack segment
  
ends


.code segment 
   
;INPUT
MOV SI, 0
MOV DI, 0
LOOPINPUT:
CMP SI, 16
JZ TESTINPUT
MOV AH, 1H
INT 21H 
CMP AL, 39H
JBE NUMBER
LETTER:
SUB AL, 41H
ADD AL, 0AH
JMP CONTINUE
NUMBER:
SUB AL, 30H
JMP CONTINUE
CONTINUE:
SHL AL, 4
MOV DL, AL
MOV AH, 1H
INT 21H
CMP AL, 39H
JBE NUMBER2
LETTER2:
SUB AL, 41H
ADD AL, 0AH
JMP CONTINUE2
NUMBER2:
SUB AL, 30H
JMP CONTINUE2
CONTINUE2:
ADD DL, AL
;SUB DL, 30H
MOV ORGDATA[SI], DL
INC SI
JMP LOOPINPUT

TESTINPUT:
CMP DI, 16
JZ START
MOV AL, ORGDATA[DI]
INC DI
JMP TESTINPUT    
  
    
    
START:
MOV SI,0
MOV DI,0
LOOPCIPHER:

CMP DI,16
JZ ENDCIPHER
MOV AL,ORGDATA[DI]
MOV CL, CKEY [DI]
XOR AL,CL
MOV ORGDATA[DI],AL
INC DI
JMP LOOPCIPHER


ENDCIPHER:
;Test first roundkey (Starting with 19 a0 9a e9)
;CMP SI,16
;JZ BYECIPHER
;MOV AL,ORGDATA[SI]
;INC SI
;LOOP ENDCIPHER
;BYECIPHER:
;----------------------------
 
 
BIGLOOP:

CMP COUNTER,11
JZ EXITBIGLOOP 
 

;Subbytes---------------------------------------------- 
MOV SBOXINDEX,0
MOV SI, 0
MOV DI, 0
LOOPSUBBYTES:
CMP SI, 16
JZ ENDSUBBYTES
 
MOV AL, ORGDATA[SI]
AND AL, 0F0H
SHR AL, 4 ;CL has higher byte  1
MOV DL, 10H
MUL DL ;AX HAS 16 DECIMAL
MOV AH, 0
MOV SBOXINDEX, AX

MOV CL, ORGDATA[SI]
AND CL, 0FH ;AL has lower byte 9
MOV CH,0
ADD SBOXINDEX, CX
MOV DI, SBOXINDEX

MOV AL, SBOX[DI]
MOV ORGDATA[SI], AL
 
INC SI
JMP LOOPSUBBYTES

ENDSUBBYTES:

;Shift Rows--------------------------------------------

MOV SI,0

LOOPSHIFTROWS:
CMP SI,0
JZ ZERO
CMP SI,4
JZ ENDSHIFTROWS
CMP SI,3
JZ THIRD
CMP SI,2
JZ SECOND
CMP SI,1
JZ FIRST 

ZERO:

INC SI
JMP LOOPSHIFTROWS

FIRST:

MOV DI,4

MOV AL,ORGDATA[DI + 0]
MOV DL,ORGDATA[DI + 3]
MOV ORGDATA[DI + 0],DL
MOV ORGDATA[DI + 3],AL

MOV AL,ORGDATA[DI + 0]
MOV DL,ORGDATA[DI + 1]
MOV ORGDATA[DI + 0],DL
MOV ORGDATA[DI + 1],AL

MOV AL,ORGDATA[DI + 1]
MOV DL,ORGDATA[DI + 2]
MOV ORGDATA[DI + 1],DL
MOV ORGDATA[DI + 2],AL             

INC SI
JMP LOOPSHIFTROWS

SECOND:

MOV DI,8

MOV AL,ORGDATA[DI + 0]
MOV DL,ORGDATA[DI + 2]
MOV ORGDATA[DI + 0],DL
MOV ORGDATA[DI + 2],AL

MOV AL,ORGDATA[DI + 1]
MOV DL,ORGDATA[DI + 3]
MOV ORGDATA[DI + 1],DL
MOV ORGDATA[DI + 3],AL

INC SI
JMP LOOPSHIFTROWS


THIRD:

MOV DI,12

MOV AL,ORGDATA[DI + 0]
MOV DL,ORGDATA[DI + 3]
MOV ORGDATA[DI + 0],DL
MOV ORGDATA[DI + 3],AL

MOV AL,ORGDATA[DI + 1]
MOV DL,ORGDATA[DI + 3]
MOV ORGDATA[DI + 1],DL
MOV ORGDATA[DI + 3],AL

MOV AL,ORGDATA[DI + 2]
MOV DL,ORGDATA[DI + 3]
MOV ORGDATA[DI + 2],DL
MOV ORGDATA[DI + 3],AL

INC SI
JMP LOOPSHIFTROWS

ENDSHIFTROWS:   

;MIX COLOUMNS--------------------------------------------------------

CMP COUNTER,10
JZ  ENDMIXCOL

MOV DX,0
MOV SI,0
MOV DI,0
MOV SP,1

LOOPMIXCOL:

CMP SP,5
JZ ENDMIXCOL1
MOV BP,0
ADD BP,SP
ADD BP,SP
ADD BP,SP
ADD BP,SP


SUBLOOPMIXCOL:
CMP DI,BP
JZ ENDSUBMIXCOL
MOV CL,ORGDATA[SI]
MOV AL,ONETWOTHREE[DI]
CMP AL,01H
JZ ONE
CMP AL,02H
JZ TWO
CMP AL,03H
JZ THREE

;------------------------------------
ONE:
 
JMP FINAL

TWO:
CMP CL,80H
JB NEXTTWO
SHL CL,1
XOR CL,1BH
JMP FINAL
NEXTTWO:
SHL CL,1 
JMP FINAL

       
THREE:
CMP CL,80H
JB NEXTTHREE
MOV CH,CL
SHL CL,1
XOR CL,1BH
XOR CL,CH
JMP FINAL
NEXTTHREE:
MOV CH,CL
SHL CL,1
XOR CL,CH
JMP FINAL


FINAL:
XOR DL,CL
ADD SI,4
INC DI
CMP DI,BP
JNZ SUBLOOPMIXCOL
JMP NEXTMIX

;------------------------------------
ENDSUBMIXCOL:

JMP FINAL

NEXTMIX:

CMP DH,1
JZ END1
CMP DH,2
JZ END2
CMP DH,3
JZ END3
CMP DH,4
JZ ENDMIXCOL

INC SP
SUB DI,4
MOV DATAPOSTMIXCOL[DI],DL
MOV AL,DATAPOSTMIXCOL[DI]
MOV SI,0
MOV DL,0
ADD DI,4

JMP LOOPMIXCOL

ENDMIXCOL1:

INC DH
MOV SI,1
MOV DL,0
MOV DI,0
MOV SP,1
;-----------------------------------
LOOP1:

CMP SP,5
JZ ENDMIXCOL2
MOV BP,0
ADD BP,SP
ADD BP,SP
ADD BP,SP
ADD BP,SP
JMP SUBLOOPMIXCOL

END1:

INC SP
SUB DI,4
MOV DATAPOSTMIXCOL[1+DI],DL
MOV SI,1
MOV DL,0
ADD DI,4
JMP LOOP1

ENDMIXCOL2:

INC DH
MOV SI,2
MOV DL,0
MOV DI,0
MOV SP,1
;-----------------------------------
LOOP2:

CMP SP,5
JZ ENDMIXCOL3
MOV BP,0
ADD BP,SP
ADD BP,SP
ADD BP,SP
ADD BP,SP
JMP SUBLOOPMIXCOL

END2:

INC SP
SUB DI,4
MOV DATAPOSTMIXCOL[2+DI],DL
MOV SI,2
MOV DL,0
ADD DI,4
JMP LOOP2

ENDMIXCOL3:

INC DH
MOV SI,3
MOV DL,0
MOV DI,0
MOV SP,1
;-----------------------------------
LOOP3:

CMP SP,5
JZ ENDMIXCOL
MOV BP,0
ADD BP,SP
ADD BP,SP
ADD BP,SP
ADD BP,SP
JMP SUBLOOPMIXCOL



END3:

INC SP
SUB DI,4
MOV DATAPOSTMIXCOL[3+DI],DL
MOV SI,3
MOV DL,0
ADD DI,4
JMP LOOP3


ENDMIXCOL:

;ADD ROUND KEY ------------------------   



MOV DI,0
LOOPROUND:
CMP DI,16
JZ EXITLOOPROUND 

CMP COUNTER,10
JZ AFTER1 
MOV AL,DATAPOSTMIXCOL[DI]
JMP AFTER2 
AFTER1:
MOV AL,ORGDATA[DI]  
AFTER2:

CMP COUNTER,1
JZ KEY1   
CMP COUNTER,2
JZ KEY2
CMP COUNTER,3
JZ KEY3
CMP COUNTER,4
JZ KEY4
CMP COUNTER,5
JZ KEY5 
CMP COUNTER,6
JZ KEY6  
CMP COUNTER,7
JZ KEY7
CMP COUNTER,8
JZ KEY8
CMP COUNTER,9
JZ KEY9
CMP COUNTER,10
JZ KEYA


KEY1:
MOV CL, RKEY1[DI]
JMP NEXT
KEY2:
MOV CL, RKEY2[DI]
JMP NEXT
KEY3:
MOV CL, RKEY3[DI]
JMP NEXT
KEY4:
MOV CL, RKEY4[DI]
JMP NEXT
KEY5:
MOV CL, RKEY5[DI] 
JMP NEXT
KEY6:
MOV CL, RKEY6[DI]
JMP NEXT
KEY7:
MOV CL, RKEY7[DI]
JMP NEXT
KEY8:
MOV CL, RKEY8[DI]
JMP NEXT
KEY9:
MOV CL, RKEY9[DI]
JMP NEXT
KEYA:
MOV CL, RKEYA[DI]
JMP NEXT

NEXT:
XOR AL,CL
MOV DATAPOSTMIXCOL[DI],AL
INC DI
JMP LOOPROUND

EXITLOOPROUND:  
;///////////////////////////////////////////////////STOP HERE TO CHECK/////////////////////////////     
;///////////////////////////////////////////////////STOP HERE TO CHECK/////////////////////////////
MOV DI,0
LOOPSHIFT:
CMP DI,16
JZ ENDLOOPSHIFT
MOV DL,DATAPOSTMIXCOL[DI]   
MOV ORGDATA[DI],DL
INC DI
JMP LOOPSHIFT
ENDLOOPSHIFT:

INC COUNTER
JMP BIGLOOP

 



EXITBIGLOOP:
   
MOV DI,0
LOOPTEST0:
CMP DI,16
JZ ENDLOOPTEST0 


MOV DL,ORGDATA[DI]   ; 1 byte
AND DL,0F0H         ; HIGHER HALF BYTE    
SHR DL,4
CMP DL,9
JG ALPHA1
ADD DL,30H
JMP NOTALPHA1
ALPHA1:
ADD DL,37H
NOTALPHA1: 

MOV AH,2H 
INT 21H 


MOV DL,ORGDATA[DI]   ; 1 byte
AND DL,0FH           ; LOWER HALF BYTE  

CMP DL,9
JG ALPHA
ADD DL,30H
JMP NOTALPHA
ALPHA:
ADD DL,37H
NOTALPHA: 

MOV AH,2H 
INT 21H  

;SPACING
MOV DL,20H
MOV AH,2H 
INT 21H


;NEWLINE
CMP DI,3 
JZ NEWLINE
CMP DI,7
JZ NEWLINE
CMP DI,11
JZ NEWLINE
JMP NOTNEWLINE

NEWLINE:
MOV DL,0AH
MOV AH,2H 
INT 21H   

MOV SI,0
LOOPBACK:
CMP SI,12
JZ NOTNEWLINE
MOV DL,08H
MOV AH,2H 
INT 21H
INC SI 
JMP LOOPBACK

NOTNEWLINE:

INC DI                                                          
JMP LOOPTEST0
ENDLOOPTEST0: 

;MOV DI,0
;LOOPTEST:
;CMP DI,16
;JZ ENDLOOPTEST
;MOV DL,ORGDATA[DI]
;MOV AH,2H 
;INT 21H
;INC DI                                                              
;JMP LOOPTEST
;ENDLOOPTEST: 


ret