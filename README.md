Download Link: https://assignmentchef.com/product/solved-ada-homework-1-ada-meetup
<br>
<strong>Problem 1 – ADA Meetup (Programming) </strong>

<h2>Problem Description</h2>

<em>N </em>people are lining up to enter a meetup held by the Aged Drivers Association, also known as the ADA. Each person is characterized by two parameters: a preference index <em>p<sub>i </sub></em>and a friendliness factor <em>f<sub>i</sub></em>. The former indicates what a person likes, and the closer two people’s indices are, the more similar their tastes are, and vice versa. The friendliness factor, on the other hand, indicates how friendly a person is. A person with a higher friendliness factor is more tolerant to people with different tastes. As we all know, old drivers tend to argue about which kinds of cars are better for driving. Therefore, when the <em>i</em>-th person enters the room, the person will only greet those whose tastes the person considers tolerable.

More formally, person <em>i </em>will greet the person <em>j </em>if and only if <em>i &gt; j </em>and |<em>p<sub>j </sub></em>− <em>p<sub>i</sub></em>| ≤ <em>f<sub>i</sub></em>. WillyPillow, being a weeb with no friends to greet, decides to count the number of greetings that takes place.

<h2>Input</h2>

The first line of the input file contains an integer indicating <em>N</em>.

The second line contains <em>N </em>integers separated by spaces, with the <em>i</em>-th integer indicating <em>p<sub>i</sub></em>, the preference index of the <em>i</em>-th person.

The third line contains <em>N </em>integers separated by spaces, with the <em>i</em>-th integer indicating <em>f<sub>i</sub></em>, the

friendliness level of the <em>i</em>-th person.

<strong>Test Group 0                                                               Test Group 2 </strong>

<ul>

 <li>Sample Input 1 ≤ <em>N </em>≤ 5 × 10<sup>3</sup></li>

 <li>0 ≤ <em>p<sub>i</sub>,f<sub>i </sub></em>≤ 10<sup>9</sup></li>

</ul>

<strong>Test Group 1 </strong>

<strong>Test Group 3 </strong>

<ul>

 <li>1 ≤ <em>N </em>≤ 10<sup>6</sup></li>

 <li>0 ≤ <em>p<sub>i</sub>,f<sub>i </sub></em>≤ 10<sup>9 </sup> 1 ≤ <em>N </em>≤ 10<sup>6</sup></li>

 <li>|<em>f<sub>i </sub></em>− 5 × 10<sup>8</sup>| ≥ 5 × 10<sup>8 </sup> 0 ≤ <em>p<sub>i</sub>,f<sub>i </sub></em>≤ 10<sup>9</sup></li>

</ul>

<h2>Output</h2>

Please output an integer indicating the number of greetings that takes place.

<h1>Sample Input 1                                                        Sample Input 2</h1>

5                                                                                                           10

18 0 14 8 12                                                                                            17 17 10 10 0 1 6 6 17 13

9 8 14 4 11                                                                                               12 16 18 12 16 6 6 16 15 16

<h1>Sample Output 1                                                     Sample Output 2</h1>

5                                                                                                           35

<h2>Hint</h2>

Because the input files are large, please add

<ul>

 <li>std::ios base::sync with stdio(false);</li>

 <li>std::cin.tie(nullptr); to the beginning of the main function if you’re using std::cin.</li>

</ul>

<strong>Problem 2 – Maximum Subarray Revisited (Programming) (10 points)</strong>

<h2>Problem Description</h2>

WillyPillow has recently learned about the famous <em>Maximum Subarray Problem </em>in the <em>Algorithm Design and Analysis </em>course. However, this problem had already been studied by many people for a long time, which makes it less challenging to solve for WillyPillow. Therefore, he quickly came up with the <em>dynamic </em>version of the maximum subarray problem, but was not able to solve it. Since WillyPillow has no friends to discuss with, you decide to help him with the modified task.

Formally speaking, you are given an integer array <em>A </em>of length <em>N </em>and <em>Q </em>updates. The <em>i</em>-th update is specified by two integers <em>p<sub>i</sub>,v<sub>i</sub></em>, meaning that the <em>p<sub>i</sub></em>-th entry of <em>A </em>is updated to <em>v<sub>i</sub></em>. You should output the answer to the <em>Maximum Subarray Problem </em>on the modified array after each update. Recall that the answer to the <em>Maximum Subarray Problem </em>is

