# Isomorphism

Prove that if two graphs $A$ and $B$ have the same number of nodes and are
completely connected, they must be isomorphic. I have started with the formal
definition of isomorphism below. Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$G_1=(V_1 , E_1)$ is isomorphic to $G_2 = (V_2, E_2)$ if there exists a
one-to-one and onto function (bijection) $f: V_1 \rightarrow V_2$ such that $(u,v)
\in E_1$ iff $(f(u),f(v)) \in E_2$.

## Answer

We know that two graphs must have the same number of nodes to be isomorphic, so having the same number of nodes is a necessary condition for isomorphism. Now, since we know that isomorphic graphs are defined by $G_1=(V_1 , E_1)$ is isomorphic to $G_2 = (V_2, E_2)$ if there exists a one-to-one and onto function (bijection) $f: V_1 \rightarrow V_2$ such that $(u,v)\in E_1$ iff $(f(u),f(v)) \in E_2$. For each of the possible graphs $A$ and $B$, this must be true.

For the smallest relevant example of this problem, we can look at a completely connected set of graphs with three nodes each. This makes two triangles. For $A = (V_A , E_A)$, $V_A = (1,2,3)$ and $E_A = [(1,2),(1,3),(2,3)]$ We then can compare to an isomorphic graph in $B = (V_B , E_B)$, $V_B = (1,3,2)$, and $E_B$ = [(1,3),(1,2),(2,3)]$ which can be found by swapping  3 and 2, this one is obviously isomorphic, but is the base case for our pattern. For this, there are $V-i$ edges connected to each node, where i is the number of nodes checked, starting with one. This pattern will continue for each other possibility. The first node has $3-1 = 2$ edges connected to it, the second node we check has $3-2 = 1$ edges connected to it. This accounts for all edges, and shows that the two graphs are isomorphic, when comparing the edges, since all edges will appear in this pattern. 1,2 is guaranteed, as are 1,3 and 2,3. This will hold true for the others. This pattern exists because each node has $V - 1$ edges, but one edge is always pre-accounted for when moving between two nodes, for example, (1,2) is already accounted for when checking edges that are connected to node 2.

To show another case, let's look at a completely connected set of graphs with four nodes each. For $A = (V_A , E_A)$, $V_A = (1,2,3,4)$ and $E_A = [(1,2),(1,3),(1,4),(2,3),(2,4),(3,4)]$ and for $B = (V_B , E_B)$, $V_B = (2,3,1,4)$ and $E_B$ = [(2,3),(2,1),(2,4),(3,1),(3,4),(1,4)]$, or sorted = $E_B = [(2,3),(1,2),(2,4),(1,3),(3,4),(1,4)]$. This shows that for adding another completely connected node leads to the same result. Using the pattern established before, $V - i$ edges per node, where i is the number of nodes already checked and v is the number of nodes, there are 3,2,and 1 edges accounted for by the first three nodes. This pattern continues to hold true. The edges will always be the same, no matter how many ways you swap the nodes.

Another key to seeing this is that no matter which way the nodes are checked, the same edges will still exist. Since every node is connected to every other node, node 1,000,001 could be swapped for node 7 and the edge (7, 1,000,001) would still exist, just be found another way. Regardless of how the vertices are labeled, the edges remain the same. Thus, any two sets of completely connected graphs have to be isomorphic.

### Sources and Plagarism Statement

Referenced my answer for isomorphism nodes. Used basic definition of isomorphism. No other sources were used.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
