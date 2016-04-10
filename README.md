# codejam-qualificationround
Solution for Google Code Jam 2016 Qualification Round problems

only did ex01 - ex03 since that was more than double the points I needed to qualify for round 1. Maybe I'll do and upload ex04 here later for practice

The entire problem descriptions (with examples) are in the folders. Below just basic descpritions:

ex01 - Counting Sheep:

Problem

Bleatrix Trotter the sheep has devised a strategy that helps her fall asleep faster. First, she picks a number N. Then she starts naming N, 2 × N, 3 × N, and so on. Whenever she names a number, she thinks about all of the digits in that number. She keeps track of which digits (0, 1, 2, 3, 4, 5, 6, 7, 8, and 9) she has seen at least once so far as part of any number she has named. Once she has seen each of the ten digits at least once, she will fall asleep.

Bleatrix must start with N and must always name (i + 1) × N directly after i × N. For example, suppose that Bleatrix picks N = 1692. She would count as follows:

N = 1692. Now she has seen the digits 1, 2, 6, and 9.
2N = 3384. Now she has seen the digits 1, 2, 3, 4, 6, 8, and 9.
3N = 5076. Now she has seen all ten digits, and falls asleep.
What is the last number that she will name before falling asleep? If she will count forever, print INSOMNIA instead.

Input

The first line of the input gives the number of test cases, T. T test cases follow. Each consists of one line with a single integer N, the number Bleatrix has chosen.

Output

For each test case, output one line containing Case #x: y, where x is the test case number (starting from 1) and y is the last number that Bleatrix will name before falling asleep, according to the rules described in the statement.


ex02 - Revenge of the Pancakes:

Problem

The Infinite House of Pancakes has just introduced a new kind of pancake! It has a happy face made of chocolate chips on one side (the "happy side"), and nothing on the other side (the "blank side").

You are the head waiter on duty, and the kitchen has just given you a stack of pancakes to serve to a customer. Like any good pancake server, you have X-ray pancake vision, and you can see whether each pancake in the stack has the happy side up or the blank side up. You think the customer will be happiest if every pancake is happy side up when you serve them.

You know the following maneuver: carefully lift up some number of pancakes (possibly all of them) from the top of the stack, flip that entire group over, and then put the group back down on top of any pancakes that you did not lift up. When flipping a group of pancakes, you flip the entire group in one motion; you do not individually flip each pancake. Formally: if we number the pancakes 1, 2, ..., N from top to bottom, you choose the top i pancakes to flip. Then, after the flip, the stack is i, i-1, ..., 2, 1, i+1, i+2, ..., N. Pancakes 1, 2, ..., i now have the opposite side up, whereas pancakes i+1, i+2, ..., N have the same side up that they had up before.

For example, let's denote the happy side as + and the blank side as -. Suppose that the stack, starting from the top, is --+-. One valid way to execute the maneuver would be to pick up the top three, flip the entire group, and put them back down on the remaining fourth pancake (which would stay where it is and remain unchanged). The new state of the stack would then be -++-. The other valid ways would be to pick up and flip the top one, the top two, or all four. It would not be valid to choose and flip the middle two or the bottom one, for example; you can only take some number off the top.

You will not serve the customer until every pancake is happy side up, but you don't want the pancakes to get cold, so you have to act fast! What is the smallest number of times you will need to execute the maneuver to get all the pancakes happy side up, if you make optimal choices?

Input

The first line of the input gives the number of test cases, T. T test cases follow. Each consists of one line with a string S, each character of which is either + (which represents a pancake that is initially happy side up) or - (which represents a pancake that is initially blank side up). The string, when read left to right, represents the stack when viewed from top to bottom.

Output

For each test case, output one line containing Case #x: y, where x is the test case number (starting from 1) and y is the minimum number of times you will need to execute the maneuver to get all the pancakes happy side up.


ex03 - Coin Jam:

Problem

A jamcoin is a string of N ≥ 2 digits with the following properties:

Every digit is either 0 or 1.
The first digit is 1 and the last digit is 1.
If you interpret the string in any base between 2 and 10, inclusive, the resulting number is not prime.
Not every string of 0s and 1s is a jamcoin. For example, 101 is not a jamcoin; its interpretation in base 2 is 5, which is prime. But the string 1001 is a jamcoin: in bases 2 through 10, its interpretation is 9, 28, 65, 126, 217, 344, 513, 730, and 1001, respectively, and none of those is prime.

We hear that there may be communities that use jamcoins as a form of currency. When sending someone a jamcoin, it is polite to prove that the jamcoin is legitimate by including a nontrivial divisor of that jamcoin's interpretation in each base from 2 to 10. (A nontrivial divisor for a positive integer K is some positive integer other than 1 or K that evenly divides K.) For convenience, these divisors must be expressed in base 10.

For example, for the jamcoin 1001 mentioned above, a possible set of nontrivial divisors for the base 2 through 10 interpretations of the jamcoin would be: 3, 7, 5, 6, 31, 8, 27, 5, and 77, respectively.

Can you produce J different jamcoins of length N, along with proof that they are legitimate?

Input

The first line of the input gives the number of test cases, T. T test cases follow; each consists of one line with two integers N and J.

Output

For each test case, output J+1 lines. The first line must consist of only Case #x:, where x is the test case number (starting from 1). Each of the last J lines must consist of a jamcoin of length N followed by nine integers. The i-th of those nine integers (counting starting from 1) must be a nontrivial divisor of the jamcoin when the jamcoin is interpreted in base i+1.

All of these jamcoins must be different. You cannot submit the same jamcoin in two different lines, even if you use a different set of divisors each time.


ex04 - Fractiles:

Problem

Long ago, the Fractal civilization created artwork consisting of linear rows of tiles. They had two types of tile that they could use: gold (G) and lead (L).

Each piece of Fractal artwork is based on two parameters: an original sequence of K tiles, and a complexity C. For a given original sequence, the artwork with complexity 1 is just that original sequence, and the artwork with complexity X+1 consists of the artwork with complexity X, transformed as follows:

replace each L tile in the complexity X artwork with another copy of the original sequence
replace each G tile in the complexity X artwork with K G tiles
For example, for an original sequence of LGL, the pieces of artwork with complexity 1 through 3 are:

C = 1: LGL (which is just the original sequence)
C = 2: LGLGGGLGL
C = 3: LGLGGGLGLGGGGGGGGGLGLGGGLGL
Here's an illustration of how the artwork with complexity 2 is generated from the artwork with complexity 1:



You have just discovered a piece of Fractal artwork, but the tiles are too dirty for you to tell what they are made of. Because you are an expert archaeologist familiar with the local Fractal culture, you know the values of K and C for the artwork, but you do not know the original sequence. Since gold is exciting, you would like to know whether there is at least one G tile in the artwork. Your budget allows you to hire S graduate students, each of whom can clean one tile of your choice (out of the KC tiles in the artwork) to see whether the tile is G or L.

Is it possible for you to choose a set of no more than S specific tiles to clean, such that no matter what the original pattern was, you will be able to know for sure whether at least one G tile is present in the artwork? If so, which tiles should you clean?

Input

The first line of the input gives the number of test cases, T. T test cases follow. Each consists of one line with three integers: K, C, and S.

Output

For each test case, output one line containing Case #x: y, where x is the test case number (starting from 1) and y is either IMPOSSIBLE if no set of tiles will answer your question, or a list of between 1 and S positive integers, which are the positions of the tiles that will answer your question. The tile positions are numbered from 1 for the leftmost tile to KC for the rightmost tile. Your chosen positions may be in any order, but they must all be different.

If there are multiple valid sets of tiles, you may output any of them. Remember that once you submit a Small and it is accepted, you will not be able to download and submit another Small input. See the FAQ for a more thorough explanation. This reminder won't appear in problems in later rounds.