!

In particular, if the answer is negative, you should output 0 instead.

<h2>Input</h2>

The first line of the input contains two integers <em>N </em>and <em>Q</em>, representing the length of the array and the number of updates, respectively.

The second line contains <em>N </em>integers, representing the original array <em>A</em>.

<em>Q </em>lines follow, the <em>i</em>-th of which contains two integers <em>p<sub>i</sub>,v<sub>i</sub></em>, representing an update of <em>A<sub>p</sub></em><em><sub>i </sub></em>into <em>v<sub>i</sub></em>.

<ul>

 <li>1 ≤ <em>N,Q </em>≤ 5 · 10<sup>5</sup></li>

 <li>|<em>A<sub>i</sub></em>| ≤ 10<sup>9</sup></li>

 <li>1 ≤ <em>p<sub>i </sub></em>≤ <em>N</em></li>

 <li>|<em>v<sub>i</sub></em>| ≤ 10<sup>9</sup></li>

</ul>

<strong>Test Group 0                                                                    Test Group 3 </strong>

<ul>

 <li><em>N,Q </em>≤ 2000 <em>N,Q </em>≤ 10<sup>5</sup></li>

</ul>

<strong>Test Group 1  Test Group 4  </strong>• <em>N,Q </em>≤ 5000 • No other constraints.

<strong>Test Group 2 </strong>

<ul>

 <li><em>Q </em>= 0</li>

</ul>

<h2>Output</h2>

Output <em>Q </em>+ 1 lines. The first line should contain the answer before any updates. The rest <em>Q </em>lines should contain the answer after each update, following the chronological order.

<strong>Sample Input 1                                                        Sample Output 1</strong>

10 10                                                                                                   10

-1 -5 -10 0 7 -1 4 -6 -3 -4                                                              4

5 -4                                                                                                      10

3 10                                                                                                     10

5 -5                                                                                                      10

10 8                                                                                                     8

3 -2                                                                                                      10

8 1                                                                                                        9

10 7                                                                                                     9

1 -7                                                                                                      9

<ul>

 <li>4 16</li>

 <li>9</li>

</ul>

<h2>Hint</h2>

It may be useful to store the recursion tree of the Divide and Conquer approach to the classic maximum subarray problem.

Because the input files are large, please add

<ul>

 <li>std::ios base::sync with stdio(false);</li>

 <li>std::cin.tie(nullptr); to the beginning of the main function if you’re using std::cin.</li>

</ul>

<strong>Problem 3 – Good Subpermutations (Programming) (15 points)</strong>

<h2>Problem Description</h2>

A continuous segment [<em>l,r</em>] of a permutation <em>P </em>is <em>good </em>if the value of (<em>P<sub>l</sub>,P<sub>l</sub></em><sub>+1</sub><em>,…,P<sub>r</sub></em>) is also continuous. That is, if we collect <em>P<sub>l</sub>,P<sub>l</sub></em><sub>+1</sub><em>,…,P<sub>r </sub></em>into a new list <em>B </em>and sort it, then <em>B</em><sub>1 </sub>= <em>B</em><sub>2 </sub>− 1<em>,B</em><sub>2 </sub>= <em>B</em><sub>3 </sub>− 1<em>,…,B<sub>i</sub></em>−<sub>1 </sub>= <em>B<sub>i </sub></em>− 1<em>,…,B</em><sub>|<em>B</em></sub>|−<sub>1 </sub>= <em>B</em><sub>|<em>B</em></sub>| − 1 hold.

Given a permutation <em>P </em>of length <em>N</em>, count the number of good segments. Note that a sequence <em>A </em>of <em>N </em>integers is called a permutation of length <em>N </em>if 1 ≤ <em>A<sub>i </sub></em>≤ <em>N </em>for all 1 ≤ <em>i </em>≤ <em>N </em>and <em>A<sub>i </sub></em>6= <em>A<sub>j </sub></em>for all 1 ≤ <em>i </em>6= <em>j </em>≤ <em>N</em>.

