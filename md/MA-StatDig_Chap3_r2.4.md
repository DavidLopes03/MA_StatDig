## Discrete-Time Random Processes 

Profs.: David Lavanchy & Maurizio Tognolini HEIG-VD 

MA-StatDig Lecture3 v2.4 19.02.2024 

**1** 

## **Objectives of this chapter** 

- [Introduction to random variables. ] 

- [Moments of  random variables ] 

- [Joint moments  ] 

- [Parameters estimations ] 

- [Introduction to Random process ] 

- [Stationarity and ergodicity  ] 

- [Power spectrum] 

MA-StatDig Lecture3 v2.4 19.02.2024 

**2** 

## **Random variables** 

 **Example of random variable:** A fair  coin that is equally likely to result (Head or Tail) when flipped. With a  large amount of flipping we would be Heads half of the time and Tail the other half. 

 If  we flip N times (N large)  result would be _nH nT_ approximatively: _N_[= 0] _[.]_[5] _N_[= 0] _[.]_[5] 

It is  an equal probability to get a Tail or a Head result, the  probability assignments is made for two possible experimental  outcomes  H={Heads} and T={Tails}: _Pr{H}_ = 0 _._ 5 _Pr{T }_ = 0 _._ 5 

MA-StatDig Lecture3 v2.4 19.02.2024 

**3** 

## **Sample space and events** 

 The set of  all possible experimental outcomes are called _sample space_ denoted by    . We define : Ω 

_Pr{_ Ω _}_ = 1 

For the coin flipping experiment we have: Ω= _{H, T } Pr{H, T }_ = 1 

Subsets of the sample are called _events_ and subsets consisting of a single element are called _elementary events_ . In our example we have two elementary events: 

= = _ω H ω T_ 1 _{ }_ 2 _{ }_ 

MA-StatDig Lecture3 v2.4 19.02.2024 

**4** 

## **Mapping of events to random variable** 

 We map now a real variable x to the outcome, we can say x is the amount of gain in CHF. 

The mapping  is defined between the set of experimental outcomes             and the set of real numbers,R: _ωi ∈_ Ω _f_ : Ω _→ R_ = _ω_ 1 _{H}_ = _⇒ x_ = 1 = _ω_ 2 _{T }_ = _⇥ x_ = _−_ 1 Sample Space Q 0 We can also associate  a probability to ®) 6 * the variable x: Oe 2 _Pr{x_ = 1 _}_ = 0 _._ 5 _Pr{x_ = _−_ 1 _}_ = 0 _._ 5 Q; « 3; For  any number  a different to 1 or -1 | the probability : Figure 3.1 The definition of a random variable in terms of a mapping _Pr{x_ = _α}_ = 0 _if α ⇥_ = _±_ 1 from elementary events in a sample space Q to points on the real line. and 

_Pr_ Ω = _Pr x_ = _±_ 1 = 1 _{ } { }_ 

MA-StatDig Lecture3 v2.4 19.02.2024 

**5** 

## **Discrete random variable** 

 In this experiment the  random variable x is a _discrete real variable_ and generally they  could have  an associated probability: 

_Pr{x_ = 1 _}_ = _p Pr{x_ = _−_ 1 _}_ = 1 _− p_ 

- In the roll of fair die experiment we have a real random variable with 6 possible values, because  we map the x value to the number obtained with the roll of the die. 

 A _complex random variable_ may be defined by assigning complex numbers to elementary events in the sample space. Ex. two fair die, each giving  a real  number  m and n assigned to the real and imaginary part of z : 

**==> picture [121 x 22] intentionally omitted <==**

MA-StatDig Lecture3 v2.4 19.02.2024 

**6** 

## **Continuos random variable** 

 **Random variable could be** _**continuos**_ **and may be assume  a continuum of values** . 

**Ex:** An infinite  resolution roulette wheel for which any number in the interval [0,1] may result from the spin of the wheel. The sample space of this experiment is: Ω= _{ω_ : 0 _≤ ω ≤_ 1 _}_ The number in the interval [0,1] is equally likely to occur than the probability assignment to     may be Ω defined as follow: _Pr{⇥ ⇤ I}_ = _Pr{α_ 1 _< ⇥ ⇥ α_ 2 _}_ = _α_ 2 _− α_ 1 where I is an interval                     that is a subset of _I_ =] _α_ 1 _, α_ 1] Ω For two disjoints intervals I1 and I2 we have: _Pr{ω ∈ I_ 1 _or ω ∈ I_ 2 _}_ = _Pr{ω ∈ I_ 1 _}_ + _Pr{ω ∈ I_ 2 _}_ 

MA-StatDig Lecture3 v2.4 19.02.2024 

**7** 

## **Probability Distribution function** 

 For a real valued random variable x one statistical characterisation is the _F α probability distribution function x_ ( ) _F α Pr x α x_ ( ) = _{ ≤ }_ For the coin tossing experiment we have: 

Typically  the **discrete** random variable  has picewise continuos probability distribution function . 

**==> picture [259 x 157] intentionally omitted <==**

**----- Start of picture text -----**<br>
Fx ( α )<br>1<br>α<br>−<br>1 1<br>**----- End of picture text -----**<br>


MA-StatDig Lecture3 v2.4 19.02.2024 

