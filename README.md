Download Link: https://assignmentchef.com/product/solved-fe621-homework-3
<br>
<strong>Problem 1 . Finite difference methods.</strong>

<ul>

 <li>Implement the Explicit Finite Difference method to price both European Call and Put options. Please derive the final discretized equation and rearrange them appropriately. Clearly state the steps for carrying out the valuation.</li>

 <li>Implement the Implicit Finite Difference method to price European Call and Put options. Again underline the steps used particularly clearly separate and label as such the tridiagonal system solver.</li>

 <li>Implement the Crank-Nicolson Finite Difference method and price both European Call and Put options. Here derive the final discretized equation and rearrange them appropriately. Clearly state the steps for carrying out the valuation.</li>

 <li>For both the Explicit and Implicit Finite Difference schemes estimate the numbers ∆<em>t</em>, ∆<em>x</em>, and the total number <em>N<sub>j </sub></em>of points on the space grid <em>x </em>needed to obtain a desired error of <em>ε </em>= 0<em>.</em> <em>Hint. </em>Remember the order of convergence for each of the schemes. For each schemes select ∆<em>t</em>, ∆<em>x </em>as well as <em>n </em>and <em>N<sub>j </sub></em>so that the order of convergence is smaller than the desired error. Please note that <em>N<sub>j </sub></em>has to be chosen in such a way so that the range of <em>x </em>values span the entire possible range at <em>T</em>.</li>

 <li>Consider <em>S</em><sub>0 </sub>= 100<em>,K </em>= 100, <em>T </em>= 1 year, <em>σ </em>= 20%<em>,r </em>= 6%<em>,δ </em>= 2%.</li>

</ul>

Calculate and report the price for the European Call and Put using explicit, implicit, and Crank-Nicolson methods, while including the number of steps that you calculated in the previous point (part d).

<ul>

 <li>Repeat part (d) of this problem, but this time get the empirical number of iterations. Specifically, obtain the Black Scholes price for the data in (e), then do an iterative procedure to figure out the ∆<em>x</em>, ∆<em>t</em>, <em>N</em>, and <em>N<sub>j </sub></em>to obtain the accuracy for <em>ε </em>= 0<em>.</em> Put the results of the 3 methods (EFD, IFD, CNFD) side by side in a table and write your observations.</li>

 <li>Using the parameters from part (e), plot on the same graph the implicit finite difference values <em>p<sub>u</sub>,p<sub>m</sub>,p<sub>d </sub></em>as a function of <em>σ </em>∈{0<em>.</em>05<em>,</em>0<em>.</em>1<em>,</em>0<em>.</em>15<em>,…,</em>0<em>.</em>6}. Write detailed comments on your observations.</li>

 <li>Implement the Crank-Nicolson Finite Difference method and price both European Call and Put options. Use the same parameters as in part (e) and the same number of steps in the grid. Put the results of the 3 methods (EFD, IFD, CNFD) side by side in a table and write your observations.</li>

 <li>Calculate the hedge sensitivities for the European call option using the Explicit Finite Difference method. You need to calculate Delta, Gamma, Theta, and Vega.</li>

</ul>

<strong>Problem 2 . Finite difference methods applied to market data. </strong>We will use here the algorithms implemented in Problem 1 to price European Call and Put options using market data, and compare these methods.

<ul>

 <li>Download Option prices (you can use the Bloomberg Terminal, Yahoo! Finance, etc.) for an equity, for 3 different maturities (1 month, 2 months, and 3 months) and 10 strike prices. Use the same method from Homework 1 to calculate the implied volatility. Set the current short-term interest rate equal to the one from the day you downloaded the data.</li>

 <li>Use the Explicit, Implicit, and Crank-Nicolson Finite Difference schemes implemented in Problem 1 to price European Call and Put options. Use the calculated implied volatility to obtain a space parameter ∆<em>x </em>that insures stability and convergence with an error magnitude of no greater than 0<em>.</em>001<em>.</em></li>

 <li>For the European style options above (puts and calls) calculate the corresponding Delta, Gamma, Theta, and Vega using the Explicit finite difference method.</li>

 <li>Create a table with the following columns: time to maturity <em>T</em>, strike price <em>K</em>, type of the option (Call or Put), ask price <em>A</em>, bid price <em>B</em>, market price <em>C<sub>M </sub></em>= (<em>A</em>+<em>B</em>)<em>/</em>2, implied volatility from the BSM model <em>σ</em><sub>imp</sub>, option price calculated with EFD, IFD, and CNFD. Plot on the same graph <em>A,B,C<sub>M</sub></em>, and the 3 option prices obtained with finite difference schemes, as a function of <em>K </em>and <em>T</em>. What do you observe?</li>

</ul>

<strong>Problem 3. Design an EFD scheme </strong>We know that an option price under a certain stochastic model satisfies the following PDE:

<em>.</em>

Assume you have an equidistant grid with points of the form (<em>i,j</em>) = (<em>i</em>∆<em>t,j</em>∆<em>x</em>), where <em>i </em>∈{1<em>,</em>2<em>,…,N</em>} and <em>j </em>∈{−<em>N<sub>S</sub>,N<sub>S</sub></em>}. Let <em>V<sub>i,j </sub></em>= (<em>i</em>∆<em>t,j</em>∆<em>x</em>).

<ol>

 <li>Discretize the derivatives and give the finite difference equation for an Explicit scheme. Use the notation introduced above.</li>

 <li>Assume you have to be pricing a European Call. Do you need boundary conditions? If you do what are the boundary conditions?</li>

 <li>What do you observe about the process of updating coefficients?</li>

</ol>