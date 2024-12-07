*IMPORTANT NOTE: THIS IS (NEARLY) AN ENTIRE MYSTERY MACHINE TRANSCRIPT. WHAT YOU TURN IN DOES NOT HAVE TO BE THE ENTIRE TRANSCRIPT, ONLY "INTERESTING SEGMENTS". BELOW I HAVE HIGHLIGHTED IN GREEN SOME EXAMPLES OF INTERESTING SEGMENTS. IF THIS WAS YOUR TRANSCRIPT, YOU WOULD ONLY HAVE  TO ACTUALLY TRANSCRIBE AND TURN IN SOME OF THE GREEN ONES.*  
   
\[--- I initially tried to get my subject to get mode 8, but it was not functioning properly. Thus, the subject already knew the syntax of number-character-number-character, etc. She also knew that she was supposed to find what the question mark did.---\]  
   
mode 4  
   
2a3s  
Aasss  
   
"Hmm, same as last time...1 question mark"  
   
2a1?3s  
Aaaasss  
   
"Huuh, it adds another a... no, it doubled the a"  
   
4a1?3s  
Aaaaaaaasss  
   
"Okay, it doubles the 'a' from before"  
   
\[---From the very beginning, she figures out that the question mark will double some sequence of characters within the string, but does not know how/which sets are doubled. \---\]  
   
2a1?3s  
aaaasss  
2a2?3s  
Aasss  
   
"What if I put '2?'... WAH, it gets rid of it\! So if I put '2?' it does nothing¦"  
   
