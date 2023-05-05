Download Link: https://assignmentchef.com/product/solved-csie-homework-2
<br>
<ul>

 <li>std::cin.tie(nullptr); to the beginning of the main function if you are using std::cin.</li>

</ul>

<strong>Problem 1 – Glass Bridge 2.0 </strong><a href="https://ada-judge.csie.ntu.edu.tw/#!/"><strong>(Programming)</strong></a>

<strong>Problem Description</strong>

Improved from the fifth game in <a href="https://www.netflix.com/tw-en/title/81040344"><em>Squid Game (2021)</em></a><a href="https://www.netflix.com/tw-en/title/81040344">,</a> Glass Bridge 2.0 is another deadly game played on an <em>n</em>×<em>m </em>grid, where contestants have to reach the goal cell by jumping from a square glass to another. To better describe the environment, we use (<em>i,j</em>) to denote the cell on the <em>i</em>-th row and on the <em>j</em>-th column. The starting cell is located on (1<em>,</em>1) while the goal one is located on (<em>n,m</em>). For each of the remaining cells, the cell (<em>i,j</em>) satisfies <strong>exactly one </strong>of the following states:

<ul>

 <li>The cell is placed with a square glass with a given risk value, since the glass may be smashed when you step on it. To make the game more exciting, there may be a bundle of banknotes on that piece of glass. Considering the revenue and risk, the <strong>expected profit </strong>could be modeled as <em>a<sub>i,j </sub></em>if one jumps onto the glass.</li>

 <li>The cell is empty, since a previous contestant has smashed the glass there. In other words, the cell is now impassable – if one steps on this cell, she/he will fall into a horrible abyss immediately.</li>

</ul>

You, as the next contestant to move on, are going to reach the goal cell by jumping from one cell to another. A jump from (<em>x,y</em>) to (<em>x</em><sup>0</sup><em>,y</em><sup>0</sup>) is valid if <strong>all </strong>of the following conditions hold:

<ul>

 <li>The cell (<em>x</em><sup>0</sup><em>,y</em><sup>0</sup>) is placed with a square glass.</li>

 <li><em>x </em>≤ <em>x</em><sup>0 </sup>≤ <em>n</em></li>

 <li><em>y </em>≤ <em>y</em><sup>0 </sup>≤ <em>m</em></li>

 <li>1 ≤ (<em>x</em><sup>0 </sup>− <em>x</em>) + (<em>y</em><sup>0 </sup>− <em>y</em>) ≤ <em>k</em></li>

</ul>

Currently standing on the starting cell, (1<em>,</em>1), you would like to first realize if it is possible to reach the goal cell with those currently existing glasses. If so, please come up with a jumping path such that <em>S</em>, the sum of expected profit over all cells on your path, is maximized.

<strong>Input</strong>

The first line of the input contains 1 integer <em>T </em>– the number of test cases. Then, in each test case: • The first line is an empty line. This may make it more friendly for you to distinguish between test cases with your naked eyes.

<ul>

 <li>The second line contains 3 integers <em>n,m,k</em>, denoting the size of the grid and your jumping ability.</li>

 <li>Then, <em>n </em>lines follow, the <em>i</em>-th of which contains <em>m </em>strings or integers, the <em>j</em>-th of which is:

  <ul>

   <li>0, if (<em>i,j</em>) = (1<em>,</em>1) or (<em>n,m</em>).</li>

   <li><em>a<sub>i,j</sub></em>, if the cell (<em>i,j</em>) is placed with a square glass.</li>

   <li>“X” (without quotation marks), if the cell (<em>i,j</em>) is empty.</li>

  </ul></li>

</ul>

<strong>Constraints</strong>

<ul>

 <li>1 ≤ <em>T </em>≤ 100</li>

 <li>1 ≤ <em>n,m </em>≤ 10<sup>6</sup></li>

 <li>2 ≤ <em>nm </em>≤ 10<sup>6</sup></li>

 <li><sup>X</sup><em>nm </em>≤ 10<sup>6</sup></li>

 <li>1 ≤ <em>k </em>≤ <em>n </em>+ <em>m </em>− 2</li>

 <li>−456<em>,</em>456<em>,</em>456<em>,</em>456 ≤ <em>a<sub>i,j </sub></em>≤ 456<em>,</em>456<em>,</em>456<em>,</em>456</li>

 <li>You may obtain up to 10<em>.</em>2 points from this problem even if your solution is not fully accepted.</li>

