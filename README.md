java cAssignment 1
COMP30026 Models of Computation
School of Computing and Information Systems
Due: Friday 30 August at 8:00pm
Aims
To improve your understanding of propositional logic and first-order predicate
logic, including their use in mechanised reasoning; to develop your skills in
analysis and formal reasoning about complex concepts, and to practise writing
down formal arguments with clarity.
Marking
Each question is worth 2 marks, for a total of 12. We aim to ensure that
anyone with a basic comprehension of the subject matter receives a passing
mark. Getting full marks is intended to be considerably more difficu< the
harder questions provide an opportunity for students to distinguish themselves.
Your answers will be marked on correctness and clarity. Do not leave us
guessing! It is better to be clear and wrong; vague answers will attract few
if any marks. This also means you must show your working in mechanical
questions!
Finally, make sure your writing is legible! We cannot mark what we cannot
read. (Keep in mind that the exam will be on paper, so this will be even more
important later!)
Academic Integrity
In this assignment, individual work is called for. By submitting work for
assessment you declare that:
1. You understand the University  s policy on academic integrity.
2. The work submitted is your original work.
3. You have not been unduly assisted by any other person or third party.
4. You have not unduly assisted anyone else.
5. You have not used any unauthorized materials, including but not limited
to AI and translation software.
1
However, if you get stuck, you can use the discussion board to ask any ques-
tions you have. If your question reveals anything about your approach or work-
ing, please make sure that it is set to   private  .
You may only discuss the assignment in basic terms with your peers (e.g.
clarifying what the question is asking, or recommending useful exercises). You
may not directly help others in solving these problems, even by suggesting
strategies.
Soliciting or accepting further help from non-staff is cheating and will lead
to disciplinary action.
Q1 Propositional Logic: Island Puzzle
You come across three inhabitants of the Island of Knights and Knaves. Now, a
mimic has eaten one of them and stolen their appearance, as well as their status
as a knight or knave. (And is thus bound by the same rules. Remember that
knights always tell the truth, and knaves always lie!)
Each makes a statement:
1. A says:   C is either the mimic or a knight, or both.  
2. B says:   It is not the case that both A is the mimic and C is a knave.  
3. C says:   If B is a knight, then the mimic is a knave.  
Task A
Translate the information above into propositional formulas. Give an appropri-
ate interpretation of all propositional letters used. Use the same interpretation
throughout the question; do not give multiple interpretations.
Task B
Determine which of , , and is the mimic, and prove that it must be the
case using an informal argument.
Some advice: A good answer should not be much longer than about 250
words. But do not worry about the length of your first draft! Instead focus on
finding a proof in the first place. Once you have that, it is much easier to find a
shorter proof. Also, remember that clarity is key: write in complete sentences
with good grammar, but do not include irrelevant information or repeat yourself
unnecessarily.
Q2 Propositional Logic:
Validity and Satisfiability
For each of the following propositional formulas, determine whether it is valid,
unsatisfiable, or contingent. If it is valid or unsatisfiable, prove it by drawing
an appropriate resolution refutation. If it is contingent, demonstrate this with
two appropriate truth assignments.
1. ?    (    ?)
2
2. (    (    (    )))    (?    ?(?    ?))
3. ?((    )    )    ( ? )    (    ?)
4. ( ? )    ((    ) ? ( ? ))
Hint: If you are unsure, you can use a truth table to help you decide!
Q3 Predicate Logic: Translation and Seman-
tics
Task A
Translate the following English sentences into formulas of predicate logic. Give
an appropriate interpretation of any non-logical symbols used. Use the same
interpretation throughout this question; do not give multiple interpretations.
1. Iron is heavier than oxygen.
2. All actinides are radioactive.
3. Some, but not all, lanthanides are radioactive.
4. Actinides are heavier than lanthanides.
5. Both lanthanides and actinides are heavier than iron and oxygen.
6. At least three isotopes of lanthanides are radioactive, but the only lan-
thanide without any non-radioactive isotopes is promethium.
Task B
By arguing from the semantics of predicate logic, prove that the universe of
every model of following formula has at least 3 distinct elements. (Resolution
refutations will receive 0 marks.)
??((, )    ?(, ))    ??((, ))
Q4 Predicate Logic: Red-Black Trees
The use of function symbols in our notation for predicate logic allows us to
create a simple representation of binary trees. Namely, let the constant symbol
represent the root node of the tree, and the unary functions and represent
the left and right children of a node. The idea is that () is the left child of the
root node, (()) is the right child of the left child of the root node, and so on.
With this representation defined, we can now prove statements about trees.
A red-black tree is a special type of binary tree that can be searched faster,
in which each node is assigned a colour, either red or black. Let the predicates
and denote whether a node is red or black respectively. A red-black tree is
faster to search because it must satisfy some constraints, two of which are:
3
1. Every node is red or black, but not both:
?((()    ?())    (()    ?())) (1)
2. A red node does not have a red child:
?(()    (?(())    ?(()))) (2)
代 写COMP30026、C++
代做程序编程语言Task
Use resolution to prove that these two conditions entail that a tree consisting
of a non-black root with a red left child is not a red-black tree.
Q5 Informal Proof: Palindromes
Assume the following definitions:
1. A string is a finite sequence of symbols.
2. Given a symbol , we write the string consisting of just also as .
3. Given strings and , we write their concatenation as .
4. Given a collection of symbols 1,   , , we have the following:
(a) The expression 1   stands for the string of symbols whose th
symbol is equal to for all integers from 1 to .
(b) The reverse of the empty string is the empty string.
(c) The reverse of a nonempty string 1   of length is the string
1   where = ?+1 for all positive integers    .
(d) The expression   1 stands for the reverse of 1  .
5. A string is a palindrome if and only if it is equal to its reverse.
Task
The proof attempt below has problems. In particular, it does not carefully
argue from these definitions. Identify and describe the problems with the proof.
Then, give a corrected proof.
Theorem. Let be a palindrome. Then is also a palindrome.
Proof (attempt). We have = 1   for some symbols 1,   , where is
the length of . Since is a palindrome, it is by definition equal to itself under
reversal, so =   1 and = ?+1 for all positive integers    .
Therefore = 1    1, and hence there exist symbols 1,   , 2
such that = 1  2. Since the reverse of 1    1 is itself, it follows
that is a palindrome, as desired.
4
d f g h ie
b
a
c
Figure 1: Diagram of our 9-segment display. Colour key: horizontal segments
are blue, vertical segments are green, and diagonal segments are orange.
Q6 Propositional Logic: Logic on Display
One common practical application of propositional logic is in representing logic
circuits. Consider a 9-segment LED display with the segments labelled a through
i, like the one shown on Figure 1. To display the letter   E  , for example, you
would turn on LEDs , , , and , and turn the rest off.
Arrays of similar displays are commonly used to show numbers on digital
clocks, dishwashers, and other devices. Each LED segment can be turned on or
off, but in most applications, only a small number of on/off combinations are of
interest (e.g. displaying a digit in the range 0 C9 only uses 10 combinations). In
that case, the display can be controlled through a small number of input wires.
For this question, we are interested in creating a display for eight symbols
from the proto-science of alchemy. Since we only want eight different symbols
(see Figure 2), we only need three input wires: , , and .
Figure 2: Table of symbols, their encodings in terms of , and , and the
corresponding on/off state of the segments  C.
So, for example, is represented by = = = 0, and so when all three
wires are unpowered, we should turn on segments , and ? and turn off the
other segments. Similarly, is represented by = = 0 and = 1, so when
wires and are off and the wire is on, we should turn on , and , and
turn off the other segments.
5
Note that each of the display segments  C can be considered a propositional
function of the variables , , and . For example, segment e is on when the
input is one of 101, 110, or 111, and is off otherwise. That is, we can capture
its behavior as the following propositional formula:
(    ?    )    (       ?)    (       ).
The logic display must be implemented with logic circuitry. Here we assume
that only three types of logic gates are available:
1. An and-gate takes two inputs and produces, as output, the conjunction
(  ) of the inputs.
2. An or-gate implements disjunction (  ).
3. An inverter takes a single input and negates (?) it.
Task
Design a logic circuit for each of  C using as few gates as possible. Your answer
does not need to be optimal1 to receive full marks, but it must improve upon
the trivial answer. (Incorrect answers will receive 0 marks.)
We can specify the circuit by writing down the Boolean equations for each
of the outputs  C. For example, from what we just saw, we can define
= (    ?    )    (       ?)    (       )
and thus implement using 10 gates. But the formula (    ?  )    (   )
is equivalent, so we can in fact implement using 5 gates.
Moreover, the nine functions might be able to share some circuitry. For
example, if we have a sub-circuit defined by = ?    , then we can define
=    (    ?    ?), and also possibly reuse in other definitions. That is,
we can share sub-circuits among multiple functions. This can allow us to reduce
the total number of gates. You can define as many   helper   sub-circuits as you
please, to create the smallest possible solution.
Submission
Go to   Assignment 1 (Q6)   on Gradescope, and submit a text file named q6.txt
consisting of one line per definition. This file will be tested automatically, so it
is important that you follow the syntax exactly.
We write ? as - and    as +. We write    as ., or, simpler, we just leave it
out, so that concatenation of expressions denotes their conjunction. Here is an
example set of equations (for a different problem):
# An example of a set of equations in the correct format:
a = -Q R + Q -R + P -Q -R
b = u + P (Q + R)
c = P + -(Q R)
d = u + P a
u = -P -Q
# u is an auxiliary function introduced to simplify b and d
1Indeed, computing an optimal solution to this problem is extremely difficult!
6
Empty lines, and lines that start with   #  , are ignored. Input variables are
in upper case. Negation binds tighter than conjunction, which in turn binds
tighter than disjunction.  Note the use of a helper function , allowing and
to share some circuitry. Also note that we do not allow any feedback loops
in the circuit. In the example above, depends on , so is not allowed to
depend, directly or indirectly, on (and indeed it does not).

         
加QQ：99515681  WX：codinghelp
