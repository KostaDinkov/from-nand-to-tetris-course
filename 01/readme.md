
# Unit 1: Boolean Functions and Gate Logic


## Description of the Laws of Boolean Algebra

NOTE: using C# style logical operator notation

* & - AND
* ! - NOT
* | - OR
* ^ - XOR
### Annulment Law – 

`A & 0 = 0`    A variable AND’ed with 0 is always equal to 0

`A | 1 = 1`    A variable OR’ed with 1 is always equal to 1

### Identity Law –

`A | 0 = A`   A variable OR’ed with 0 is always equal to the variable

`A & 1 = A`    A variable AND’ed with 1 is always equal to the variable

### Idempotent Law –

`A | A = A`    A variable OR’ed with itself is always equal to the variable

`A & A = A`    A variable AND’ed with itself is always equal to the variable

### Complement Law – 

`A  & !A = 0`    A variable AND’ed with its complement is always equal to 0

`A | !A = 1`    A variable OR’ed with its complement is always equal to 1

### Commutative Law – 

`A  & B = B & A`    The order in which two variables are AND’ed makes no difference

`A | B = B | A`    The order in which two variables are OR’ed makes no difference

### Double Negation Law – 

`!!A = A`     A double complement of a variable is always equal to the variable

### De Morgan´s Theorem – There are two “de Morgan´s” rules or theorems,

`!(A | B) = !A & !B`

`!(A & B) = !A | !B`

### Distributive Law – 

`A & (B | C) = A & B | A & C`    (OR Distributive Law)

`A | (B & C) = (A | B) & (A | C)`    (AND Distributive Law)

### Absorptive Law -

`A | (A & B) = A`    (OR Absorption Law)

`A & (A | B)  =  A`    (AND Absorption Law)

### Associative Law –

`A | (B | C) = (A | B) | C = A | B | C`    (OR Associate Law)

`A & (B & C) = (A & B) & C = A & B & C`    (AND Associate Law)

## Extract a function from a truth table

**Problem - derive a formula for the XOR function based on the truth table specification**

| A    | B    | XOR  | Formula |
| ---- | ---- | ---- | ------- |
| 0    | 0    | 0    |         |
| 1    | 0    | 1    | A & !B  |
| 0    | 1    | 1    | !A & B  |
| 1    | 1    | 0    |         |

```
XOR(A,B) = (A & !B) | (!A & B)
```

* First we write a formula for each row that we have a 1 in the result of the XOR function
* The formula must be true for the specific row and false for every other row
* We "OR" all individual formulas together
* We can use boolean algebra rules to simplify the expression, if needed.

#### Precedence of Logical Operators

| Operator | Precedence |
| -------- | ---------- |
| ! (NOT)  | High       |
| & (AND)  | Medium     |
| \| (OR)  | Low        |

Using the precedence table we can rewrite the equation as follows:

```
XOR(A,B) = A & !B | !A & B
```

## Logic Gates

>*From Wikipedia:*
>
>*In electronics, a logic gate is an idealized or physical device implementing a Boolean function; that is, it performs a logical operation on one or more binary inputs and produces a single binary output.*

| A    | B    | AND  | NAND | OR   | NOR  | XOR  | XNOR |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 0    | 0    | 0    | 1    | 0    | 1    | 0    | 1    |
| 1    | 0    | 0    | 1    | 1    | 0    | 1    | 0    |
| 0    | 1    | 0    | 1    | 1    | 0    | 1    | 0    |
| 1    | 1    | 1    | 0    | 1    | 0    | 0    | 1    |

### Hardware Description Language (HDL)



> *From [Wikipedia](https://en.wikipedia.org/wiki/Hardware_description_language):*
>
> *In computer engineering, a **hardware description language** (**HDL**) is a specialized computer language used to describe the structure and behavior of electronic circuits, and most commonly, digital logic circuits.*
>
> *A hardware description language enables a precise, formal description of an electronic circuit that allows for the automated analysis and simulation of an electronic circuit. It also allows for the synthesis of a HDL description into a netlist (a specification of physical electronic components and how they are connected together), which can then be placed and routed to produce the set of masks used to create an integrated circuit.*
>
> *A hardware description language looks much like a programming language such as C; it is a textual description consisting of expressions, statements and control structures. One important difference between most programming languages and HDLs is that HDLs explicitly include the notion of time.*



![xor diagram](.\img\xor.jpg) 