**8** 

## **Probability density function** 

 Another  useful statistical characterisation of a random variable is the _probability density function_ , which is the derivative of the distribution function. _α[d] fx_ ( ) = _dα[F][x]_[(] _[α]_[)] For the coin experiment the   probability density function is given by: 

Typically  the **discrete** random variable  has unit impulse  probability density. 

**==> picture [219 x 145] intentionally omitted <==**

**----- Start of picture text -----**<br>
fx ( α )<br>(1 / 2) (1 / 2)<br>α<br>−<br>1 1<br>**----- End of picture text -----**<br>


MA-StatDig Lecture3 v2.4 19.02.2024 

**9** 

## **Case of a continuos random variable** 

##  For the spinning roulette we have: 

**==> picture [611 x 266] intentionally omitted <==**

**----- Start of picture text -----**<br>
 0 ; α <  0<br>1 ; 0  ≤ α ≤ 1<br>Fx ( α ) = α ; 0  ≤ α <  1 fx ( α ) =<br>⇤ 0 ; otherwise<br>⇥ 1 ; 1  ≤ α<br>Fx ( α ) fx ( α )<br>1<br>1<br>α α<br>− 1 1 − 1 1<br>**----- End of picture text -----**<br>


MA-StatDig Lecture3 v2.4 19.02.2024 

**10** 

## **Ensemble Averages** 

- In many application a complete statistical characterisation of  a random variable may not be possible or necessary if the average  behaviour of the random variable is known. 

 Expected value of  a random variable x that assume the value     with the probability                    is defined _αk Pr{x_ = _αk}_ as: 

**==> picture [282 x 25] intentionally omitted <==**

_k_ 

 Using the  density probability  function, this _⇥_ expectation may be written as: _E x_ = _α dα { } αfx_ ( ) _−⇥_ 

**==> picture [319 x 25] intentionally omitted <==**

MA-StatDig Lecture3 v2.4 19.02.2024 

**11** 

## **Example with roll die** 

 _N_ Suppose that the die is rolled      times and that _T nk_ number k appears      times. The average value is given by: = _x[n]_[1][ + 2] _[n]_[2][ + 3] _[n]_[3][ + 4] _[n]_[4][ + 5] _[n]_[5][ + 6] _[n]_[6] _⟨ ⇥NT N T_ 

**==> picture [475 x 104] intentionally omitted <==**

The expected values could be calculated as: 

**==> picture [422 x 71] intentionally omitted <==**

E{x} ne prends pas forcement une valeur qui fait partie de l’ensemble des x possibles MA-StatDig Lecture3 v2.4 19.02.2024 

**12** 

## **Expected value of a function of random variable** 

 In order to find the average power dissipated in a resistor  when the current intensity x applied is a = random variable. The dissipated  power is _y Rx_[2] and  we have to find the expected value of y. If  x  has _α_ = _x_ a  probability density function          and if _fx_ ( ) _y g_ ( ) then: _⇥ E_ = _E x_ = _α α dα {y} {g_ ( ) _} g_ ( ) _fx_ ( ) _−⇥_ 

 Example: for the average power in the resistor we have: 

_⇥_ 

= _P E Rx_[2] = _R α_[2] _α dα ⇤ ⌅ { } fx_ ( ) _−⇥_ 

Exercice : calculer P moyen MA-StatDig Lecture3 v2.4 19.02.2024 

**13** 

## **Variance** 

 The mean square value is  frequently used as a measure for the quality of an estimate. For example  the ˆ _x_ estimator     that minimise the mean square error, **(See later)** = ˆ _E x − x ξ {_ [ ][2] _}_  The mean square value of the random variable y=x-E{x} is called **Variance** : 

**==> picture [516 x 57] intentionally omitted <==**

## _σx_ is called the **standard deviation** . 

 Due to the linearity of the expectation we can write: 

**==> picture [476 x 28] intentionally omitted <==**

## **Exercice:** démontrer cette  équivalence 

MA-StatDig Lecture3 v2.4 19.02.2024 

**14** 

## **Jointly distributed random variables** 

 In the case  we work with more than one random variable and they are not independent we need a _joint distribution function_ . (ex: y = x(1) + jx(2) ) 

- Given two random variables x(1) and x(2) the joint distribution function is: 

_F α Pr x α α x_ (1) _,x_ (2)( 1 _, α_ 2) = _{_ (1) _≤_ 1 _, x_ (2) _≤_ 2 _} α_ 1 which defines the probability that x(1) is less than _α_ **and** x(2) is less than     . 2 

- The joint density function for two random variables : 

**==> picture [464 x 57] intentionally omitted <==**

MA-StatDig Lecture3 v2.4 19.02.2024 

**15** 

## **Joint Moments** 

 _r_ The correlation denoted      is the second order joint _xy_ moment: 

**==> picture [147 x 26] intentionally omitted <==**

 An ensemble average related to the correlation is the covariance       : _cxy_ 

= _c Cov E x − m − m_ = _E m m[∗] xy_ ( _x, y_ ) = _{_ [ _x_ ][ _y y_ ] _[∗] } {xy[∗] } − x y_ = = _m E x m E_ where                     and                   . _x { } y {y}_  Frequently , it is useful to normalise the covariance so that is invariant to scaling. That is the correlation coeff. _[∗][∗][∗]_ 

