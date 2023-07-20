# ML-Unsupervised-Learning-Clustering-AsoociationRuleLearning

Association rule learning is a type of unsupervised learning technique that checks for the dependency of one data item on another data item and maps accordingly so that it can be more profitable. It tries to find some interesting relations or associations among the variables of dataset. It is based on different rules to discover the interesting relations between variables in the database.

The association rule learning is one of the very important concepts of machine learning, and it is employed in Market Basket analysis, Web usage mining, continuous production, etc. Here market basket analysis is a technique used by the various big retailer to discover the associations between items. We can understand it by taking an example of a supermarket, as in a supermarket, all products that are purchased together are put together.

<h2>For example,</h2> if a customer buys bread, he most likely can also buy butter, eggs, or milk, so these products are stored within a shelf or mostly nearby. Consider the below diagram:
<img src = "https://static.javatpoint.com/tutorial/machine-learning/images/association-rule-learning.png">

<h2>Association rule learning can be divided into three types of algorithms:</h2>
<ul>
<li>Apriori</li>
<li>Eclat</li>
<li>F-P Growth Algorithm</li>
</ul>
We will understand these algorithms in later chapters.

<h2>How does Association Rule Learning work?</h2>
Association rule learning works on the concept of If and Else Statement, such as if A then B.
<img src ="https://static.javatpoint.com/tutorial/machine-learning/images/association-rule-learning2.png">
Here the If element is called antecedent, and then statement is called as Consequent. These types of relationships where we can find out some association or relation between two items is known as single cardinality. It is all about creating rules, and if the number of items increases, then cardinality also increases accordingly. So, to measure the associations between thousands of data items, there are several metrics. These metrics are given below:
<ul>
<li>Support</li>
<li>Confidence</li>
<li>Lift</li>
</ul>
Let's understand each of them:

Support
Support is the frequency of A or how frequently an item appears in the dataset. It is defined as the fraction of the transaction T that contains the itemset X. If there are X datasets, then for transactions T, it can be written as:
<img  src ="https://static.javatpoint.com/tutorial/machine-learning/images/association-rule-learning3.png">
<h2>Confidence</h2>
Confidence indicates how often the rule has been found to be true. Or how often the items X and Y occur together in the dataset when the occurrence of X is already given. It is the ratio of the transaction that contains X and Y to the number of records that contain X.
<img src = "https://static.javatpoint.com/tutorial/machine-learning/images/association-rule-learning4.png">
<h2>Lift</h2>
It is the strength of any rule, which can be defined as below formula:
<img src = "https://static.javatpoint.com/tutorial/machine-learning/images/association-rule-learning5.png">

It is the ratio of the observed support measure and expected support if X and Y are independent of each other. It has three possible values:
<ul>
<li>If <h2>Lift= 1:</h2> The probability of occurrence of antecedent and consequent is independent of each other.</li>
<li><h2>Lift>1:</h2> It determines the degree to which the two itemsets are dependent to each other.</li>
<li><h2>Lift<1:</h2> It tells us that one item is a substitute for other items, which means one item has a negative effect on another.</li>
</ul>
<h2>Types of Association Rule Lerning</h2>
Association rule learning can be divided into three algorithms:

<h2>Apriori Algorithm</h2>
This algorithm uses frequent datasets to generate association rules. It is designed to work on the databases that contain transactions. This algorithm uses a breadth-first search and Hash Tree to calculate the itemset efficiently.

It is mainly used for market basket analysis and helps to understand the products that can be bought together. It can also be used in the healthcare field to find drug reactions for patients.

<h2>Eclat Algorithm</h2>
Eclat algorithm stands for Equivalence Class Transformation. This algorithm uses a depth-first search technique to find frequent itemsets in a transaction database. It performs faster execution than Apriori Algorithm.

<h2>F-P Growth Algorithm</h2>
The F-P growth algorithm stands for Frequent Pattern, and it is the improved version of the Apriori Algorithm. It represents the database in the form of a tree structure that is known as a frequent pattern or tree. The purpose of this frequent tree is to extract the most frequent patterns.


<h2>Applications of Association Rule Learning</h2>
=>It has various applications in machine learning and data mining. Below are some popular applications of association rule learning:
<ul>
<li>Market Basket Analysis: It is one of the popular examples and applications of association rule mining. This technique is commonly used by big retailers to determine the association between items.</li>
<li>Medical Diagnosis: With the help of association rules, patients can be cured easily, as it helps in identifying the probability of illness for a particular disease.</li>
<li>Protein Sequence: The association rules help in determining the synthesis of artificial Proteins.</li>
<li>It is also used for the Catalog Design and Loss-leader Analysis and many more other applications.</li>
</ul>
<h2>Apriori Algorithm in Machine Learning</h2>
The Apriori algorithm uses frequent itemsets to generate association rules, and it is designed to work on the databases that contain transactions. With the help of these association rule, it determines how strongly or how weakly two objects are connected. This algorithm uses a breadth-first search and Hash Tree to calculate the itemset associations efficiently. It is the iterative process for finding the frequent itemsets from the large dataset.

This algorithm was given by the R. Agrawal and Srikant in the year 1994. It is mainly used for market basket analysis and helps to find those products that can be bought together. It can also be used in the healthcare field to find drug reactions for patients.

<h2>What is Frequent Itemset?</h2>

Frequent itemsets are those items whose support is greater than the threshold value or user-specified minimum support. It means if A & B are the frequent itemsets together, then individually A and B should also be the frequent itemset.

Suppose there are the two transactions: A= {1,2,3,4,5}, and B= {2,3,7}, in these two transactions, 2 and 3 are the frequent itemsets.