</ul>

<table width="599">

 <tbody>

  <tr>

   <td width="219"><strong>Test Group 0 (0 %)</strong>• Sample Input</td>

   <td width="380"><strong>Test Group 1 (15 %)                                         Test Group 2 (25 %)</strong>•   <em>n,m </em>≤ 30   • <em>n,m </em>≤ 30•   <em>k </em>= 1</td>

  </tr>

  <tr>

   <td width="219"><strong>Test Group 3 (45 %)</strong></td>

   <td width="380"><strong>Test Group 4 (15 %, Bonus Subtask)</strong></td>

  </tr>

 </tbody>

</table>

<ul>

 <li>= 1 and No additional constraint</li>

</ul>

<strong>Output</strong>

For each test case:

<ul>

 <li>In the first line, please output a string <em>s</em>. <em>s </em>= Passable if it is possible for you to reach the goal cell with those currently existed glasses. Otherwise, <em>s </em>= Impassable.</li>

 <li>If <em>s </em>= Passable, you have to specify your jumping path. In the second line, please output <em>S</em>, the maximized sum of the expected profit. In the third line, please output <em>L</em>, the length (including the starting and goal cells) of your path planned. Then <em>L </em>lines follow, the <em>i</em>-th of which should contain 2 integers, <em>x<sub>i</sub>,y<sub>i</sub></em>, denoting the <em>i</em>-th coordinate in your path. Note that you <strong>don’t </strong>have to minimize the length of your path. If there are multiple solutions, you may print any.</li>

</ul>

<a href="https://imgur.com/a/PYMCu8v"><strong>Hint</strong></a>

<ol>

 <li>Since each input includes several independent test cases, please carefully clear all results of the</li>

</ol>

current test case before dealing with the next one.

<ol start="2">

 <li>In Sample Input 1, the first and second test cases are exactly the same. However, the Sample Output comes up two different paths to answer the same test case. This is just a demonstration on the special scoring method.</li>

 <li>Test Group 4 may be a challenging subtask. This could be viewed as a bonus subtask since you are still able to obtain 50 points from programming problems even without solving it. Nevertheless, you are encouraged to give it a try because it’s solvable without any advanced data structure or algorithm – what you need is just an ingenuity!</li>

</ol>

<strong>Sample Input 1                                                        Sample Output 1</strong>

5                                                                                 Passable

-1

3 3 1                                                                           5

<a href="#_Toc22740">0 0 0 1                                                                                                                                                     1</a>

<a href="#_Toc22741">-1 0 -1 1                                                                                                                                                   2</a>

<a href="#_Toc22742">X -1 0 2                                                                                                                                                    2</a>

<a href="#_Toc22743">3                                                                                                                                                             2</a>

<a href="#_Toc22744">3 3 1 3                                                                                                                                                     3</a>




<h1><a name="_Toc22740"></a>0 0 0                                                                            Passable</h1>

<h1><a name="_Toc22741"></a>-1 0 -1                                                                         -1</h1>

<h1><a name="_Toc22742"></a>X -1 0                                                                          5</h1>

1 1

3 3 1                                                                           1 2

0 -7 X                                                                          2 2

X X 20                                                                         2 3

0 10 0                                                                          3 3

Impassable

3 3 2                                                                            Passable

0 -7 X                                                                          13

X X 20                                                                         4

<ul>

 <li>13 0 1 1</li>

 <li>2</li>

</ul>

5 7 9                                                                           2 3

0 X X X X X X                                                                3 3

X X X X X X X                                                                 Passable

X X X -456456456456 X X X                                           -456456456456

X X X X X X X                                                                3

X X X X X X 0                                                                1 1

<h2><a name="_Toc22743"></a>3 4</h2>

5 7

<strong>Behind the Scene</strong>

Some wise words from YP, one of the lead TAs, upon knowing the Test Group 4 in this problem:

<strong>Problem 2 – ADA Removal Game (Programming) </strong>

<strong>Problem Description</strong>