**==> picture [512 x 61] intentionally omitted <==**

and we have 1 _|ρxy| ≤_ 

MA-StatDig Lecture3 v2.4 19.02.2024 

**16** 

## **Independent, Uncorrelated** 

- In order to test if two random variables have any relationship or dependence. 

**Definition:** Two random variables x and y are said to be statistically independent if the joint probability density function is separable, 

_α fx,y_ ( _α, ⇥_ ) = _fx_ ( ) _fy_ ( _⇥_ ) 

 A weaker form but more easy to apply of independence is: 

= _r E_ = _E x E_ = _m m[∗] xy {xy[∗] } { } {y[∗] } x y c_ = _r m m[∗]_ then _xy xy − x y_[= 0] then the random variables x and y are uncorrelated. 

 Clearly, statistically independent random variables are always uncorrelated. MA-StatDig Lecture3 v2.4 19.02.2024 

**17** 

## **Orthogonality of random variables** 

 **Property :** The variance of a sum of **uncorrelated** random variables is equal to the sum of the variables _V ar{x_ + _y}_ = _V ar{x}_ + _V ar{y}_ 

- A property related to un-correlatedness is orthogonality, and for two random variables are said orthogonal if their correlation is zero 

_r_ = 0 _xy_ 

- Zero mean uncorrelated variables will always be orthogonal. 

MA-StatDig Lecture3 v2.4 19.02.2024 

**18** 

## **Linear mean square estimation.** 

 Here we consider the problem of estimation of  a random variable y in term of an observation of another random variable x. That because  the variable y can’t be directly measured or observed. In ˆ mean square estimation  an estimate     is to be found _y_ that minimise the mean square error: ˆ = _E − ξ {_ ( _y y_ )[2] _}_ in linear mean square estimation the estimator is constrained to be of the form 

ˆ _y_ = _ax_ + _b_ the  goal is to find the variables  a  and  b that minimize the men square error 

ˆ = _⇠ E{_ ( _y − y_ )[2] _}_ = _E{_ ( _y − ax − b_ )[2] _}_ 

MA-StatDig Lecture3 v2.4 19.02.2024 

**19** 

## **Linear mean square error estimator** 

 If we derive the mean square error we will find the minima of the error and  the related b and a. 

_⇥ξ_[= 0] _⇥a_[=] _[ −]_[2] _[E][{]_[(] _[y][ −][ax][ −][b]_[)] _[x][}]_[ =] _[ −]_[2] _[E][{][xy][}]_[ + 2] _[aE][{][x]_[2] _[}]_[ + 2] _[bm][x] ⇥ξ ⇥b_[=] _[ −]_[2] _[E][{]_[(] _[y][ −][ax][ −][b]_[)] _[}]_[ =] _[ −]_[2] _[m][y]_[ + 2] _[am][x]_[ + 2] _[b]_[ = 0] _E −_ ˆ _x_ = _E ex_ = 0 the  first equation says: _{_ ( _y y_ ) _} { }_ where  e is the estimator error, and it is known as the orthogonality principle. If  we  solve  for a and b: 

**==> picture [432 x 127] intentionally omitted <==**

MA-StatDig Lecture3 v2.4 19.02.2024 

**20** 

## **Best estimate** 

**==> picture [427 x 59] intentionally omitted <==**

and for b: 

**==> picture [587 x 244] intentionally omitted <==**

**==> picture [606 x 102] intentionally omitted <==**

**21** 

## Linear Mean-Square Estimation 

- In general 

- Assume that x and y are uncorrelated, then 

- Assume that and therefore which implies 

MA-StatDig Lecture3 v2.4 19.02.2024 

**22** 

## **Gaussian Random variable** 

**==> picture [628 x 159] intentionally omitted <==**

- For two random variables x and y they are defined _jointly_ 

MA-StatDig Lecture3 v2.4 19.02.2024 

**23** 

## **Property of  Gaussian distribution** 

 **Property 1** : In x and y are jointly Gaussian then for any constant a and b the  random variable                     is  also _z_ = _ax_ + _by_ Gaussian with mean: _mz_ = _amx_ + _bmy_ and variance: _⇥z_ = _a_[2] _⇥x_[2][+] _[ b]_[2] _[⇥] y_[2][+ 2] _[ab⇥][x][⇥][y][ρ][xy]_ 

 **Property 2** : If two Gaussian variables are uncorrelated = 0 _ρxy_ then they are statistically independent: _α fxy_ ( _α, ⇥_ ) = _fx_ ( ) _fy_ ( _⇥_ ) 

 **Property 3** : If x and y are jointly Gaussian the optimum nonlinear estimator for y=g(x) that minimize the meanˆ square error ,is  a linear estimator: _y_ = _ax_ + _b_ 

 **Property 4** : If x is Gaussian with zero mean: 

1 _·_ 3 _·_ 5 _. . . n − σ[n] n even E{x[n] }_ = ( 1) _x_ ; 0 _n odd_ ; 

MA-StatDig Lecture3 v2.4 19.02.2024 

**24** 

