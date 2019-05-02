# LC3-Von-Neumann-Model

## Author: Tomas S
## Date: 4/19/2019
## Project: LC3 Final README

The purpose of the circuit is to mimic the Von Neumann Model using logisim. More specifically the instructions which are implemented are ADD, ADD(Immediate), AND, AND(Immediate), NOT, JMP, LD, LDR, ST, STR. Some instructions were left out for time's sake. In all the major components of the circuit are the Control Unit, ALU, Registers, Memory, and Main. 

A summary of the circuit is the control unit takes in an instruction from the memory. From there the instruction cycle starts and the instruction is interpreted using a 4-16bit decoder. Then depending on the instruction specific control signals might be sent to various parts of the lc3 computer using tunnels. From here a value might be retrieved from a register or assignment to a register. Or possible to or from the memory. In all the circuit houses small processes that work together to complete the instruction cycle as instructed by the instruction.

## Notes:
- In the beginning, I struggled with a register issue where all the registers were being written to and reset during a cycle. This was an issue caused by the DR not being set prior to the operation.
- All instructions have been tested and noted as working.
- File names ending with _2 due to a halfway reset in the engineer's making of the circuit. 

## INSTRUCTION TESTS:

ADD - Tested, Works using 200f (LD), 220e (LD), 1001 (ADD), 3005 (ST)
ADD IMMU5 - Tested, Works using 200f (LD), 103f (ADD), 3005 (ST)
AND - Tested, Works using 200f (LD), 220e (LD), 5001 (AND), 3005 (ST)
AND IMMU5 - Tested, Works using 200f (LD), 503b (AND), 3005 (ST)
NOT - Tested, Works using 200f (LD), 903f (NOT), 3005 (ST)
JMP - Tested, Works using 200f (LD), c000 (JMP)
LD - Tested, Works using 200f (LD), 3003 (ST)
LDR - Tested, Works using 220e (LD), 6067 (LDR), 3004 (ST)
ST - Tested, Works using 200f (LD), 3003 (ST)
STR - Tested, Works using 200f (LD), 220e (LD), 706f (STR)    