Consider an array <em>A </em>containing <em>N </em>elements. For each operation, you can choose 2 or 3 contiguous elements, whose pairwise greatest common divisor is greater than 1, and remove them from the array. After removal, the remaining parts of the array are concatenated. Meanwhile, you earn points by doing this operation, and the point is calculated by adding up the greatest common divisor of each pair of adjacent elements you removed.

Formally, consider an array <em>A </em>of length <em>N</em>, you can choose two integers <em>i,k </em>such that 1 ≤ <em>i </em>≤ <em>i</em>+<em>k</em>−1 ≤

<em>N,k </em>= {2<em>,</em>3} where gcd(<em>A<sub>x</sub>,A<sub>y</sub></em>) <em>&gt; </em>1<em>,</em>∀<em>i </em>≤ <em>x </em>≤ <em>y </em>≤ <em>i</em>+<em>k</em>−1. Remove <em>A<sub>i</sub>,…,A<sub>i</sub></em><sub>+<em>k</em>−1 </sub>from the array and

<em>i</em>+<em>k</em>−2

get ) points. After the operation, the new array becomes <em>A</em><sub>1</sub><em>,…,A<sub>i</sub></em><sub>−1</sub><em>,A<sub>i</sub></em><sub>+<em>k</em></sub><em>,…,A<sub>N</sub></em>

of length <em>N </em>− <em>k</em>.

You can perform the above operation multiple times until the array is empty. Please find the maximum total points you can receive to eliminate the entire array, and determine whether it is possible to do so.

For example, array [2<em>,</em>3<em>,</em>12<em>,</em>6<em>,</em>4] can be totally eliminated by removing (3<em>,</em>12<em>,</em>6) and (2<em>,</em>4) in order, which gets 11 points. Or, it can also be removed by (3<em>,</em>12) and (2<em>,</em>6<em>,</em>4), which gets 7 points. There is no other way to remove the entire array. Hence, the answer should be the greater one 11.

<strong>Input</strong>

The first line contains an integer indicating <em>N</em>, where 2 ≤ <em>N </em>≤ 500.

The second line contains <em>N </em>space-separated positive integers <em>a<sub>i</sub></em>, where 2 ≤ <em>a<sub>i </sub></em>≤ 10<sup>9</sup>.

<table width="499">

 <tbody>

  <tr>

   <td width="202"><strong>Test Group 0 (0 %)</strong>•   Sample Input<strong>Test Group 1 (10 %)</strong>•   <em>N </em>≤ 10</td>

   <td width="297"><strong>Test Group 3 (30 %)</strong>•   <em>N </em>≤ 100<strong>Test Group 4 (40 %)</strong>•   No other constraints.</td>

  </tr>

 </tbody>

</table>

<strong>Test Group 2 (20 %)</strong>

<ul>

 <li>2|<em>a<sub>i</sub>,</em>∀<em>i</em></li>

</ul>

<strong>Output</strong>

Please output an integer indicating the maximum points. If it is impossible to eliminate the entire array, output −1.

<table width="463">

 <tbody>

  <tr>

   <td width="328"><strong>Sample Input 1</strong>5</td>

   <td width="135"><strong>Sample Output 1</strong>11</td>

  </tr>

 </tbody>

</table>

2 3 12 6 4

<strong>Sample Input 2                                                        Sample Output 2</strong>

5                                                                                23

10 9 3 10 10

<strong>Sample Input 3                                                        Sample Output 3</strong>

6                                                                                13

2 3 6 12 6 4

<strong>Sample Input 4                                                        Sample Output 4</strong>

5                                                                                -1

2 3 8 6 4

<strong>Problem 3 – IOICamp (Programming) </strong>

<strong>Problem Description</strong>

IOICamp is a competitive programming training camp held by NTU CSIE students. Xiao Feng, an IOICamp staff, is full of enthusiasm to dedicate himself to making it better.

One day, Baluteshih, the general coordinator of IOICamp, assigned <em>N </em>tasks to Xiao Feng. Concretely, the <em>i</em><sup>th </sup>task consists of <em>x<sub>i </sub></em>units of work. Each unit of work costs one day for Xiao Feng to complete. Besides, Xiao Feng can not do two different tasks in one day simultaneously. Because of Baluteshih’s requirements, Xiao Feng can only work on the <em>i</em><sup>th </sup>task between <em>s<sub>i</sub></em><sup>th </sup>day and <em>e<sub>i</sub></em><sup>th </sup>day

