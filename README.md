# Turing-Machine-Simulator
Simulating the execution of Turing Machine

#### Turing Machine

In this programming assignment, you will develop a Python program to simulate the execution of Turing Machines ([Wikipedia](https://en.wikipedia.org/wiki/Turing_machine)).

A Turing Machine consists of an infinite "tape" or "memory" made up of individual cells lined up next to each other and extending in both directions. Each cell is capable of "storing/recording" one symbol (we shall use a single letter such as 'a', 'b', ...) and if a cell is not occupied, we can visualize a "#" in that cell (referred to as a blank cell!).

A Turing Machine has a "Read/Write" head that points to a particular cell and is capable of reading the symbol in the cell, possibly replacing it with another symbol, and move the Read/Write head one position to left or right.

A Turing Machine operates using the "instructions" in the Turing Machine specification. Each instruction in the specification will have the following 5 components:

1.  From state
2.  Read Symbol
3.  Write Symbol
4.  Move Direction (L or R)
5.  To state

The From and To states are usually labeled by numbers such as 1, 2, 3, etc. There are two special states: Start state = 1 and Halt state = h.

The operation of a Turing Machine begins with an initial tape content specified by the user and the Read/Write head positioned at the first symbol of the tape and starting in the start state.

After that, the Turing Machine continues to operate according to the instructions/program in the specifications. The instruction is chosen based on the "current" state and the symbol under the Read/Write head.

---
<pre>
Sample runs of the program are shown below:

mirage:p4-tm sb$ python3 TM.py equal.tm abaabb
Initial Tape:
abaabb 1
^
Final Tape:
#xxxxxx# h
 ^
ACCEPT
</pre>
---
<pre>
mirage:p4-tm sb$ python3 TM.py equal.tm abaab
Initial Tape:
abaab 1
^
Final Tape:
#xxxxx# 3
      ^
REJECT
</pre>
---
<pre>
mirage:p4-tm sb$ python3 TM.py -d equal.tm abaabb
Initial Tape:
abaabb 1
^

#xbaabb 2
^

#xbaabb 3
 ^

#xbaabb 3
  ^

#xxaabb 4
 ^

#xxaabb 4
^

#xxaabb 1
 ^

#xxaabb 1
  ^

#xxaabb 1
   ^

#xxxabb 2
  ^

#xxxabb 2
 ^

#xxxabb 2
^

#xxxabb 3
 ^

#xxxabb 3
  ^

#xxxabb 3
   ^

#xxxabb 3
    ^

#xxxabb 3
     ^

#xxxaxb 4
    ^

#xxxaxb 4
   ^

#xxxaxb 4
  ^

#xxxaxb 4
 ^

#xxxaxb 4
^

#xxxaxb 1
 ^

#xxxaxb 1
  ^

#xxxaxb 1
   ^

#xxxaxb 1
    ^

#xxxxxb 2
   ^

#xxxxxb 2
  ^

#xxxxxb 2
 ^

#xxxxxb 2
^

#xxxxxb 3
 ^

#xxxxxb 3
  ^

#xxxxxb 3
   ^

#xxxxxb 3
    ^

#xxxxxb 3
     ^

#xxxxxb 3
      ^

#xxxxxx 4
     ^

#xxxxxx 4
    ^

#xxxxxx 4
   ^

#xxxxxx 4
  ^

#xxxxxx 4
 ^

#xxxxxx 4
^

#xxxxxx 1
 ^

#xxxxxx 1
  ^

#xxxxxx 1
   ^

#xxxxxx 1
    ^

#xxxxxx 1
     ^

#xxxxxx 1
      ^

#xxxxxx# 1
       ^

#xxxxxx# 5
      ^

#xxxxxx# 5
     ^

#xxxxxx# 5
    ^

#xxxxxx# 5
   ^

#xxxxxx# 5
  ^

#xxxxxx# 5
 ^

#xxxxxx# 5
^

#xxxxxx# h
 ^

Final Tape:
#xxxxxx# h
 ^
ACCEPT
mirage:p4-tm sb$
</pre>