<h2>Note:</h2> To better understand the apriori algorithm, and related term such as support and confidence, it is recommended to understand the association rule learning.
Steps for Apriori Algorithm
Below are the steps for the apriori algorithm:

<p>Below are the steps for the apriori algorithm:</p>
<p><strong>Step-1:</strong> Determine the support of itemsets in the transactional database, and select the minimum support and confidence.</p>
<p><strong>Step-2:</strong> Take all supports in the transaction with higher support value than the minimum or selected support value.</p>
<p><strong>Step-3:</strong> Find all the rules of these subsets that have higher confidence value than the threshold or minimum confidence.</p>
<p><strong>Step-4:</strong> Sort the rules as the decreasing order of lift.</p>

<h2>Apriori Algorithm Working</h2>
We will understand the apriori algorithm using an example and mathematical calculation:
<h2>Example:</h2> Suppose we have the following dataset that has various transactions, and from this dataset, we need to find the frequent itemsets and generate the association rules using the Apriori algorithm:

<h2>Solution:</h2>
<ul class="points">
<li>In the first step, we will create a table that contains support count (The frequency of each itemset individually in the dataset) of each itemset in the given dataset. This table is called the <strong>Candidate set or C1.</strong><br>
<img src="https://static.javatpoint.com/tutorial/machine-learning/images/apriori-algorithm2.png" alt="Apriori Algorithm in Machine Learning" /></li>
<li>Now, we will take out all the itemsets that have the greater support count that the Minimum Support (2). It will give us the table for the <strong>frequent itemset L1.</strong><br>
Since all the itemsets have greater or equal support count than the minimum support, except the E, so E itemset will be removed.<br>
<img src="https://static.javatpoint.com/tutorial/machine-learning/images/apriori-algorithm3.png" alt="Apriori Algorithm in Machine Learning" /></li>
</ul>
<h3 class="h3">Step-2: Candidate Generation C2, and L2:</h3>
<ul class="points">
<li>In this step, we will generate C2 with the help of L1. In C2, we will create the pair of the itemsets of L1 in the form of subsets.</li>
<li>After creating the subsets, we will again find the support count from the main transaction table of datasets, i.e., how many times these pairs have occurred together in the given dataset. So, we will get the below table for C2:<br>
<img src="https://static.javatpoint.com/tutorial/machine-learning/images/apriori-algorithm4.png" alt="Apriori Algorithm in Machine Learning" /></li>
<li>Again, we need to compare the C2 Support count with the minimum support count, and after comparing, the itemset with less support count will be eliminated from the table C2. It will give us the below table for L2<br>
<img src="https://static.javatpoint.com/tutorial/machine-learning/images/apriori-algorithm5.png" alt="Apriori Algorithm in Machine Learning" /></li>
</ul>
<h3 class="h3">Step-3: Candidate generation C3, and L3:</h3>
<ul class="points">
<li>For C3, we will repeat the same two processes, but now we will form the C3 table with subsets of three itemsets together, and will calculate the support count from the dataset. It will give the below table:<br>
<img src="https://static.javatpoint.com/tutorial/machine-learning/images/apriori-algorithm6.png" alt="Apriori Algorithm in Machine Learning" /></li>
<li>Now we will create the L3 table. As we can see from the above C3 table, there is only one combination of itemset that has support count equal to the minimum support count. So, the L3 will have only one combination, i.e., <strong>{A, B, C}.</strong></li>
</ul>
<h3 class="h3">Step-4: Finding the association rules for the subsets:</h3>
<p>To generate the association rules, first, we will create a new table with the possible rules from the occurred combination {A, B.C}. For all the rules, we will calculate the Confidence using formula <strong>sup( A ^B)/A.</strong> After calculating the confidence value for all rules, we will exclude the rules that have less confidence than the minimum threshold(50%).</p>

Consider the below table:
<table class="alt">
<tr>
<th>Rules</th>
<th>Support</th>
<th>Confidence</th>
</tr>
<tr>
<td>A ^B &rarr; C</td>
<td>2</td>
<td>Sup{(A ^B) ^C}/sup(A ^B)= 2/4=0.5=50%</td>
</tr>
<tr>
<td>B^C &rarr; A</td>
<td>2</td>
<td>Sup{(B^C) ^A}/sup(B ^C)= 2/4=0.5=50%</td>
</tr>
<tr>
<td>A^C &rarr; B</td>
<td>2</td>
<td>Sup{(A ^C) ^B}/sup(A ^C)= 2/4=0.5=50%</td>
</tr>
<tr>
<td>C&rarr; A ^B</td>
<td>2</td>
<td>Sup{(C^( A ^B)}/sup(C)= 2/5=0.4=40%</td>
</tr>
<tr>
<td>A&rarr; B^C</td>
<td>2</td>
<td>Sup{(A^( B ^C)}/sup(A)= 2/6=0.33=33.33%</td>
</tr>
<tr>
<td>B&rarr; B^C</td>
<td>2</td>
<td>Sup{(B^( B ^C)}/sup(B)= 2/7=0.28=28%</td>
</tr>
</table>

As the given threshold or minimum confidence is 50%, so the first three rules A ^B → C, B^C → A, and A^C → B can be considered as the strong association rules for the given problem.

<h2>Advantages of Apriori Algorithm</h2>
<ul>
<li>This is easy to understand algorithm</li>
<li>The join and prune steps of the algorithm can be easily implemented on large datasets.</li>
</ul>
<h2>Disadvantages of Apriori Algorithm</h2>
<ul>
<li>The apriori algorithm works slow compared to other algorithms.</li>
<li>The overall performance can be reduced as it scans the database for multiple times.</li>
<li>The time complexity and space complexity of the apriori algorithm is O(2D), which is very high. Here D represents the horizontal width present in the database.</li>
</ul>