(inclusive).

To encourage Xiao Feng to finish as much work as possible, Baluteshih gives him some benefits. For the <em>i</em><sup>th </sup>task, if Xiao Feng completes <em>y<sub>i </sub></em>units of work, he will get <em>p<sub>i </sub></em>· <em>y<sub>i </sub></em>bonus from Baluteshih. Note that Xiao Feng can still get the bonus from Baluteshih even if he didn’t finish all units of work in the one task. Please help Xiao Feng to calculate the maximum bonus he could receive from his kindly boss, Baluteshih :).

<strong>Input</strong>

The first line of the input contains only one integer <em>N</em>, denoting the number of tasks assigned to Xiao Feng.

In the following <em>N </em>lines, the <em>i</em><sup>th </sup>line contains four integers <em>s<sub>i</sub>,e<sub>i</sub>,x<sub>i</sub>,p<sub>i</sub></em>, describing the information of the <em>i</em><sup>th </sup>task.

<strong>constraints</strong>

<ul>

 <li>1 ≤ <em>N </em>≤ 3000.</li>

 <li>1 ≤ <em>s<sub>i </sub></em>≤ <em>e<sub>i </sub></em>≤ 10<sup>9</sup>.</li>

 <li>1 ≤ <em>x<sub>i </sub></em>≤ <em>e<sub>i </sub></em>− <em>s<sub>i </sub></em>+ 1.</li>

 <li>1 ≤ <em>p<sub>i </sub></em>≤ 10<sup>9</sup>.</li>

</ul>

<strong>Test Group 0 (0 %)                                                                               Test Group 3 (15 %)</strong>

<ul>

 <li>Sample Input. <em>s</em><sub>1 </sub>≤ <em>s</em><sub>2 </sub>≤ <em>… </em>≤ <em>s<sub>N</sub></em>.</li>

 <li><em>e</em><sub>1 </sub>≤ <em>e</em><sub>2 </sub>≤ <em>… </em>≤ <em>e<sub>N</sub></em>.</li>

</ul>

<strong>Test Group 1 (15 %)                                                                                        </strong>• <em>x</em><em>i </em>= <em>e</em><em>i </em>− <em>s</em><em>i </em>+ 1<em>, </em>∀1 ≤ <em>i </em>≤ <em>N</em>.

<ul>

 <li><em>s</em>1 ≤ <em>s</em>2 ≤ <em>… </em>≤ <em>s</em><em>N</em>. <strong>Test Group 4 (30 %)</strong></li>

 <li><em>e</em><sub>1 </sub>≤ <em>e</em><sub>2 </sub>≤ <em>… </em>≤ <em>e<sub>N</sub></em>.</li>

 <li><em>p<sub>i </sub></em>= 1<em>, </em>∀1 ≤ <em>i </em>≤ <em>N</em>. No other constraints.</li>

</ul>

<strong>Test Group 2 (40 %)</strong>

<ul>

 <li><em>p<sub>i </sub></em>= 1<em>, </em>∀1 ≤ <em>i </em>≤ <em>N</em>.</li>

</ul>

<strong>Output</strong>

Print one integer denoting the maximum bonus Xiao Feng could receive if he arranges the work optimally.

<strong>Sample Input 1                                                        Sample Output 1</strong>

3                                                                                4

<h1><a name="_Toc22744"></a>1 3 2 1</h1>

<ul>

 <li>5 1 1</li>

 <li>4 1 1</li>

</ul>

<strong>Sample Input 2                                                        Sample Output 2</strong>

<ul>

 <li>55</li>

 <li>7 2 6</li>

</ul>

1 10 3 6

6 8 2 8

3 8 1 9

1 9 7 2

<strong>Sample Input 3                                                        Sample Output 3</strong>

5                                                                                67

9 10 1 5

5 15 6 7

4 6 2 8

1 6 1 3

3 9 1 1

<strong>Sample Input 4                                                        Sample Output 4</strong>

10                                                                               741483180481768