\[--- Up until this point, she has only figured out that it seems to double some set of the characters. This is when she first runs into the number before the question mark being the position of the question mark's pair, and thus doing nothing. After this point, she wants to figure out how the number before the question mark impacts the string which is printed out, but the number of pairs input is still too short for her gather any good evidence other than the fact that the question mark seems to have no impact at a certain point. \---\]  
   
2a3?3s  
aasss  
2a4?3s  
aa  
2a5?3s  
aa  
2a6?3s  
aa  
2a7?3s  
aa  
2a8?3s  
aa  
2a0?3s  
   
"I typed 9, not 0\!"  
   
aasss  
2a9?3s  
Aa  
   
\[--- At this point, she sets the goal of finding out what the question mark does with no values after the question mark and only one pair before it, isolating behavior for numbers when the number before the question mark is lower than the position that it comes in \---\]  
   
"OK, 0, 2, 3 did nothing, 1 doubled the previous character, and anything higher than 3 deleted. So what if I had only one first character?"  
   
2a9?  
aa  
2a0?  
aa  
2a1?  
aaaa  
2a2?  
aa  
2a3?  
Aa  
   
"I have a feeling that the number will delete strings, not just the one right before or right after, but two before or two after"  
   
3x2a0?  
xxxaa  
3x2a1?  
Xxxaaxxxaa  
   
\[---She thinks that the ? will double strings which exist before the ? The next few commands serve to validate this hypothesis. At this point, she still does not understand how the number before the question mark impacts what is printed out by the string. \---\]  
   
"It doubles the whole string before it"  
   
3x2a2?  
Xxxaaaa  
   
"Two doubles the second string. Right? yeah"  
   
3x2a3?  
Xxxaa  
   
"Three doubles nothing. I want to see if the number in front of the question mark tells you how many steps to double"

\[---She thinks the question mark denotes how many pairs to double in front of it, but I'm not sure if she means going forward from the start, or back from the question mark, but she seems to be on the right track.---\]  
   
1a2b3c4d5e0?  
Abbcccddddeeeee  
1a2b3c4d5e1?  
abbcccddddeeeeeabbcccddddeeeee  
1a2b3c4d5e2?  
abbcccddddeeeeebbcccddddeeeee  
1a2b3c4d5e3?  
abbcccddddeeeeecccddddeeeee  
1a2b3c4d5e4?  
abbcccddddeeeeeddddeeeee  
1a2b3c4d5e5?  
abbcccddddeeeeeeeeee  
1a2b3c4d5e6?  
Abbcccddddeeeee  
   
"Okay, this makes sense. So it starts at the nth pair, and keeps doubling the strings until it reaches the question mark position, and if the n before the question mark is greater than the number of sets you have, then it does nothing. Okay, I want to see what happens if it's after. I will delete the strings before. No, just make them all one and keep them there"  
   
   
1a1b1c1d1e0?1f1g1h1i  
abcdefghi  
1a1b1c1d1e1?1f1g1h1i  
Abcdeabcdefghi  
   
"Okay, now I'm deleting the letters before because it's two cluttered"  
   
\[---Now she is trying to see what happens if the question mark is before some pairs of numbers/letters. At this point, she still does not understand what happens if the question mark's number denotes the position of the question mark in the command line.---\]  
   
1?1f1g1h1i  
fghi  
2?1f1g1h1i  
fghi  
3?1f1g1h1i  
Ghi  
   
"Oh, three deleted a letter\! Three deleted the next letter"  
   
4?1f1g1h1i  
Hi  
   
"Four deleted 2 letters ¦Why does it start at three?"  
   
5?1f1g1h1i  
i  
5?2f3g4h1i  
I  
"Does it delete or does it half it? I'll do 2 3 and 4 instead of 1 1 1"  
   
\[---At this point, she tries to see if different numbers in the number letter pair affects the behavior of the question mark. She also wants to see what different values in front of the question mark does.---\]  
   
1?2f3g4h1i  
ffggghhhhi  
2?2f3g4h1i  
ffggghhhhi  
3?2f3g4h1i  
ggghhhhi  
4?2f3g4h1i  
hhhhi  
5?2f3g4h1i  
i  
6?2f3g4h1i  
   
"Just deletes all of them... okay. Now I'm going to test a question mark with things before and after"  
   
\[---At this point, she has a general idea of what the question mark does, and how it impacts the pairs before the ? based on number. She validates her theory by performing a few more tests. She thinks that the number will delete characters if the number before the question mark denotes a position after the question mark, and it will double characters if the number denotes a position before the position of the question mark. The deletion or doubling corresponds to the number.---\]  
   
1a2b3c0?2d3e4f  
Abbcccddeeeffff  
   
"One should double the abc and do nothing to the def"  
   
1a2b3c1?2d3e4f  
Abbcccabbcccddeeeffff  
"Okay"  
1a2b3c2?2d3e4f  
Abbcccbbcccddeeeffff  
"Okay, 2 works"  
1a2b3c3?2d3e4f  
Abbccccccddeeeffff  
   
"3 ... wait, it didn't delete my d's  ... weirdo  ...How does the number of pairs in front of the question mark affect things after?"  
   
\[---She still does not understand what happens when the number before the question mark denotes the position of the question mark or the position plus one. \---\]  
   
1a2b3c4?2d3e4f  
Abbcccddeeeffff  
   
"So it stopped duplicating the letters ¦ Maybe it has to stop duplicating the letters before to do anything after"  
   
1a2b3c5?2d3e4f  
abbcccddeeeffff  
1a2b3c6?2d3e4f  
Abbccceeeffff  
   
"okay, so at 6 it starts deleting my letters after ¦why 6?\! So I guess it takes two numbers of doing nothing before it starts deleting, or so it seems. So if I have only 1 letter before the question mark ¦"  
   
1a6?2d3e4f  
A  
   
\[---At this point, she is trying to figure out if her rationale for deleting and repeating (delete if number is after number of pairs before question mark \+ 1, repeat if number is before the position of the question mark, is correct and runs tests to validate---\]  
   
1a0?2d3e4f  
addeeeffff  
1a1?2d3e4f  
aaddeeeffff  
1a2?2d3e4f  
addeeeffff  
1a3?2d3e4f  
Addeeeffff  
"Four should delete the d's"  
1a4?2d3e4f  
Aeeeffff  
   
"Yaaay\! Okay, now what? Another question mark"  
   
\[---After taking CS 107, she makes sure to check all possible edge cases to make sure no strange behavior occurs. She tries with two question marks in a set of commands to see if anything strange occurs with it at the very end of the sequence \---\]  
   
1a4?2d3e4f3?  
Aeeeffff  
   
"That didn't do anything ... $\#%&"  
   
1a4?2d3e4f0?  
aeeeffff  
1a4?2d3e4f1?  
aeeeffff  
1a4?2d3e4f2?  
Aeeeffff  
   
"Why is it not doing anything?"  
   
\[---She is testing to see why if there are any edge cases with two sets of question marks---\]  
   
1a4?2d3e4f3?  
aeeeffff  
1a4?2d3e4f4?  
aeeeffff  
1a4?2d3e4f5?  
aeeeffff  
1a4?2d3e4f6?  
aeeeffff  
1a4?2d3e4f7?  
aeeeffff  
1a4?2d3e4f8?  
aeeeffff  
1a4?2d3e4f9?  
Aeeeffff  
   
"Okay, so the second question mark just doesn't do anything. Okay, now put one before it"  
   
0?1a4?2d3e4f  
addeeeffff  
1a4?2d3e4f  
aeeeffff  
1a4?2d3e4f  
Aeeeffff  
0?1a4?2d3e4f  
Addeeeffff  
   
"It nullifies the action of the second question mark, if I put it before the second one. So only the first question mark matters"  
   
\[---At this point, she tries to validate her previous assumption by keeping the pairs the same but removing the second question mark and inserting a number and question mark at the front of the line of code \---\]  
   
1?1a4?2d3e4f  
addeeeffff  
5?1a4?2d3e4f  
eeeffff  
2?1a4?2d3e4f  
addeeeffff  
4?1a4?2d3e4f  
ddeeeffff  
3?1a4?2d3e4f  
ddeeeffff  
4?1a4?2d3e4f  
Ddeeeffff  
   
"4 should delete the question mark, which doesn't do anything"  
   
5?1a4?2d3e4f  
Eeeffff  
   
"Only the first question mark does anything. So the number in front of the question marks ¦it will duplicate..the sets of letters before it. Starting from the nth set ¦okay, N is the number of sets before the question mark. It will duplicate starting from set number N until it reaches the question. If N is greater than the number of sets it doesn't duplicate anything. And then there will be two n's where it doesn't do anything. After that, it starts deleting the sets after the question mark one by one."  
   
1a2?2d3e4f  
Addeeeffff  
   
\[---I asked her, "What are you trying to do now?", because she started typing without speaking. She is trying to figure out why the N doesn't do anything if it's the position of the question mark or one after.---\]  
   
"I'm trying to make sense of why it doesn't do anything for two numbers"  
   
1a3?2d3e4f  
addeeeffff  
1a4?2d3e4f  
Aeeeffff  
   
"It keeps the ones from four on. Okay, that makes sense. So I already made sense of what it does to the sets before the question mark. So for the sets after the question mark, it deletes all the sets between the question mark and the nth set. So if I put something something 4 question mark it will only print out the stuff before the question mark and the stuff after the question mark from set 5 on."

\[--- At this point, she is sure that she is correct, and asks me for confirmation. The only thing that bothered her was the two cases she tested last. I told her that it could be seen as an equivalent of a "jump to" statement, and she exclaimed that she hadn't thought of it from a CS methodology standpoint. After thinking it through as a jump to statement, she realized that her definition was consistent to the statement, but from a less methodological viewpoint. \---\]  
