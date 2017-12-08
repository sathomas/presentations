### The Enemy of My Enemy is ?
##### Structural Balance in Polymicrobial Networks

---

#### Structural Balance

![](https://rawgit.com/sathomas/presentations/sbalance/assets/alliances.svg)

Data from [[Strogatz2010](https://opinionator.blogs.nytimes.com/2010/02/14/the-enemy-of-my-enemy/)]

+++

#### Structural Balance

`$$
\sigma (a \to b) = \left\{ {\begin{array}{*{20}{r}}
{ + 1}\\
{ - 1}\\
0
\end{array}}~~{\begin{array}{*{20}{r}}
{if~a~promotes~b\\
{ - 1}\\
0
\end{array}}\right.
$$`

`$$\Pi (a,b,c) = \sigma (a \to b) \cdot \sigma (b \to c) \cdot \sigma (c \to a)$$`

`$$\Sigma (a,b,c) = \sigma (a \to b) + \sigma (b \to c) + \sigma (c \to a)$$`

---?image=https://rawgit.com/sathomas/presentations/sbalance/assets/bacteria-808158_1920.jpg

#### Polymicrobial Networks

- Species can promote the growth of other species (positive interaction)
- Species can inhibit the growth of other species (negative interaction)

Image from [[Pixabay](https://pixabay.com/en/bacteria-electron-microscope-stained-808158/)]

+++

#### Community Dynamics

`$${\textstyle{{d{x_i}} \over {dt}}} = {r_i}{x_i}\left( {1 - \sum\limits_{j = 1}^N {{\alpha _{ij}}{x_j}} } \right)$$`

---

#### Available Data

![](https://rawgit.com/sathomas/presentations/sbalance/assets/o_graphs.svg)

+++

#### Data Characteristics

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


---

#### Strong Structural Balance

![](https://rawgit.com/sathomas/presentations/sbalance/assets/o_cistrong.svg)

+++

#### Cycle Index

`$$ci = \frac{{\left\| {\{ \;(a,b,c) \in G\;| \;\Pi (a,b,c) = 1\;\} } \right\|}}{{\left\| {\{ \;(a,b,c) \in G\;|\;a \to b \to c \to a\;\} } \right\|}}$$`


---

#### Weak Structural Balance

![](https://rawgit.com/sathomas/presentations/sbalance/assets/o_ciweak.svg)

+++

#### Weak Cycle Index

`$$ci _{w}= \frac{{\left\| {\{ \; \forall \;(a,b,c) \;| \;\Pi (a,b,c) = 1\; \cup \;\Sigma (a,b,c) \ne 1\;\} } \right\|}}{{\left\| {\{ \;(a,b,c) \in G\;|\;a \to b \to c \to a\;\} } \right\|}}$$`

---

#### Cycle Lengths

![](https://rawgit.com/sathomas/presentations/sbalance/assets/o_cilength.svg)

---

#### Signed Clustering Coefficient

![](https://rawgit.com/sathomas/presentations/sbalance/assets/o_c_s.svg)

`$${C_s}(G) = \frac{{\sum\nolimits_{(a,b,c) \in G\;} {\Pi (a,b,c)} }}{{\lVert {\{ \;(a,b,c) \in G\;|\;a \to b \to c\;\} } \rVert}}$$`

---

#### Signed Clustering Coefficient

| Data set       |   C  |   Cs  |   S   |
| :------------- | ---: | ----: | ----: |
| [Brown]        | 0.93 |  0.00 |  0.00 |
| [Friedman2017] | 0.87 | -0.04 | -0.04 |
| [Lo2017]       | 0.08 | -0.05 | -0.67 |
| [Xiao2017]     | 0.93 | +0.27 | +0.29 |

---

#### Discussion

- Is balance theory valid for polymicrobial networks?
- Is network inference data for polymicrobial networks valid?