317828572 952962709 511194031 474210

139065667 594136128 184836056 727043

145449199 856665845 135232964 221941

185367317 719253355 508496356 303732

286924029 536237215 174723858 743784

448407424 788782769 294918233 970051

128701901 369779350 133590454 996886

268148730 724234276 442825804 255091

658359136 999211180 190588357 715619

114934339 328552693 120729904 373197

<strong>Hint</strong>

<ol>

 <li>It might be useful to solve <strong>Test Group 2 </strong>before solving the rest of the problem. If you encounter some difficulties, please try to solve it first.</li>

 <li>It is recommended to use C++ Standard Template Library (STL) data structures, such as std::stack, std::queue, std::priority queue, std::list, std::vector, and std::set. They can reduce your coding complexity.</li>

</ol>

<strong>Problem 4 – Restricted Candies (Programming) </strong>

<strong>Problem Description</strong>

<em>The definition of an alternating sequence is slightly different from that of in Homework 1.</em>

Baluteshih brings <em>N </em>candies to his friend, Waynetu. Those candies are lined on the table. Each candy has its own sweetness indicated by an integer. The sweetness of the candies from left to right are <em>a</em><sub>1</sub>, <em>a</em><sub>2</sub>, <em>…</em>, <em>a<sub>N</sub></em>, respectively.

Baluteshih assigns Waynetu an interesting mission. He asks Waynetu to remove some candies from the table, so that the remaining candies on the table are <em>alternating</em>. Formally, we say that a sequence of candies with sweetness <em>b</em><sub>1</sub>, <em>b</em><sub>2</sub>, <em>…</em>, <em>b<sub>k </sub></em>is <em>alternating </em>if <em>b<sub>i </sub>×b<sub>i</sub></em><strong><sub>+1 </sub></strong><em>&lt; </em><strong>0 </strong>holds for all 1 ≤ <em>i &lt; k</em>.

With the aforementioned rule, Waynetu hopes to maximize the sum of the sweetness of the candies on the table.

However, Ltf0501 comes and interrupts the mission. Because he wants to make this mission more interesting, he gives Waynetu an additional restriction, that is, <strong>Waynetu needs to leave exactly </strong><em>k </em><strong>candies on the table</strong>. Moreover, for each <em>k </em>between 1 to <em>N</em>, Waynetu needs to determine whether it is possible to leave exactly <em>k </em>candies on the table; if so, Waynetu also need to maximize the sum of the sweetness for that <em>k </em>value.

Please help Waynetu find the maximum possible sum of exactly <em>k </em>remaining candies’ sweetness for each <em>k </em>between 1 to <em>N</em>.

<strong>Input</strong>

The first line contains two integers <em>T</em>, representing the number of test cases, and <em>flag </em>(<em>flag </em>∈ {0<em>,</em>1}), which will be described in the output section.

Each test case includes two lines: the first line contains an integer <em>N </em>(1 ≤ <em>N </em>≤ 10<sup>5</sup>), and the second line contains <em>N </em>integers <em>a</em><sub>1</sub>, <em>a</em><sub>2</sub>, <em>…</em>, <em>a<sub>N </sub></em>(|<em>a<sub>i</sub></em>| ≤ 10<sup>9</sup><em>,</em><em>a<sub>i </sub>6</em><strong>= 0</strong>).

It is guaranteed that the sum of <em>N </em>within the same input file does not exceed 10<sup>5</sup>.

<strong>Test Group 0 (0 %) Test Group 2 (20 %) </strong>• Sample Input.       • P<em>N </em>≤ 1000.

<strong>Test Group 3 (30 %)</strong>

<ul>

 <li><em>flag </em>= 1, <em>a</em><sub>1 </sub><em>&gt; </em>0 and <em>a<sub>N </sub>&gt; </em></li>

</ul>

<strong>Test Group 1 (20 %)</strong>

<strong>Test Group 4 (30 %)</strong>

<ul>

 <li><em>flag </em>= 1, <em>a</em><sub>1 </sub><em>&gt; </em>0 and <em>a<sub>N </sub>&gt; </em></li>

 <li><sup>P</sup><em>N </em>≤ 1000. No additional constraints.</li>

</ul>