## **Bias and consistency** 

 Consider the problem of estimating the parameter    of a _θ_ sequence of random variables     for                         . _xn n_ = 1 _,_ 2 _, . . . , N_ Since the ˆ _θ_ estimate is a function of N variables we will denote it by _N_ In general we would that the estimate is equal on the average to the true value. 

 The difference between the expected value of the estimate and the actual value     is called the Bias and will be noted B: _θ_ = _B θ − E θ {_[ˆ] _N }_ if the bias is zero then the expected value of the estimate is equal to the true value and the estimate is said unbiased. 

_E θ_ = _θ {_[ˆ] _N }_ If             then     is said biased. If an estimate is biased but the _B_ = 0 _θ_ ˆ bias  goes to zero as the number  N goes to infinity, is said _asymptotically unbiased_ lim _N →⇥[E][{][θ]_[ˆ] _[N][}]_[ =] _[ θ]_ 

MA-StatDig Lecture3 v2.4 19.02.2024 

**25** 

## **Example 3.2.2** 

 Let _x_ a random variable defined on the coin flipping experiment, the values of _x_ are 1 or -1 and the coin is unfair so that the probability of Head is _p_ and ( _1-p_ ) for the Tail. The mean value of _x_ is: 

_m_ = _E x_ = _− − −_ 1 _x { } p_ (1 _p_ ) = 2 _p_ 

However, suppose the value of _p_ is unknown  and that the mean of _x_ is to be estimated. 

 Flipping the coin N times and denoting the resulting values  for _x_ by     , consider the estimator for       (the _xi mx_ expected value). 

The expected value is estimated  with the last value of x ˆ (for this example): _mx_ = _xN_ 

_m_ ˆ _x E{m_ ˆ _x}_ = _E{xN }_ = _E{x}_ = 2 _p −_ 1 The expected value of       is: then this estimator is _unbiased._ 

MA-StatDig Lecture3 v2.4 19.02.2024 

**26** 

## **Example 3.2.2** 

ˆ  _mx_ It is clear  that the estimator       is a good estimate for the  mean. Therefore the accuracy of the estimator does not improve as a number of observations N increases. The variance of the estimate is: 

_− − V ar{_ ˆ _mx}_ = _V ar{xN }_ = _E{_ ( _x E{xN }_ )[2] _}_ = _E{_ ( _x_[2] 2 _xE{xN }_ + _E_[2] _{xN }_ ) _}_ = _E x_[2] 2 _E_[2] _x_ + _E_[2] _x_ = _E x_[2] _E_[2] _x { } − { } { } { } − { }_ And the therms: _− E x_[2] = _− { } p_ + ( 1)[2] (1 _p_ ) = 1 _E_[2] _{x}_ = (2 _p −_ 1)[2] 

Then: _V ar x_ = 1 _− −_ = 4 _− { N }_ (2 _p_ 1)[2] _p_ (1 _p_ ) 

Does not decrease with N. 

MA-StatDig Lecture3 v2.4 19.02.2024 

**27** 

