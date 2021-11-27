# Whiteboard Advice
Whiteboard-style interviews are ubiquitous in the tech industry.
For those who not had the pleasure, whiteboard interviewing is the practice of asking candidates to solve technical questions on a whiteboard,
piece of paper, or computer during the interview. This kind of environment can feel like a pressure cooker and cause even the most competent engineer to fall apart.

### The Advice: Communicate!
The best piece of technical interview advice I have received and can impart upon you is to communicate, communicate,
communicate! This may seem like an anti-climactic piece of advice, but I hope to be able to demonstrate to you that it’s actually the most important skill to prepare prior to an interview.

Note: as I discuss examples in the rest of this article, they will have a software engineering slant as it is the most familiar domain to me.
Despite that slant, you can apply these skills to any whiteboard-style interview.


### What Do You Mean Communicate?
Let’s say you are in the interview and your interviewers throw you a whiteboard question. Do you step up to the whiteboard and feverishly start solving the problem?
That tends to be everyone’s instinct, but it’s definitely not the right way to go. Even if you think you understand the problem, you should take some very important steps before moving forward.

### Ask About Edge Cases
It’s still not time to dive right into coding the solution. Think for a bit about the inputs and expected output and think about potential edge cases to the problem. Ask about them. In many cases, the interviewer hasn’t even thought about edge cases and will make something up. That’s great — it shows you’re analytical and will work hard to try to prevent bugs (which often crop up due to edge cases).

### Ask About Test Cases
This is free and you should take advantage of it. Simply ask if there are any test cases that the function should pass. Your interviewer might be expecting you to ask this question, so it might be necessary. But it’s also possible the interviewer was not expecting the question and will think “ah, this candidate knows about testing!”

### Write Pseudocode and Ask If It Makes Sense
Again, you don’t actually want to start writing code in an actual language. You’ll find yourself constrained by trying to remember the methods or other idiosyncrasies of the language rather than trying to come up with the correct logic. Instead, let your interviewer know you’re going to start by writing pseudocode and fill in the actual code later. (Coincidentally, this is a reasonable way to write actual code as well).

### Write the Actual Code and Ask if it Looks Good
You should now convert your pseudocode into actual code. You don’t even need to remove the comments. At this point, you just need to plug the appropriate code for your language in. If you forget some syntax or a method name, you should be able to ask your interviewer for this information without too much grief. If they give you trouble, just say you’ll leave it as pseudocode for now.

#### We’re All Human
Above all, remember that we’re all human. Your interviewer has been in your position and understands the stress of a technical interview. Your interviewer has probably seen quite a few candidates sweating it out, but possibly very few open who openly discuss problems in a conversational manner. If you can achieve this, you’ll be in great shape.

#### What Has Your Experience Been?
Have you been in a technical interview where communication saved you? Have you had the opposite experience? Let me know in the comments! I’d love to hear about your experiences.


# 7 tips to ace a programming interview
## 1. Take a few minutes.
Speaking as an interview coach, this is one misstep that I see all the time during mock interviews. The canonical tip that everyone gives is, “talk more!”. What most of those well-meaning advice-givers overlook, however, is that talking and thinking at the same time is extremely hard. Nervous interviewees will jump straight into talking, passing up a great opportunity for concentrated thought.


## 2. Write down the steps of the solution.
Even after you have an idea of how to attack the problem, don’t start writing code down. Write down the general steps of how you will solve it on one side of the whiteboard, where it’s visible but won’t get in the way. You don’t need to be verbose, just get the steps in order and somewhat readable.
- Start at middle of array.
- Keep variables tracking left and right boundaries of search area.
- If value equal to search_val, return true.
- If left and right boundaries are adjacent, return false.
- If value bigger than search_val, go halfway towards left boundary, and move the right boundary along with us.
- If value smaller than search_val, go halfway towards right boundary, and move the left boundary along with us.

## 3. Write pseudocode first.
Time to write code? Nope. Take a “dry run” at writing the code by writing some pseudocode. Often we run into problems halfway through writing the code, and there’s no point wasting time over syntax when you might have to throw the code away. Instead, write some half-baked code-looking stuff that lays out the structure of how your code will work. Do it over on the side of the whiteboard, so you have space left to work.

## 4. Don’t sweat the small stuff.
Programming interviews are not about how well you’ve remembered your semicolons, nor are they about being able to remember all of the flags on a TCP packet. They’re about demonstrating depth and breadth of knowledge, personality strengths, and problem-solving abilities. If you make a mistake, it’s okay. Brush it off and move on.

## 5. Sit down. Be humble.
A programming interview isn’t just a written exam. It’s an assessment of your programming abilities, and there are plenty of things that fall into that category beyond mere coding prowess. 

## 6. Come prepared.
When it comes to programming interviews, there is no substitute for HOBIS (which stands for Hours of Butt-In-Seat). If you want to be ready, you have to put in the time. It’s important in order to maximize your chances of acing the interview, but it’s also important for your peace of mind during the interview and afterwards. In the interview, knowing that you’ve done all you can to prepare helps you stay calm and cool, and increases your chances of success. And afterwards, regardless of the outcome, knowing that you could not have reasonably done more to prepare helps you feel proud of your work and start moving towards your next goal.

## 7. Review your work.
You won’t always finish questions in the time permitted, but occasionally you’ll have extra time after coming up with a solution. If this happens, it’s tempting to say “Well, I’m done!”. Interviews are stressful and we want them to be over as fast as possible. This is reasonable, but:
Think about how silly you look if your solution is not right.