<h2>Input</h2>

The first line contains an integer <em>N </em>indicating the length of the permutation, where 1 ≤ <em>N </em>≤ 5 · 10<sup>5</sup>. The second line contains <em>N </em>integers <em>P<sub>i </sub></em>indicating the input sequence. It’s guaranteed that the input sequence is a permutation of length <em>N</em>.

<table width="499">

 <tbody>

  <tr>

   <td width="328"><strong>Test Group 0 (10 %)</strong>•    <em>N </em>≤ 200<strong>Test Group 1 (10 %)</strong>•    <em>N </em>≤ 2000</td>

   <td width="171"><strong>Test Group 3 (50 %)</strong>•    <em>N </em>≤ 10<sup>5</sup><strong>Test Group 4 (10 %)</strong>•    No other constraints.</td>

  </tr>

 </tbody>

</table>

<strong>Test Group 2 (20 %)</strong>

<ul>

 <li><em>N </em>≤ 5000</li>

</ul>

<h2>Output</h2>

Print an integer indicating the number of <em>good segments </em>in the given permutation.

<strong>Sample Input 1                                                        Sample Output 1</strong>

5                                                                                                           15

1 2 3 4 5

<strong>Sample Input 2                                                        Sample Output 2</strong>

5                                                                                                           10

5 1 2 4 3

<strong>Sample Input 3                                                        Sample Output 3</strong>

10                                                                                                         26

7 6 5 8 9 10 1 2 3 4

<h2>Sample Input 4</h2>

20

1 2 3 4 10 9 8 7 6 5 11 14 13 12 20 19 18 17 16 15

<strong>Sample Output 4</strong>

81

<strong>Hint</strong>

The following observation might be useful:

<ul>

 <li>The value of a set of numbers <em>S </em>is continuous if and only if</li>

</ul>

<strong>Problem 4 – Different Strings (Programming) (15 points)</strong>

<h2>Problem Description</h2>

You are given two strings <em>S</em><sub>1 </sub>and <em>S</em><sub>2</sub>, and you have 3 string operations:

<ul>

 <li><strong>Insertion </strong>of a single character. If <em>a </em>= <em>uv</em>, then inserting a character <em>x </em>between <em>u </em>and <em>v </em>produces <em>uxv</em>.</li>

 <li><strong>Deletion </strong>of a single character. For example, deleting <em>x </em>changes <em>uxv </em>to <em>uv</em>.</li>

 <li><strong>Substitution </strong>of a single character. For example, substituting <em>x </em>for a character <em>y </em>6= <em>x </em>changes <em>uxv </em>to <em>uyv</em>.</li>

</ul>

Your goal is to use these operations to make all the corresponding characters in these two strings different. To be more specific, we need to change and, such that:

] for 0

You need to output the minimum number of operations needed to change the two strings.

<h2>Input</h2>

There are two lines, which are <em>S</em><sub>1 </sub>and <em>S</em><sub>2</sub>.

<ul>

 <li><em>S</em><sub>1 </sub>and <em>S</em><sub>2 </sub>contain only uppercase and lowercase alphabets.</li>

 <li>|<em>S</em><sub>1</sub>|<em>,</em>|<em>S</em><sub>2</sub>| ≤ 2000</li>

</ul>

<h2>Output</h2>

An integer indicates the minimum number of operations needed.

<strong>Subtask 1 (25 %)</strong>

<ul>

 <li><em>S</em><sub>1 </sub>and <em>S</em><sub>2 </sub>contains only alphabet “A”.</li>

</ul>

<strong>Subtask 2 (25 %)</strong>

<ul>

 <li><em>S</em><sub>1 </sub>and <em>S</em><sub>2 </sub>contains only alphabets “A” and “B”.</li>

</ul>

<strong>Subtask 3 (50 %)</strong>

<ul>

 <li>No other constraints.</li>

</ul>




<strong>Sample Input 1                                                        Sample Input 2</strong>

abcdcdc                                                                                            AAAAA

abcddc                                                                                              AAAA

<strong>Sample Output 1                                                     Sample Output 2</strong>

2                                                                                                           4