## **Parameter estimation** 

 In order to estimate  a parameter convergence, in some sense , to its true value  it is  necessary  that the variance of the estimate go to zero as the number of observations goes to infinity, lim[lim][=] _[−][E][{][θ]_[ˆ] _[N][}|]_[2] _[}]_[ = 0] _N →⇥[V ar][θ]_[ˆ] _[N] N →⇥[E][{|][θ]_[ˆ] _[N]_ ˆ if       is unbiased,                   , it follows from the _θN E{θ_[ˆ] _N }_ = _θ ϵ >_ 0 Tchebycheff inequality that for any _− Pr{|⇥_[ˆ] _N ⇥| ⇤ ϵ} ⇥[V ar][{][⇥]_[ˆ] _[N][}] ϵ_[2] ˆ _θN is said to converge to     with probability oneθ_ . 

MA-StatDig Lecture3 v2.4 19.02.2024 

**28** 

## **Mean-square convergence** 

 Another stronger form of convergence with probability one  is given by the mean-square. 

lim _[−][θ][}|]_[2] _[}]_[ = 0] _N →⇥[E][{|][θ]_[ˆ] _[N]_ 

 The estimate is said to be consistent if it converge to the true value of the parameter. 

 **Exemple 3.2.3** : The sample mean Let x be a r.v. with a mean       and the  variance      . _mx σx_[2] _x n_ Given N uncorrelated  observations  of  x  denoted by _m_ suppose that the estimator for       is formed as follow, _x_ 

_N_ ˆ = _m_[1] _x x n N n_ =1 

MA-StatDig Lecture3 v2.4 19.02.2024 

**29** 

## **Example 3.2.3** 

**==> picture [602 x 147] intentionally omitted <==**

- Therefore the sample mean is an unbiased estimator. The variance of the estimate is: 

**==> picture [356 x 70] intentionally omitted <==**

the sample mean is a consistent estimator. 

MA-StatDig Lecture3 v2.4 19.02.2024 

**30** 

## **RANDOM PROCESS** 

##  **Definitions** : 

As a **random variable** may be thought of as a mapping from a sample space of a given experiment into the set of a real or complex numbers , a **discrete-time random process** is a mapping from the sample space    into the set of discrete time Ω signals x(n). Thus a discrete-time random process is a collection or ensemble of discrete time signals. 

- We will focus our attention to discretetime random processes, such as the white noise process on the right 

MA-StatDig Lecture3 v2.4 19.02.2024 

**31** 

## **Example of  a  random** 

## **process** 

 Consider a rolling of a fair die and let the outcome of a roll of the die be assigned to the _**random variable**_ **A** that assumes  an integer value from 1 to 6. With 

_x n Acos nω_ ( ) = ( 0) 

a _**random process**_ has been created that consist of an ensemble of six different discrete-time signals. 

MA-StatDig Lecture3 v2.4 19.02.2024 

**32** 

## **Example of  a  random** 

## **process** 

- An example of a random process would be to flip a fair coin at each instance in time and set x(n)=1 for Heads and x(n)=-1 for Tails. Since each flip would be independent of each other flip, this is called a Bernoulli process 

MA-StatDig Lecture3 v2.4 19.02.2024 

**33** 

## **Example of  a  random** 

## **process** 

- Often random processes are filtered with LTI filters such as resulting in a new output process 

y(n) = O.Sy(m — 1) + x(n). MA-StatDig Lecture3 v2.4 19.02.2024 

**34** 

## Random Processes 

- A powerful point of view for a discrete-time random process is, that it is simply an indexed sequence of random variables 

- Where each r.v. has an underlying probability distribution function or probability density function 

- The dependencies between these indexed r.v.’s can now be described by a joint distribution function 

MA-StatDig Lecture3 v2.4 19.02.2024 

**35** 

## Random Processes 

- As an example, assume a random process is formed form a sequence of Gaussian random variables x(n) 

- If the variables are uncorrelated, this is so called Gaussian white noise 

- If though x(n)=α, where α is a Gaussian r.v., then each sample realisation in the ensemble is equal to a constant for all times 

- Both processes have the same first-order statistics, the difference is in their higher order statistics 

MA-StatDig Lecture3 v2.4 19.02.2024 

**36** 

## **Ensemble averages** 

 Since a discrete-time random process is an indexed sequence of random variables, sees x(—2), x(—1), x(0), x(1), x(2), tae we may calculate  the mean of each of these random variables and generate  the (deterministic) sequence known as mean of the process. 

_m n E x n x_ ( ) = _{_ ( ) _}_ Similarly computing the variance of each random variable in the sequence that defines the variance of the process. _σ_[2] _x_[(] _[n]_[) =] _[ E][{|][x]_[(] _[n]_[)] _[ −][m][x]_[(] _[n]_[)] _[|]_[2] _[}]_  Two additional ensemble  averages that are important in the study of random processes are the autocovariance: 

_c E x k − m k x l − m l x_ ( _k, l_ ) = _{_ [ ( ) _x_ ( )][ ( ) _x_ ( )] _[∗] }_ 

MA-StatDig Lecture3 v2.4 19.02.2024 

**37** 

## **Autocorrelation** 

##  The autocorrelation is given by: 

_r E x k x l x_ ( _k, l_ ) = _{_ ( ) ( ) _[∗] }_ 

relating  x(k) and x(l). 

 If k=l the  auto-covariance is reduced to variance: _c σ_[2] _x_ ( _k, k_ ) = _x_[(] _[k]_[)]  The covariance and the  correlation are related by: _c r − m k m[∗] x_ ( _k, l_ ) = _x_ ( _k, l_ ) _x_ ( ) _x_[(] _[l]_[)] 

For convenience, unless stated otherwise , random processes will always be assumed to have zero mean, so auto-covariance and autocorrelation could be used interchangeably. 

MA-StatDig Lecture3 v2.4 19.02.2024 

**38** 

## **Covariance and correlation** 

 Auto-covariance and autocorrelation sequences provide informations about the same random process. When more than one process are involved for ex. x(k) from one process and y(l) from another, we can define correlation and covariance: 

_c E x k − m k l − m l xy_ ( _k, l_ ) = _{_ [ ( ) _x_ ( )][ _y_ ( ) _y_ ( )] _[∗] } rxy_ ( _k, l_ ) = _E{x_ ( _k_ ) _y_ ( _l_ ) _[∗] } c r − m k m[∗] xy_ ( _k, l_ ) = _xy_ ( _k, l_ ) _x_ ( ) _y_[(] _[l]_[)] 

_c_ If                       two random process are said _xy_ ( _k, l_ ) = 0 uncorrelated. If                      the two process are  said _rxy_ ( _k, l_ ) = 0 to be orthogonal. 

MA-StatDig Lecture3 v2.4 19.02.2024 

**39** 

## **Example 3.3.1** 

 The harmonic process: Consider the random phase sinusoid: 

**==> picture [233 x 25] intentionally omitted <==**

where A and     are constant and    is a random variable _ω_ 0 _φ −π · · · π_ that is uniformly distributed over               the probability density function is given by: 

_− ⇥ ⇥ α ⇥_ (2 ) _[−]_[1] ; _⇥ ⇥ α fφ_ ( ) = 0 _otherwise_ ; 

The mean of this process is: 

**==> picture [417 x 25] intentionally omitted <==**

> _⇥_ 1 _m n x_ ( ) = 2 _⇥[Asin]_[(] _[n⇤]_[0][ +] _[ α]_[)] _[dα]_[ = 0] _−⇥_ 

MA-StatDig Lecture3 v2.4 19.02.2024 

**40** 

## **Example** 

 The autocorrelation of x(n) may be determined in a similar fashion 

_rx_ ( _k, l_ ) = _E{x_ ( _k_ ) _x[∗]_ ( _l_ ) _}_ = _E{Asin_ ( _k⇥_ 0 + _φ_ ) _Asin_ ( _l⇥_ 0 + _φ_ ) _} r_[1] _x_ ( _k, l_ ) = 2 _[A]_[2] _[E][{][cos]_[[(] _[k][ −][l]_[)] _[⇥]_[0][]] _[} −]_[1] 2 _[A]_[2] _[E][{][cos]_[[(] _[k]_[ +] _[ l]_[)] _[⇥]_[0][ + 2] _[φ]_[]] _[}]_ the first term is  an expected value of  a constant and the second  term is equal to zero. Therefore: 

**==> picture [292 x 50] intentionally omitted <==**

We notice  that  the autocorrelation of **x(n)** don’t **k k-l** . depends of , it depend only of  the  difference We called this  process: Wide Sense **stationary** (WSS) process. 

MA-StatDig Lecture3 v2.4 19.02.2024 

**41** 

## **Autocorrelation of a sum of process.** 

 In any application of data acquisition, **noise or measurement errors are invariably introduced** into recorded data. In many application noise is modelled as additive noise: _y_ ( _n_ ) = _x_ ( _n_ ) + _w_ ( _n_ ) where  w(n) is an additive noise zero mean and uncorrelated to the signal x(n). In this case the autocorrelation of the recorded signal y(n): _ry_ ( _k, l_ ) = _E{y_ ( _k_ ) _y_ ( _l_ ) _[∗] }_ = _E{_ [ _x_ ( _k_ ) + _w_ ( _k_ )][ _x_ ( _l_ ) + _w_ ( _l_ )] _[∗] }_ = _E x k x l_ + _E w k w l_ + _E x k w l_ + _E w k x l {_ ( ) ( ) _[∗] } {_ ( ) ( ) _[∗] } {_ ( ) ( ) _[∗] } {_ ( ) ( ) _[∗] }_ if x(n) and w(n) are uncorrelated: 

_E{x_ ( _k_ ) _w_ ( _l_ ) _[∗] }_ = _E{w_ ( _k_ ) _x_ ( _l_ ) _[∗] }_ = 0 

and then: 

_r r r y_ ( _k, l_ ) = _x_ ( _k, l_ ) + _w_ ( _k, l_ ) 

MA-StatDig Lecture3 v2.4 19.02.2024 

**42** 

## Ensemble Averages Example 3.3.3 

## • Consider M sinusoids in additive noise 

MA-StatDig Lecture3 v2.4 19.02.2024 

**43** 

## **Example 3.3.2** 

- Given two processes x(n) and y(n), where 

- The cross-correlation between x(n) and y(n) is 

- If y(n) is the output of an LSI filter with x(n) as input it follows 

MA-StatDig Lecture3 v2.4 19.02.2024 

**44** 

## **Stationary processes** 

 In signal processing applications, the statistics or ensemble averages of a random process are often . independent of time 

- The case of statistical time-invariance is said . 

- stationary 

 If the first-order density function of a random process x(n) is independent of time for  all k, the process are _α α_ said first order stationary: _fx_ ( _n_ )( ) = _fx_ ( _n_ + _k_ )( ) 

 For a first-order stationary process the first-order statistics are independent of time. The mean of the _m n m_ process are constant. _x_ ( ) = _x_ And also for the variance: _σ_[2] _x_[(] _[n]_[) =] _[ σ] x_[2] 

 A process is  second order stationary if for any k the process x(n) and the process x(n+k) have the same second order joint density function. 

MA-StatDig Lecture3 v2.4 19.02.2024 

**45** 

## **Second order stationary random process.** 

 The joint density function does not depend of time: 

_α α fx_ ( _n_ 1) _,x_ ( _n_ 2)( 1 _, α_ 2) = _fx_ ( _n_ 1+ _k_ ) _,x_ ( _n_ 2+ _k_ )( 1 _, α_ 2) _rx_ ( _k, l_ ) = _rx_ ( _k_ + _n, l_ + _n_ )  In this case the autocorrelation sequence: _r r k − x_ ( _k, l_ ) = _x_ ( _l,_ 0) the correlation depends only on the difference k-l separating the two variables in time: 

_r r x_ ( _k, l_ ) = _x_ ( _Lag_ ) 

 This difference is called the lag, and in this case we will drop the second argument: 

MA-StatDig Lecture3 v2.4 19.02.2024 

**46** 

## **Wide stationary process WSS** 

- A process is strictly stationary, if the joint probability density functions of any order are independent of n 

- Since we will concentrate on ensemble averages such as correlations and cross-correlations,a more useful concept is “wide sense stationarity” 

- Note that is weaker than second-order stationarity, since it is defined on ensemble averages and not on densities 

**Definition:** 

A random process is said wide-sense stationary if the following three conditions are satisfied: 

1. The mean of the process is a constant: 

2. The autocorrelation depends only of the lag. 

3. The variance of the process is finite 

MA-StatDig Lecture3 v2.4 19.02.2024 

**47** 

## Stationary Processes WSS 

- A similar concept exists for two or more processes 

   - Jointly wide sense stationary 

   - x(n) and y(n) have to be WSS and 

_rxy_ ( _k, l_ ) = _rxy_ ( _k_ + _n, l_ + _n_ ) _r k − l E x k l xy_ ( ) = _{_ ( ) _y[⇤]_ ( ) _}_ 

• The autocorrelation sequence of a WSS  process has a number of useful Property properties a conjugate 

- 

- Property 1 follows from the definition 

_rx_ ( _k_ ) = _E{x_ ( _n_ + _k_ ) _x[⇤]_ ( _n_ ) _}_ = _E{x[⇤]_ ( _n_ ) _x_ ( _n_ + _k_ ) _}_ = _rx[⇤]_[(] _[−][k]_[)] 

MA-StatDig Lecture3 v2.4 19.02.2024 

**48** 

## Stationary Processes WSS 

- This property relates the value of the autocorrelation sequence at 0 with the mean-square value of the process 

- Again, this property follows directly from the definition 

MA-StatDig Lecture3 v2.4 19.02.2024 

**49** 

## Stationary Processes WSS 

- This property places an upper bound on the autocorrelation sequence 

- And the last property is concerned with mean-square periodic processes 

Therefore, if a = 27/N, then r,(k) is periodic with period N and x(n) is mean-square MA-StatDig Lecture3 v2.4 periodic. 19.02.2024 

**50** 

## Autocorrelation Matrices 

• Often the autocorrelation sequence is represented in matrix form 

• Taking the expectation results in the autocorrelation matrix 

- Clearly 

MA-StatDig Lecture3 v2.4 19.02.2024 

**51** 

## Autocorrelation Matrices 

- Note that the autocorrelation matrix is a Hermitian Toeplitz matrix (in the case of a real process: symmetric Toeplitz) 

- In other words 

- Property 2: **R** x>=0 

   - **R** x is positive semi definite (or nonnegative) (error in book: **R** x>0) 

- 

- Property 3 

- The eigenvalues of the autocorrelation matrix  of  a WSS process are  real and non- negative. 

MA-StatDig Lecture3 v2.4 19.02.2024 

**52** 

## Autocorrelation Matrices Example 

MA-StatDig Lecture3 v2.4 19.02.2024 

**53** 

## What is Ergodicity? 

- Most often, the autocorrelation sequence and the mean are needed, but not explicitly available. All that we have access to is a sample realization of the random process 

- Hence we need to estimate the needed ensemble averages using time averages 

   - But is this always permissible? 

MA-StatDig Lecture3 v2.4 19.02.2024 

**54** 

## Ergodicity problem 

- First, let us estimate the mean m x(n) of a random process x(n) 

- If we assume that we have a large number of sample realizations of the process available, this works as follows 

- Most of the time, we only have . 

- one realization of the process Hence we need to estimate the needed ensemble averages using time averages 

MA-StatDig Lecture3 v2.4 19.02.2024 

**55** 

## Ergodicity exemple 

- For this to work, some constraints must be imposed on the process 

- For example, assume we have this random process, where A is either 1 or 2 with probability 50% 

- The mean of this process is 

- Using a single realization for this process and a large number of samples N, the time average will result in 

MA-StatDig Lecture3 v2.4 19.02.2024 

**56** 

## **Exemple 3.3.5** 

MA-StatDig Lecture3 v2.4 19.02.2024 

**57** 

## **Exemple 3.3.5 /2** 

MA-StatDig Lecture3 v2.4 19.02.2024 

**58** 

## White Noise 

- A WSS process is called white if 

- Hence white noise is simply a sequence of uncorrelated random variables each having a variance of 

- Since this is the only condition for white noise, there is an infinite number of white noise processes 

MA-StatDig Lecture3 v2.4 19.02.2024 

**59** 

## The Power Spectrum 

- The power spectrum (or more precisely the power spectral density) of a WSS process is defined as the discrete-time Fourier transform of the autocorrelation sequence 

- If the power spectrum is known the inverse discrete-time Fourier transform results in the autocorrelation sequence 

- Sometimes it is convenient to use the z-transform instead of the discrete-time Fourier transform 

MA-StatDig Lecture3 v2.4 19.02.2024 

**60** 

## Power Spectrum properties 

## • The power spectrum has a number of useful properties 

MA-StatDig Lecture3 v2.4 19.02.2024 

**61** 

## • The power spectrum has a number of useful properties 

MA-StatDig Lecture3 v2.4 19.02.2024 

**62** 

## The Power Spectrum Example 

## MA-StatDig Lecture3 v2.4 19.02.2024 

**63** 

## Filtering Random Processes 

- What happens if we let a WSS process through a LTI filter? 

- What happens to the mean of the output process y(n)? 

- What happens to the autocorrelation function of the output process y(n)? 

   - To answer that, we need to compute first the cross-correlation sequence between the input and the output, which only depends on the difference between n+k and n 

MA-StatDig Lecture3 v2.4 19.02.2024 

**64** 

## Filtering Random 

## Processes 

• The autocorrelation sequence might now be computed as follows 

MA-StatDig Lecture3 v2.4 19.02.2024 

**65** 

## Filtering Random Processes 

• Therefore, if x(n) is WSS, then y(n) is WSS (given the filter is stable), furthermore, since the cross-correlation only depends on the lag, they are also jointly WSS 

• An interesting interpretation of this result follows by noticing that r is the deterministic h autocorrelation of the unit sample response hence 

MA-StatDig Lecture3 v2.4 19.02.2024 

**66** 

## Filtering Random Processes 

## • And the frequency domain interpretation of this result is 

MA-StatDig Lecture3 v2.4 19.02.2024 

**67** 

## 3.4.1 Filtering White noise 

MA-StatDig Lecture3 v2.4 19.02.2024 

**68** 

## Example 

## MA-StatDig Lecture3 v2.4 19.02.2024 

**69** 

## **Special Types Of Random Processes** 

- Autoregressive Moving Average Process ARMA(p,q) 

   - We filter white noise v(n) b,(k)z* σ H(z) = Ba —prot 

   - ( Pv(z) = v[2] ) with a causal LTI filter having a rational system function re re 1+) ap(k)z k=1 

   - with p poles and q zeros 

