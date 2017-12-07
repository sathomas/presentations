### The Enemy of My Enemy is ?
##### Structural Balance in Polymicrobial Networks

---

#### Structural Balance

![](https://rawgit.com/sathomas/presentations/sbalance/assets/alliances.svg)

Data from [[Strogatz2010](https://opinionator.blogs.nytimes.com/2010/02/14/the-enemy-of-my-enemy/)]

+++

#### Structural Balance

`$$\sigma (a \to b) = \left\\{ {\begin{array}{*{20}{r}} { + 1} { - 1} 0 \end{array}} ~~\begin{array}{*{20}{l}} {{\rm{if~}}a{\rm{~promotes~}}b} {{\rm{if~}}a{\rm{~inhibits~}}b} {{\rm{otherwise}}} \end{array}\right.$$`

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

<table class="table1"><thead><tr><th style="text-align:left;">Data set</th><th style="text-align:right;">Nodes</th><th style="text-align:right;">Edges</th><th style="text-align:right;">mean(k)</th><th style="text-align:right;">Frac(+)</th><th style="text-align:left;">Summary</th></tr></thead><tbody><tr><td style="text-align:left;">[Brown]</td><td style="text-align:right;">10</td><td style="text-align:right;">88</td><td style="text-align:right;">8.8</td><td style="text-align:right;">0.45</td><td style="text-align:left;">Cystic Fibrosis lung microbiome</td></tr><tr><td style="text-align:left;">[Bucci2016] (1)</td><td style="text-align:right;">14</td><td style="text-align:right;">23</td><td style="text-align:right;">1.6</td><td style="text-align:right;">0.65</td><td style="text-align:left;">Clostridium difficile infection</td></tr><tr><td style="text-align:left;">[Bucci2016] (2)</td><td style="text-align:right;">13</td><td style="text-align:right;">24</td><td style="text-align:right;">1.8</td><td style="text-align:right;">0.50</td><td style="text-align:left;">Germ-free mouse colonization</td></tr><tr><td style="text-align:left;">[deVos2017]</td><td style="text-align:right;">4</td><td style="text-align:right;">6</td><td style="text-align:right;">1.5</td><td style="text-align:right;">0.50</td><td style="text-align:left;">Urinary tract infection</td></tr><tr><td style="text-align:left;">[Friedman2017]</td><td style="text-align:right;">8</td><td style="text-align:right;">53</td><td style="text-align:right;">6.6</td><td style="text-align:right;">0.74</td><td style="text-align:left;">Synthetic soil microbiome</td></tr><tr><td style="text-align:left;">[Lo2017]</td><td style="text-align:right;">15</td><td style="text-align:right;">35</td><td style="text-align:right;">2.3</td><td style="text-align:right;">0.40</td><td style="text-align:left;">Human gut microbiome</td></tr><tr><td style="text-align:left;">[Xiao2017]</td><td style="text-align:right;">7</td><td style="text-align:right;">41</td><td style="text-align:right;">5.9</td><td style="text-align:right;">0.68</td><td style="text-align:left;">Synthetic maize root microbiome</td></tr></tbody></table>

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

`$$ci _{weak}= \frac{{\left\| {\{ \;(a,b,c) \in G\;| \;(a \to b \to c \to a)\; \cap \;\Sigma (a,b,c) \ne 1\;\} } \right\|}}{{\left\| {\{ \;(a,b,c) \in G\;|\;a \to b \to c \to a\;\} } \right\|}}$$`

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