<h1>Problem 5 – Time Complexity &amp; Recurrence (Hand-Written) (15</h1>

<strong>points)</strong>

<em>Note</em>: In this problem, if you use any theorem not covered by the lectures, slides, and the textbook, you should prove it first.

<ul>

 <li><strong>Asymptotic Notations </strong>(5%, 1% each)</li>

</ul>

<em>True </em>or <em>False</em>.

If your answer is <em>True</em>, no explanation is needed.

If your answer is <em>False</em>, give a <strong>counterexample</strong>, or <strong>briefly </strong>explain the reason.

<em>Note</em>: All functions (<em>f</em>(<em>n</em>), <em>g</em>(<em>n</em>)) mentioned below are <strong>non-negative </strong>and <strong>increasing</strong>.

<ul>

 <li><em>f</em>(<em>n</em>) + <em>g</em>(<em>n</em>) = <em>O</em>(min(<em>f</em>(<em>n</em>)<em>,g</em>(<em>n</em>)))</li>

 <li><em>e<sup>f</sup></em><sup>(<em>n</em>) </sup>= <em>O</em>(<em>e<sup>g</sup></em><sup>(<em>n</em>)</sup>) implies <em>f</em>(<em>n</em>) = <em>O</em>(<em>g</em>(<em>n</em>))</li>

</ul>

)), then <em>f</em>(<em>n</em>) + <em>g</em>(<em>n</em>) = Θ(<em>f</em>(<em>n</em>))

<ul>

 <li><strong>Solve Recurrences </strong>(10%)</li>

</ul>

Give the tight bound (Θ-bound, <em>e.g. T</em>(<em>n</em>) = Θ(<em>n</em><sup>3</sup>)) of the following recurrence equations. Assume: <em>T</em>(<em>n</em>) = 1<em>,</em>∀<em>n </em>≤ 1

<em>Note</em>: Show your derivation thoroughly. Following hints is strongly recommended.

