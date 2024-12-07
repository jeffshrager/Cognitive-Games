**Mystery Machine Cheat Sheet**  
---

ATTENTION: You must enter a mode by using the 

     mode \[mode number\]  
As:   
     mode 3       \[Or whatever mode number you like\]

before anything will work. Even if you aren't going to use the ? key (which is the only thing the mode affects) you still need to enter a mode to get started. (I recommend mode 3 because it's the simplest ? mode, but if you're not using the ? the mode number doesn't matter.)  
---

Every program in the MM language is one line long.

A "step" is always two characters: a number, followed by any alphabetic character "command". For example: "3x", "5-", "6?" In these cases the "commands" are x, \-, ? respectively.

Digits (0-9) put that number in the MM's "register". No matter how many digits you enter, the register only remembers the last one. So, for example, if your program looks like 12343247+ only the number 7 is going to be registered (that is, used). 

In the below, I'll use \# to indicate a single digit or the number in the register, and \+ or \- to indicate characters (or ? when we're talking about loops, below).

Any character other than a digit or ? just tells the MM to print out the given character the number of times in the register. 

Some example simple programs (without ?s):

Input: 3-  
Output: \---

3-4+  
\---++++

3-4+5x  
\---++++xxxxx

*Again: There is only one register and it only holds one digit. So if you put multiple digits, like 53, or forget to put a digit before a command, it'll just use whatever's left in the register.*

Some example slightly confusing programs (without ?s):

3-4+        
\---++++    \[normal\]

53-4+  
\---++++    \[the 5 is overwritten by the 3, so you only get 3 minuses\]

3-+  
\---+++     \[the 3 is applied to the \+ also because we left out an argument for the \+ so it used the 3 left in the register\]

\+  
              \[no output \-- no argument at all \-- nothing happens\!\]

Note that although all the examples are \+ and \-, any character other than a digit or ? will work just as well. For example:

3-4+        
\---++++    \[normal\]

3x4y        
xxxyyyy    \[also normal\!\]

Sometimes subjects discover this on their own, but if they are getting confused counting the minuses \-- which are intentionally hard to count\! \-- you might suggest using a different character that's easier to distinguish.

The register is cleared at the beginning of each GO (run) so until it hits a number in reading the program, nothing at all will happen. This can be confusing. 

For example:

xyz abc 5 mno pqr  
     mmmmmnnnnnooooo     pppppqqqqqrrrrr

\[This has 5 spaces at the beginning, and then again in the middle, which are impossible to count, which is why in the instructions on the MM page is says not to use spaces\!\]

---

The question mark (?) command means "repeat" (but don't tell your subjects that\! :-)

Different modes make the ? do different things. See the cheat sheet below.

Some common confusions:

* In some modes it's counting *characters* (as in positions in the program line), and in others it's counting *steps*, that is, 2-character pairs, like 4x. This can get very confusing if your subject is a little confused and doesn't adhere to the standard two-character (digit and output char) format. For example, 3+4- is "standard" and a mode that is counting steps will count these correctly, but if they did something like 34+ or 31-45+ the "step counting" modes are moving by 2 character positions, so it'll output something almost uninterpretable. (Again, this is by design\!) 

* If the subject doesn't put a number before the ?, it will (as usual) use the last number in the register (i.e., the last digit encountered, as described above). This can get *very* confusing\! For example, these two programs are equivalent in most modes: 3x2y2? and 3x2y?, the "2" being carried to the "?" because we didn't have a number before the "?". Generally you'll want to be sure that you have a number before the "?", because otherwise the command-counting modes (4 and 6\) will do totally confusing things as they are just going by pairs of input chars. (Actually, it's totally confusing regardless ... which is, afterall, the point\! :-)

Mode details, and some examples:

* Mode 1 restart the programming counting \# *characters* ***back*** from the ?, and runs through ***once*** more (ignoring the ? the second time through). To go back to the beginning, \# would be one less than the length of the program (i.e., program length \- 1). If you overshoot the beginning of the program, it just starts from the beginning. (That is, you can't overshoot the beginning, even with a large number for \#.)

* Mode 2 restarts the program at the indicated *character* position (starting with 1). Note that if you hit a symbol instead of a number, the symbol will appear the number of times given by the number associated with the ? This can be *ultra* confusing\!

* Mode 3 just runs the whole program again once. (This is the simplest mode)

Mode 4 begins again at the nth *step* (*not the nth character\!*). The first step is number 1\. Note that (as above) a "step" is defined as a pair of chars (like "3x"), if you do something technically incorrect, like: "33x" you'll be confused because it's just counting by twos, not really parsing for steps.

You're now saying to yourself: WTF?\!

Okay, examples:

mode 4

3-4+  
\---++++              \[the basic program we're going to use\]

3-4+?1  
\---++++              \[I did 1? instead of ?1 so it tried to go to the 4th step, but there isn't one\]

3-4+1?  
\---++++---++++       \[good, so that restarted from step 1, and we ran both steps again\]

3-4+1?  
\---++++---++++       \[just making sure it's repeatable\!\]

3-4+?2  
\---++++              \[aaaa\!\!\!\!\!\!\!\! Oh, damn\! reversed the \# and ? again\!\]

3-4+2?  
\---++++++++          \[That's better: Started from the second step \-- actually the 3rd char, that is, the 4 \-- and ran to the end\]

53-4+  
\---++++              \[recall that only one digit matters, so the 5 got overwritten by the 3\]

53-4+1?  
\---++++---++++       \[just proving to myself that this still does the right thing\]

53-4+2?  
\---++++--++++       

\[Okay, so THIS is the confusing one\! Because the 5 shifted everything up by one, even though it doesn't play a role in the program, the 2? asked us to start at position 3 \-- that is, at the second step, which in a normal program (without the errant 5\) would have been step 2 (4+, as above), but here it actually lands us at the minus\! So the 2 gets carried from the ? argument and applied to the minus, so you get 2 minuses, and then the 4+ ... see, ULTRA confusing\!\]

* Mode 5 runs the program through again beginning at a random character position\! (NOT a random step\!)

* Mode 6 is mode 4 crossed with mode 1\. It restarts the program at the nth *step* (not character\!) ***before*** the ? command. (Note the ultra-confusing-ness warnings above\!)

You may wonder why the modes aren't in "simplest-to-hardest" order. That's by design so as not to give a hint to the subject about how much simpler or harder the analysis might be.