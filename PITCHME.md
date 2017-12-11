### The Enemy of My Enemy is ?
##### Structural Balance in Polymicrobial Networks

---?image=https://rawgit.com/sathomas/presentations/sbalance/assets/bacteria-808158_1920.jpg

#### Polymicrobial Networks

- Species can promote the growth of other species (positive interaction)
- Species can inhibit the growth of other species (negative interaction)
- Generalized Lotka-Volterra model captures interactions as “adjacency matrix.”

`$${\textstyle{{d{x_i}} \over {dt}}} = {r_i}{x_i}\left( {1 - \sum\limits_{j = 1}^N {{\alpha _{ij}}{x_j}} } \right)$$`<!-- .element: style="color:white;font-size:75%;" -->

---

#### Balance Theory

- Directed networks balanced if `$\Pi (a,b,c) = 1$` for all triplets.
- Weakly balanced if `$\Sigma (a,b,c) \ne 1$` for all triplets
- Cycle index for partially connected networks

`$$
\sigma (a \to b) = \left\{ {\begin{array}{*{20}{r}}
{ + 1}\\
{ - 1}\\
0
\end{array}}~~{\begin{array}{*{20}{l}}
{{\rm{if~}}a{\rm{~promotes~}}b}\\
{{\rm{if~}}a{\rm{~inhibits~}}b}\\
{{\rm{otherwise}}}
\end{array}}\right.
$$`<!-- .element: style="font-size:50%;" -->

`$$\Pi (a,b,c) = \sigma (a \to b) \cdot \sigma (b \to c) \cdot \sigma (c \to a)$$`<!-- .element: style="font-size:50%;" -->

`$$\Sigma (a,b,c) = \sigma (a \to b) + \sigma (b \to c) + \sigma (c \to a)$$`<!-- .element: style="font-size:50%;" -->

`$$ci = \frac{{\left\| {\{ \;(a,b,c) \in G\;| \;\Pi (a,b,c) = 1\;\} } \right\|}}{{\left\| {\{ \;(a,b,c) \in G\;|\;a \to b \to c \to a\;\} } \right\|}}$$`<!-- .element: style="font-size:50%;" -->

`$$ci _{weak}= \frac{{\left\| {\{ \;(a,b,c) \in G\;| \;(a \to b \to c \to a)\; \cap \;\Sigma (a,b,c) \ne 1\;\} } \right\|}}{{\left\| {\{ \;(a,b,c) \in G\;|\;a \to b \to c \to a\;\} } \right\|}}$$`<!-- .element: style="font-size:50%;" -->

+++

#### Structural Balance in the Real World

![](https://rawgit.com/sathomas/presentations/sbalance/assets/alliances.svg)

---

#### Available Data Sets

| Data set        | Nodes | Edges | mean(k) | Frac(+) | Summary                         |
| :-------------- | ----: | ----: | ------: | ------: | :------------------------------ |
| [Brown]         |    10 |    88 |     8.8 |    0.45 | Cystic Fibrosis lung microbiome |
| [Bucci2016] (1) |    14 |    23 |     1.6 |    0.65 | Clostridium difficile infection |
| [Bucci2016] (2) |    13 |    24 |     1.8 |    0.50 | Germ-free mouse colonization    |
| [deVos2017]     |     4 |     6 |     1.5 |    0.50 | Urinary tract infection         |
| [Friedman2017]  |     8 |    53 |     6.6 |    0.74 | Synthetic soil microbiome       |
| [Lo2017]        |    15 |    35 |     2.3 |    0.40 | Human gut microbiome            |
| [Xiao2017]      |     7 |    41 |     5.9 |    0.68 | Synthetic maize root microbiome |
<!-- .element: style="font-size:50%;margin-top:10vh;" -->

+++

#### Resulting Networks

![](https://rawgit.com/sathomas/presentations/sbalance/assets/o_graphs.svg)


---

#### Cycle Index (Strong)

![](https://rawgit.com/sathomas/presentations/sbalance/assets/o_cistrong.svg)


---

#### Cycle Index (Weak)

![](https://rawgit.com/sathomas/presentations/sbalance/assets/o_ciweak.svg)

---

#### Arbitrary Cycle Lengths

![](https://rawgit.com/sathomas/presentations/sbalance/assets/o_cilength.svg)

[Xiao2017] shows diminishing strength of structural balance as cycle length increases.<!-- .element: style="font-size:75%;" -->

---

#### Signed Clustering Coefficient

![](https://rawgit.com/sathomas/presentations/sbalance/assets/o_c_s.svg)

`$$
\begin{array}{*{20}{l}}
{C(G) = \frac{{\left\| {\{ \;(a,b,c) \in G\;|\;a \to b \to c \to a\;\} } \right\|}}{{\left\| {\{ \;(a,b,c) \in G\;|\;a \to b \to c\;\} } \right\|}}}\\
{{C_s}(G) = \frac{{\sum\nolimits_{(a,b,c) \in G\;} {\Pi (a,b,c)} }}{{\lVert {\{ \;(a,b,c) \in G\;|\;a \to b \to c\;\} } \rVert}}}\\
{S(G) = \frac{{{C_s}(G)}}{{C(G)}}}
\end{array}
$$`<!-- .element: style="font-size:50%;" -->

---

#### Signed Clustering Coefficient

| Data set       |   C  |   Cs  |   S   |
| :------------- | ---: | ----: | ----: |
| [Brown]        | 0.93 |  0.00 |  0.00 |
| [Friedman2017] | 0.87 | -0.04 | -0.04 |
| [Lo2017]       | 0.08 | -0.05 | -0.67 |
| [Xiao2017]     | 0.93 | +0.27 | +0.29 |

Relative signed clustering coefficient, S(G), positive for balanced networks [Kunegis2014]<!-- .element: style="font-size:75%;" -->

---

#### Discussion

- No strong evidence of structural balance in polymicrobial networks.
- Is data valid?
     * Current research relies on widely varying approaches for network inference, often incorporating novel mathematical or statistical techniques.
     * Can structural balance be used to validate network inference techniques?
- Is theory valid?
     * In directed networks, the benefits of balance are not reciprocal.
     * Can balance theory be extended to accommodate both fitness costs _and_ benefits of directed interactions.