- We filter white noise v(n) 

- Assuming that the filter is stable, the output process x(n) will be WSS and its power spectrum will be 

- Or in terms of ω 

MA-StatDig Lecture3 v2.4 19.02.2024 

**70** 

## **Example** The power spectrum of an ARMA(2,2) process is shown in Fig. 3.11. This process is 

MA-StatDig Lecture3 v2.4 19.02.2024 

**71** 

## **Special Types Of Random Processes** 

- Autoregressive Moving Average Process ARMA(p,q) 

- Or in terms of difference equations 

- Multiply both sides with x*(n-k) and take the expected value 

- Since v(n) is WSS it follows that v(n) and x(n) are jointly WSS, so let 

- Which results in 

MA-StatDig Lecture3 v2.4 19.02.2024 

**72** 

## **ARMA** 

- Since 

and v(n) is white noise 

- The cross-correlation may be written as 

- Substituting this result into 

leads to 

- Assuming that h(n) is causal the right side can be written as 

MA-StatDig Lecture3 v2.4 19.02.2024 

**73** 

## **ARMA** 

• Since c (k) = 0 for k>q it follows q which are the Yule-Walker equations 

- Most often these are written in matrix form 

- Note that 

defines a recursion for the autocorrelation sequence in terms of a (k) p and b (k) O2¢(k) ; q 