<strong>Output</strong>

For each test case, please print <em>N </em>integers in a line, separated by spaces. The <em>i</em><sup>th </sup>number represents the maximum possible sum of the sweetness when Waynetu leaves exactly <em>i </em>candies on the table. If it is impossible to leave exactly <em>i </em>candies on the table, just output 0 for the <em>i</em><sup>th </sup>number.

<strong>If </strong><em>flag </em>= 1<strong>, then you can get Accepted when you have at least</strong><strong> correct answers for each test cases.</strong>

<strong>Sample Input 1                                                        Sample Output 1</strong>

1 0                                                                                6 5 8 2 5

5

3 -1 6 -7 4

<strong>Sample Input 2                                                        Sample Output 2</strong>

<ul>

 <li>0 3 0 0</li>

 <li>3 1 2 -2</li>

</ul>

1 2 3

4

1 -2 3 -4

<strong>Sample Input 3                                                        Sample Output 3</strong>

3 1                                                                             0

1                                                                                 5 0 0

1                                                                                  0 0 0 0

3

5 -1 1

4

1 2 3 4

<strong>Hint</strong>

<ol>

 <li>Since each input includes several independent test cases, please carefully clear all results of the current test case before dealing with the next one.</li>

 <li>In Sample Output 3, you will get Wrong Answer if <em>flag </em>= 0. The Sample Output is just a reminder for the special scoring method.</li>

 <li>It is recommended to use C++ Standard Template Library (STL) data structures, such as std::stack, std::queue, std::priority queue, std::list, std::vector, and std::set. They can reduce your coding complexity.</li>

</ol>

<strong>Problem 5 – Toyz’s Dog (Hand-Written) </strong>

You, Asiagodtone, as known as Toyz’s dog, notices that someone smelled strange, so you decide to trace him. With your big fat nose, you keep tracking that strange smell. After a long trip, you finally arrive at a smoky place. There is a castle surrounded by a moat, and the only path to get into the castle consists of <em>N </em>−1 floating stones in front of the gate. Each stone will sink to the deep when you step on it. You have to choose some stones as a route so that you can go into the castle and then catch the odd-smelling guy. When leaving, you have to go through all the remaining stones to prevent the enemies in the castle from chasing you. That is, you could only step on each stone once and you should let all of them sink to the bottom after leaving the castle.

<strong>Subproblem (a)</strong>

Assuming that the initial place is <em>S</em><sub>0 </sub>and the castle is located at <em>S<sub>N</sub></em>. The <em>N</em>−1 stones are numbered as <em>S</em><sub>1 </sub>to <em>S<sub>N</sub></em><sub>−1</sub>. When you jump from <em>S<sub>a </sub></em>to <em>S<sub>b</sub></em>, you spend <em>E</em>(<em>a,b</em>) energy. It does <strong>NOT </strong>guarantee that <em>E</em>(<em>a,b</em>) ≤ <em>E</em>(<em>a,c</em>) + <em>E</em>(<em>c,b</em>). Note that you are too fat to turn around your body on the stone. For example, <em>N </em>= 3, your possible path can be:

{<em>S</em><sub>0 </sub>→− <em>S</em><sub>1 </sub>→− <em>S</em><sub>2 </sub>→− <em>S</em><sub>3 </sub>→− <em>S</em><sub>0</sub>}

{<em>S</em><sub>0 </sub>→− <em>S</em><sub>1 </sub>→− <em>S</em><sub>3 </sub>→− <em>S</em><sub>2 </sub>→− <em>S</em><sub>0</sub>}

{<em>S</em><sub>0 </sub>→− <em>S</em><sub>2 </sub>→− <em>S</em><sub>3 </sub>→− <em>S</em><sub>1 </sub>→− <em>S</em><sub>0</sub>}

{<em>S</em><sub>0 </sub>→− <em>S</em><sub>3 </sub>→− <em>S</em><sub>2 </sub>→− <em>S</em><sub>1 </sub>→− <em>S</em><sub>0</sub>}<em>.</em>

