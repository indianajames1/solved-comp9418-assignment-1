Download Link: https://assignmentchef.com/product/solved-comp9418-assignment-1
<br>
<h1>1             [100 Marks] Inference in Directed Graphical Models</h1>

Consider the Bayesian network in fig. 1 and a corresponding valid Junction Tree in fig. 2.

Figure 1: Bayesian network.

This graphical model corresponds to a simplified instance of the model proposed by Williams et al. (2006) for condition monitoring in a neonatal intensive care unit. You can read more about the problem in the reference provided but tracking this and other references will not help you solve this assignment. The network is composed of <em>true states F<sub>i</sub></em>, <em>artifactual states M<sub>i </sub></em>and <em>observations T<sub>i </sub></em>for <em>i </em>= 0<em>,</em>1<em>,</em>2. The main task in these types of models is, given observations COMP9418, UNSW Sydney Advanced Topics in Statistical Machine Learning, 18s2

Figure 2: A valid Junction Tree corresponding to the Bayesian network given in fig. 1.

at time <em>i</em>, to infer the configuration of the underlying true state and how much it has been obscured by artifacts. The variables <em>T<sub>i </sub></em>are discrete with states {low<em>,</em>medium<em>,</em>high} and <em>F<sub>i</sub>,M<sub>i </sub></em>are binary variables taking on values in {true<em>,</em>false}.

You are also given the following conditional probability tables (cpts):

<table width="501">

 <tbody>

  <tr>

   <td width="281"><em>P</em>(<em>F</em><sub>0 </sub>= true) = 0<em>.</em>25</td>

   <td width="220"><em>P</em>(<em>M</em><sub>0 </sub>= true) = 0<em>.</em>12</td>

  </tr>

  <tr>

   <td width="281"><em>P</em>(<em>F</em><sub>1 </sub>= true|<em>F</em><sub>0 </sub>= false) = 0<em>.</em>1</td>

   <td width="220"><em>P</em>(<em>M</em><sub>1 </sub>= true|<em>M</em><sub>0 </sub>= false) = 0<em>.</em>05</td>

  </tr>

  <tr>

   <td width="281"><em>P</em>(<em>F</em><sub>1 </sub>= true|<em>F</em><sub>0 </sub>= true) = 0<em>.</em>9</td>

   <td width="220"><em>P</em>(<em>M</em><sub>1 </sub>= true|<em>M</em><sub>0 </sub>= true) = 0<em>.</em>95</td>

  </tr>

  <tr>

   <td width="281"><em>P</em>(<em>F</em><sub>2 </sub>= true|<em>F</em><sub>1 </sub>= false) = 0<em>.</em>33</td>

   <td width="220"><em>P</em>(<em>M</em><sub>2 </sub>= true|<em>M</em><sub>1 </sub>= false) = 0<em>.</em>25</td>

  </tr>

  <tr>

   <td width="281"><em>P</em>(<em>F</em><sub>2 </sub>= true|<em>F</em><sub>1 </sub>= true) = 0<em>.</em>2</td>

   <td width="220"><em>P</em>(<em>M</em><sub>2 </sub>= true|<em>M</em><sub>1 </sub>= true) = 0<em>.</em>68</td>

  </tr>

 </tbody>

</table>

Table 1: cpt for <em>P</em>(<em>T<sub>i </sub></em>= <em>t<sub>i</sub></em>|<em>M<sub>i </sub></em>= <em>m<sub>i</sub>,F<sub>i </sub></em>= <em>f<sub>i</sub></em>) for <em>i </em>= 0<em>,</em>1<em>,</em>2.

In the questions below, unless otherwise stated explicitly, you must <strong>show all your working</strong>. Omission of details or derivations may yield a reduction in the corresponding marks.

<ol>

 <li>[10 marks] Write down the corresponding joint distribution <em>P</em>(<em>M</em><sub>0</sub><em>,M</em><sub>1</sub><em>,M</em><sub>2</sub><em>,F</em><sub>0</sub><em>,F</em><sub>1</sub><em>,F</em><sub>2</sub><em>,T</em><sub>0</sub><em>,T</em><sub>1</sub><em>,T</em><sub>2</sub>).</li>

 <li>[20 marks] Calculate <em>P</em>(<em>M</em><sub>0</sub>|<em>T</em><sub>1 </sub>= low) efficiently using Variable (i.e. Bucket) Elimination.</li>

 <li>[20 marks] Using the Junction Tree provided in 2 along with the message-passage mechanism in the Junction Tree Algorithm (jta), calculate <em>P</em>(<em>F</em><sub>1</sub>|<em>T</em><sub>0 </sub>= low<em>,T</em><sub>1 </sub>= medium).</li>

</ol>

COMP9418, UNSW Sydney                       Advanced Topics in Statistical Machine Learning, 18s2

<ol start="2">

 <li>[20 marks] Provide an elimination order of nodes in the Bayesian network such that the created cliques give rise to the the Junction Tree of 2. Note that you need to moralise the graph first.</li>

 <li>[15 marks] Calculate <em>P</em>(<em>M</em><sub>0</sub><em>,M</em><sub>2</sub>|<em>T</em><sub>1 </sub>= medium) using the jta.</li>

 <li>[15 marks] Suppose edges <em>T</em><sub>0 </sub>→ <em>T</em><sub>1 </sub>and <em>T</em><sub>1 </sub>→ <em>T</em><sub>2 </sub>are added to the original Bayesian network. Construct a valid Junction Tree corresponding to this new Bayesian network.</li>

</ol>

<h1>References</h1>

Williams, C., Quinn, J., and McIntosh, N. (2006). Factorial switching Kalman filters for condition monitoring in neonatal intensive care. In <em>Advances in Neural Information Processing Systems</em>, pages 1513–1520.