- cq(n) is given with h(n) and bq(n), where h(n) is given by ap(k) and bq(k) 

- • If p>=q then for k>=p it holds ' p 

MA-StatDig Lecture3 v2.4 19.02.2024 

**74** 

## **Autoregressive Process** 

- When q=0 (no zeros) we have an all-pole filter 

- An ARMA(p,0) is called an autoregressive process of order p AR(p) 

- If the driving white noise has a power spectrum of then the power spectrum of x(n) is 

- ω 

- Or in terms of the frequency variable 

MA-StatDig Lecture3 v2.4 19.02.2024 

**75** 

## **Autoregressive Process** 

## • Recall the general Yule-Walker equations 

- For q=0, the Yule-Walker equations become a linear set of equations – co(0) = b(0)h*(0) = This makes all pole modeling very popular 

- Or in the convolution form 

MA-StatDig Lecture3 v2.4 19.02.2024 

**76** 

## **Autoregressive Process Example** 

MA-StatDig Lecture3 v2.4 19.02.2024 

**77** 

## **Autoregressive Process Example** 

MA-StatDig Lecture3 v2.4 19.02.2024 

**78** 

## **Autoregressive Process Example** 

MA-StatDig Lecture3 v2.4 19.02.2024 

**79** 

## **Autoregressive Process Example** 