Now, you want to design a dynamic programming algorithm to find the smallest cost of the entire trip in <em>O</em>(<em>N</em><sup>2</sup>) time complexity. Note that your should let <em>dp</em>(<em>i,j</em>) as the minimal cost of the trip, where your last point on the way you go is <em>S<sub>i </sub></em>and your first point on the way you left is <em>S<sub>j </sub></em>and then minus <em>E</em>(<em>i,N</em>)+<em>E</em>(<em>N,j</em>). Under <em>dp</em>(<em>i,j</em>) state, you should already choose <em>S</em><sub>0 </sub>to <em>S<sub>max</sub></em><sub>(<em>i,j</em>) </sub>to your path no matter the stone is on the way go or left.

<ul>

 <li>(6%) Please recursively define <em>dp</em>(<em>i,j</em>) and prove your correctness and time complexity.</li>

 <li>(6%) With the recursive function you defined in question (1), please solve the problem in <em>O</em>(<em>N</em>) space complexity.</li>

 <li>(6%) Please get the optimal path in the same space complexity as question (2).</li>

</ul>

<strong>Subproblem (b)</strong>

After the capture, you surprisingly find out that the man is your master, Toyz. However, you still send him to the jail for the justice. Unfortunately, his friend, R-code, helps Toyz escape from the jail and then flee back to his castle. This time, he set a smoke bomb at each stone on the way to the castle. Whenever you stand on a stone <em>S<sub>n</sub></em>, the bomb can be triggered and causes <em>D<sub>n </sub></em>damage on you. Luckily, you find a switch that can turn off all the bomb trap in the castle, so you will be safe when leaving the castle.

Assuming that you have initial Health Points <em>H</em>, when you stand on <em>S<sub>n </sub></em>on the way to castle, your Health Points would be reduced by <em>D<sub>n</sub></em>. Under this additional constraint, please design a dynamic programming algorithm to find the smallest cost of the entire trip, as in the subproblem (a), while keeping your Health Points greater than zero.

<ul>

 <li>(6%) Please modify your definition of dp function to solve the problem in <em>O</em>(<em>HN</em><sup>2</sup>) time.</li>

 <li>(6%) Please prove the correctness and the time complexity of your definition.</li>

</ul>

<strong>Problem 6 – Howard’s Desiring Order of Courses (Hand-Written) (20</strong>

<strong>points)</strong>

<em>In problem 6, please </em><em>briefly explain your solution in text. </em><em>Do not use pseudo code, or you will receive penalty.</em>

Howard Wang, as known as rap god, started his first semester in the CSIE department last autumn. When he was 18, he set a goal for his college life, “Having a girlfriend.” However, due to COVID-19 pandemic and lack of courage, he is still not familiar with most of his classmates, let alone making any female friend. L.Y.P., who is his best friend and a natural charmer, gave him an advice, “How about enrolling in courses with the maximum number of girls?”. Following the advice, Howard started to arrange his timetable of the upcoming semester. He collected essential information all CSIE courses and marked his preference of them. As Howard’s friend, please help him find the <strong>maximum satisfying value </strong>he can reach by arranging a desiring order of those courses.

Assuming that there are <em>n </em>courses in the CSIE department, which are <em>C</em><sub>1 </sub>to <em>C<sub>n</sub></em>. For each course <em>C<sub>i</sub></em>, Howard marked his preference of the course with <em>P<sub>i</sub></em>. Moreover, the maximum satisfying value is defined as the maximum number for that could be formed by <strong>concatenating some of the course preference values (in digits) in any order</strong>. For example, if there are three courses <em>C</em><sub>1</sub><em>, C</em><sub>2</sub><em>, C</em><sub>3 </sub>in CSIE, which <em>P</em><sub>1 </sub>= 2 <em>and P</em><sub>2 </sub>= 40 <em>and P</em><sub>3 </sub>= 2, the maximum satisfying value will be 4022.

Lastly, there are some assumptions as follows, which are used in the following problems.

<strong>Assumption 1 </strong><em>Preference of the course is always a single digit number, that is </em>∀ 1 ≤ <em>i </em>≤ <em>n</em>, <em>P<sub>i </sub></em>∈ [0<em>, </em>9].

<strong>Assumption 2 </strong><em>Preference of the course is always a small integer, that is </em>∀ 1 ≤ <em>i </em>≤ <em>n</em>, <em>P<sub>i </sub></em>∈ [0<em>, </em>1000]. <strong>Assumption 3 </strong><em>The maximum satisfying value should be a multiple of 3.</em>

