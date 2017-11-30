# lab_architecture_manipulatingbits

1  Introduction
The purpose of this assignment is to become more familiar with bit-level representations of integers and floating point numbers. You’ll do this by solving a series of programming “puzzles.” Many of these puzzles are quite artificial, but you’ll find yourself thinking much more about bits in working your way through them.

2  Logistics
This is an individual project. All handins are electronic. Clarifications and corrections will be posted on the course moodle.

3  Handout Instructions
Start by downloading the datalab-handout.tar archive. Copy datalab-handout.tar to a (protected) directory on a Linux machine in which you plan to do your work. Then give the command

  $ tar xvf datalab-handout.tar .   
This will cause a number of files to be unpacked in the directory. The only file you will be modifying and turning in is bits.c.

The bits.c file contains a skeleton for each of the 15 programming puzzles. Your assignment is to complete each function skeleton using only straightline code for the integer puzzles (i.e., no loops or conditionals) and a limited number of C arithmetic and logical operators. Specifically, you are only allowed to use the following eight operators:

 ! ~ & ^ | + << >>
A few of the functions further restrict this list. Also, you are not allowed to use any constants longer than 8 bits. See the comments in bits.c for detailed rules and a discussion of the desired coding style.

4  The Puzzles
This section describes the puzzles that you will be solving in bits.c.

4.1  Bit Manipulations
Table 1 describes a set of functions that manipulate and test sets of bits. The “Rating” field gives the difficulty rating (the number of points) for the puzzle, and the “Max ops” field gives the maximum number of operators you are allowed to use to implement each function. See the comments in bits.c for more details on the desired behavior of the functions. You may also refer to the test functions in tests.c. These are used as reference functions to express the correct behavior of your functions, although they don’t satisfy the coding rules for your functions.

Name	Description	Rating	Max Ops
isZero(x)	return 1 if x == 0, and 0 otherwise	1	2
bitNor(x,y)	~(x|y) using only ~ and &	1	8
upperBits(n)	pads n upper bits with 1’s	1	10
copyLSB(x)	set all bits of result to least significant bit of x	2	5
allEvenBits(x)	return 1 if all even-numbered bits in word are set to 1	2	12
logicalShift(x,n)	shift x to the right by n, using a logical shift	3	20
bitParity(x)	returns 1 if x contains an odd number of 0’s	4	20
Table 1: Bit-Level Manipulation Functions.
4.2  Two’s Complement Arithmetic
Table 2 describes a set of functions that make use of the two’s complement representation of integers. Again, refer to the comments in bits.c and the reference versions in tests.c for more information.

Name	Description	Rating	Max Ops
tmin()	Most negative two’s complement integer	1	4
isTmax(x)	returns 1 if x is the maximum, two’s complement number, and 0 otherwise	1	10
negate(x)	return -x	2	5
addOk(x,y)	determine if can compute x+y without overflow	3	20
isPositive(x)	return 1 if x > 0, return 0 otherwise	3	8
satAdd(x,y)	adds two numbers, saturating when overflow occurs	4	30
Table 2: Arithmetic Functions