(<em>hint: use the transformation</em>

(<em>hint: expand the equation to observe the pattern; recall</em>

<strong>Problem 6 – Controllable Ghost Leg (Hand-Written) (20 points)</strong>

“Ghost Leg”, known in Japan as Amidakuji (“Amida lottery” because the paper was folded into a fan shape resembling Amida’s halo), is a method of lottery designed to create random pairings between two sets of the same number of prizes. This is often used to distribute prizes to people, where the number of prizes is the same as the number of people.

Ghost Leg consists of vertical lines with horizontal lines connecting two adjacent vertical lines; the horizontal lines are called “legs”. Note that “legs” cannot touch other legs. The number of vertical lines equals the number of people, and at the bottom of each line there is an item – a prize that will be paired with a player. The general rule for this game is: choosing a line on the top, and following it downwards. When a horizontal line is encountered, the player needs to transit to another vertical line and then continue going down. The procedure is repeated until reaching the end of the vertical line, and then the player gets the corresponding prize. Therefore, choosing the line decides which prize you get. You can refer to the link for more details: https://en.wikipedia.org/wiki/Ghost_Leg.

The example of one ghost leg.                       Example of finding the prize if A is chosen.

You, the host of the party, want to distribute <em>N </em>prizes to <em>N </em>players by ghost leg. In addition, you plan to perform some black-box tricks on this game so that the person choosing a specific start must be able to get a specific prize you planned.

Here comes a problem: Now given a ghost leg board without any horizontal lines, you have <em>k </em>constraints, which assign <em>k </em>starting points with their corresponding prizes. What is the minimum number of horizontal lines to be added in order to satisfy all <em>k </em>constraints?

For example, you have a ghost leg without any horizontal lines as Fig. 1, and the constraints are {(c should go to 1), (b should go to 4)}. Thus, the answer should be 3, and one of the solution is illustrated in Fig. 2.

Fig 1. An empty ghost leg if <em>N </em>= 4                     Fig 2. A solution meets all the constraints

Before solving this problem, “inversion” is introduced for helping you find the solution.

<strong>Inversion </strong>Given a sequence of unique numbers <em>B </em>= <em>b</em><sub>1</sub><em>,b</em><sub>2</sub><em>,…,b<sub>n</sub></em>, an inversion is a pair of numbers <em>b<sub>i </sub></em>and <em>b<sub>j </sub></em>in this sequence such that <em>i &lt; j </em>and <em>b<sub>i </sub>&gt; b<sub>j </sub></em>. Let <em>I</em>(<em>B</em>) be the set of inversions in <em>B</em>. For example, if <em>B </em>= 1<em>,</em>3<em>,</em>5<em>,</em>2, <em>I</em>(<em>B</em>) = {(3<em>,</em>2)<em>,</em>(5<em>,</em>2)}, and the number of inversions is 2 (|<em>I</em>(<em>B</em>)| = 2).

<ul>

 <li>Given an unsorted and unique sequence <em>B </em>with <em>n </em>numbers, please design an efficient algorithm to calculate the number of inversions |<em>I</em>(<em>B</em>)| in <em>O</em>(<em>N </em>log<em>N</em>) time. (7 points)</li>

 <li>Explain why your algorithm runs in <em>O</em>(<em>N </em>log<em>N</em>). (5 points)</li>

 <li>Prove that the number of exchanges when performing bubble sort on the sequence <em>S </em>is equal to the number of inversions in <em>S</em>. (2 points)</li>

</ul>

<strong>Controllable Ghost Leg</strong>

<ul>

 <li>Describe a <em>O</em>(<em>N </em>log<em>N</em>) algorithm that calculates the minimum number of horizontal lines when |<em>constraints</em>| = <em>N</em>. You are required to prove the correctness in this problem. (2 points)</li>

 <li>Describe a <em>O</em>(<em>N </em>log<em>N</em>) algorithm that calculates the minimum number of horizontal lines when</li>

</ul>

|<em>constraints</em>| ≤ <em>N</em>. You are required to prove the correctness in this problem. (4 points)

<strong>Problem 7 – Folding Blocks (Hand-Written) (15 points)</strong>

“Folding Blocks” is a puzzle game, in which you need to unfold the blocks in order to fill the whole space. When you unfold a block, the block is extended with the same size to the unfolding direction. You can play the 2D version of this game here: https://www.crazygames.com/game/ folding-blocks-puzzle.

Here we play the puzzle on a 1D board, where the whole space can be viewed as a line illustrated below. If a 2-length block initially fills 3-4 positions, and now we unfold it to the right side, it will fill 3-6 positions of the board. Similarly, if we unfold it to the left side, it will fill 1-4 positions of the board.

Now given the length of the board, denoted as <em>N</em>, and the initial status (each block’s length and position), please decide whether this puzzle can be solved. Note that the given position of the block is its leftmost side and a puzzle is <em>solved </em>once all positions are filled after unfolding without overlapping or out-of-board blocks.

Fig 1. You can unfold the block to the left or right, but you cannot overlap other blocks or make blocks out of board when unfolding.

Fig 2. There’s an example puzzle and solution.

<ul>

 <li>Let’s start with a special case which has only a block on the board initially. Derive a method which can determine whether the problem is solvable in constant time. (Assume the time complexity of a logarithmic operation (log) is <em>O</em>(1)) (2 points)</li>

 <li>Assume there is only one block on the board initially. Design a <em>O</em>(log<em>N</em>) algorithm to output the sequence of unfold operations that solve the puzzle if it is solvable. (1 point)</li>

 <li>Assume there is only one block on the board and the distance between the block to the left and right boundaries are <em>d</em><sub>1 </sub>and <em>d</em><sub>2</sub>, respectively. Prove that there are <em>O</em>(<em>d</em><sub>1 </sub>+ <em>d</em><sub>2</sub>) possibilities of the status after unfold operations. You can think of a status as a binary array representing whether each position is occupied. (3 points)</li>

 <li>Let’s now consider the general case which can contain more than one block initially. Please design a DP algorithm to solve the problem in <em>O</em>(<em>N</em>) time. (5 points)</li>

 <li>Explain your algorithm in (4) in terms of the properties of overlapping sub-problems and optimal substructure. (2 points)</li>

 <li>Prove that the time complexity of your DP algorithm is Θ(<em>N</em>). (2 points)</li>

</ul>