MA-StatDig Lecture3 v2.4 19.02.2024 

**80** 

## **Autoregressive Process Example** 

MA-StatDig Lecture3 v2.4 19.02.2024 

**81** 

## **Moving Average Process** 

- If an ARMA model has no poles, i.e. ARMA(0,q) is called a moving average model MA(q). This is a FIR filter driven by white noise 

- For a driving white noise process of 

- The power spectrum of the MA(q) model is 

- ω 

- Or in terms of the frequency 

MA-StatDig Lecture3 v2.4 19.02.2024 

**82** 

## **Moving Average Process** 

- The general Yule-Walker equations are 

- For a MA(q) model h(n)=b(n) hence 

- This results in l= 

- where the absolute value ensures that the equation holds for all k 

- Hence the autocorrelation sequences of an MA(q) process is zero outside the interval [-q, q] 

MA-StatDig Lecture3 v2.4 19.02.2024 

**83** 

## **Moving Average Process** 

- Note that rx(k) depends nonlinearly on the moving average parameters bq(k) 

- For example MA(2) 

- Hence estimating the parameters for a moving average process is not as straight forward as for an ARMA process 

MA-StatDig Lecture3 v2.4 19.02.2024 

**84** 

# Exercises 

# Exercise 

## Solution 

## Trick: subtract the mean from both r.v.‘s 

## Exercise 

## Solution 

# Exercise 

## Solution 

## Solution 

## Exercise 

## Solution 

## Solution 

# Exercise 

## Solution 

# Exercise 

## Solution 

# Exercise 

## Solution 

# Exercise 

## Solution 

# Exercise 

## Solution 