Please answer the following problems.

<ul>

 <li>(2%) Given preference value of 6 courses <em>P </em>= [1<em>, </em>0<em>, </em>9<em>, </em>81<em>, </em>4<em>, </em>12], can you find the maximum satisfying value under no assumption and under <strong>Assumption 3</strong>, respectively?</li>

 <li>(2%) Please give a <em>O</em>(<em>n</em>log(<em>n</em>)) algorithm to find the maximum satisfying value under <strong>Assumption 1</strong>.</li>

 <li>(2%) Please give a <em>O</em>(<em>n</em>log(<em>n</em>)) algorithm to find the maximum satisfying value under <strong>Assumption 2</strong>.</li>

 <li>(4%) Please give a <em>O</em>(<em>n</em>) algorithm to find the maximum satisfying value under both <strong>Assumption 1 and 3 </strong>(If you get full points on this problem, you will automatically gain full points of</li>

</ul>

(2).)

<strong>There are still problems on the next page!</strong>

W.H.Y., Howard’s another friend, decided to further help him by his rich experience. “How about considering some courses from the college of management? There are more girls and elites!”, said W.H.Y.. Howard accepted his advice and also collected information of courses in college of management. To balance his daily life, he also collected <em>n </em>courses from college of management, which are <em>E</em><sub>1 </sub>to <em>E<sub>n</sub></em>. Same as the first time, Howard also marked his preference of each course from college of management <em>E<sub>i </sub></em>with a preference value <em>M<sub>i</sub></em>. For easier understanding, there are now <strong>total </strong>2<em>n </em><strong>distinct courses from CSIE and college of management, each has </strong><em>n </em><strong>courses, which are </strong><em>C</em><sub>1 </sub><strong>to </strong><em>C<sub>n </sub></em><strong>and </strong><em>E</em><sub>1 </sub><strong>to </strong><em>E<sub>n</sub></em>, respectively. For those courses in CSIE, each has a preference value <em>P<sub>i</sub></em>; for those in college of management, each has a preference value <em>M<sub>i</sub></em>. Same as the first part, you’re also asked to find the <strong>maximum satisfying value </strong>he can reach by arranging a desiring order of those courses. In case you forget what is maximum satisfying value, the maximum satisfying value is defined as the maximum number for that could be formed by <strong>concatenating some of the course preference values (in digits) in any order</strong>.

However, the time is limited. Howard can only put <strong>at most total </strong><em>k </em><strong>courses in his desiring order </strong>of courses. Moreover, he performed sorting this time, which <strong>preserves the relative order of the courses from the same department</strong>. That is, in the desiring order, the courses from CSIE should have the same relative order as <em>C</em><sub>1 </sub>to <em>C<sub>n</sub></em>, and the courses from management should have the same relative order as <em>E</em><sub>1 </sub>to <em>E<sub>n</sub></em>. To simplify the problem, the preference of courses is always a <strong>single digit number</strong>, that is ∀ 1 ≤ <em>i </em>≤ <em>n</em>, {<em>P<sub>i</sub>, M<sub>i</sub></em>} ∈ [0<em>, </em>9].

For example, if <em>n </em>= 3, <em>k </em>= 4, the preference value of courses are <em>P<sub>i </sub></em>= [3<em>, </em>6<em>, </em>4], <em>M<sub>i </sub></em>= [8<em>, </em>5<em>, </em>7], the maximum satisfying value will be 8764.

<ul>

 <li>(2%) Assuming <em>n </em>= 5, <em>k </em>= 5, given preference value of courses <em>P<sub>i </sub></em>= [3<em>, </em>4<em>, </em>6<em>, </em>5<em>, </em>0], <em>M<sub>i </sub></em>= [9<em>, </em>0<em>, </em>5<em>, </em>8<em>, </em>3], can you find the maximum satisfying value?</li>

 <li>(8%) Please give a <em>O</em>(<em>kn</em><sup>2</sup>) algorithm to find the maximum satisfying value given <em>P<sub>i </sub></em>and <em>M<sub>i</sub></em>.</li>

</ul>