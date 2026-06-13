## Chapter 4 

## Discrete-Time Signal Modeling 

Profs.: David Lavanchy & Maurizio Tognolini HEIG-VD 

MA-StatDig Lecture4 v1.5 11.03.2024 

**1** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **Objectives of this chapter** 

1. Signal Modeling problem 

2. Least square direct method 

3. The Prony approximation 

3.1.Shanks approximation 

4. Finite Lengths Data records 

4.1.Autocorrelation method 

4.2.Covariance method 

MA-StatDig Lecture4 v1.5 11.03.2024 

**2** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **Signal Modeling** 

## The signal modelling problem 

- The goal  of signal modelling is to build  a model  able to  reproduce the desired signal x(n) , non deterministic , usually  from another signal v(n) how we know the behaviour. 

- The input signal could  be  a deterministic signal ad  a unit impulse d(n)  or  a  periodic  sequence of  unit impulses or  a random process  as  a white noise signal w(n). 

- Another part of the model is  the transfer function H(z) who transform (linearly and dynamically) the input signal v(n)  to obtain the  desired signal x(n). 

**==> picture [455 x 142] intentionally omitted <==**

**----- Start of picture text -----**<br>
ˆ<br>v n H z [B][q] [(] [z] [)] x n<br>( ) ( ) = ( )<br>A z<br>p ( )<br>The goal is to minimise the model error:<br>ˆ<br>ys (k)z*<br>[ ——] k=0 , (4.3) e [0] ( n ) =  x ( n )  − x ( n )<br>**----- End of picture text -----**<br>


- Therefore, in developing an approach of signal modelling , it will  be important not only to find  a model that is useful, i.e. works well, but also one that has a computationally efficient procedure for deriving the  model parameters from the given data. 

MA-StatDig Lecture4 v1.5 11.03.2024 

**3** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **Least squares (direct) method** 

- In this method we model a deterministic signal x(n) as the unit sample response of  a linear time invariant LTI filter h(n). In this case we use  as input signal v(n) = d(n)  a unit impulse. 

- We assume that x(n) = 0  for n<0 and  h(n) = 0 for n<0 because  the system  is causal. The model error could be written: 

**==> picture [158 x 20] intentionally omitted <==**

- The goal is  to reduce  the error as  small as possible acting on the coefficients of the filter, we need  to define a value (variable) that represent the error, in this case  we  will use  the L2 norm of the error e’(n). 

**==> picture [124 x 149] intentionally omitted <==**

MA-StatDig Lecture4 v1.5 11.03.2024 

**4** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **Least squares (direct) method** 

- To find the coefficients  of the filter that minimize the least square error we could compute the  partial derivative of  the square  error  with respect to each of the coefficients: 

**==> picture [317 x 251] intentionally omitted <==**

- Using the Parseval theorem we could exprime  the square error with integral of the power spectrum of the error e’(n). 

- The partial derivative shown above  produce  a system of  p+q+1 non linear equations to solve to find  the filter parameters. 

- The algorithms to solve those equations  are iterative  and not adapted for real time signal processing, for this reason we  will study  some indirect methods  to  optimise  the  filter coefficients to reduce  the  mean square error. 

MA-StatDig Lecture4 v1.5 11.03.2024 

> D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 **5** 

## **The Padé Approximation** 

- Because the nonlinear equations to find  optimum value of  the coefficients  of the  filter  are non linear  and lead to mathematically intractable solutions, Padé  approximation only require solving a set of linear equations. 

## Exemple 4.3.1 

- Let x(n) be a signal that is to be modelled using a causal fist order filter all-pole (AR1) : 

**==> picture [475 x 46] intentionally omitted <==**

**==> picture [42 x 23] intentionally omitted <==**

_−_ The impulse response is : _h_ ( _n_ ) = _b_ (0)[ _a_ (1)] _[n] u_ ( _n_ ) 

The difference  equation is : 

## _x n b d n − a x n −_ ( ) = (0) ( ) (1) ( 1) 

We put the constraint **x(n) = h(n)** , and  as we have only 2 parameters **b(0) and a(1)** we could satisfy the  constraint only for **n= 0, 1** (for perfect matching for x(n) for n= 0 and 1): 

**==> picture [380 x 66] intentionally omitted <==**

**==> picture [298 x 73] intentionally omitted <==**

MA-StatDig Lecture4 v1.5 11.03.2024 

## **The Padé** 

## **Approximation** 

- If we want to model 3 samples  of  x(n) is to be modelled using a causal ARMA1 filter : 

**==> picture [206 x 52] intentionally omitted <==**

**==> picture [318 x 35] intentionally omitted <==**

> In this case the impulse response is : _h_ ( _n_ ) = _b_ (0)[ _−a_ (1)] _[n] u_ ( _n_ ) + _b_ (1)[ _−a_ (1)] _[n][−]_[1] _u_ ( _n −_ 1) 

> The difference  equation is : _x_ ( _n_ ) = _b_ (0) _d_ ( _n_ ) + _b_ (1) _d_ ( _n −_ 1) _− a_ (1) _x_ ( _n −_ 1) 

We put the constraint **x(n) = h(n)** , and  as we have 3 parameters **b(0) , b(1) and a(1)** we could satisfy the  constraint only for **n= 0, 1 , 2** (for perfect matching for x(n) for n= 0 , 1 and 2): 

_x_ (0) 

**==> picture [407 x 52] intentionally omitted <==**

In this case  we  find: 

**==> picture [459 x 46] intentionally omitted <==**

This method  imply  a  resolution of  a  non linear  system of  equations, and  this  is  the case  for  superior orders. We will see  it is possible to reformulate  the problem  to  solve  a  linear  system of  equations…. 

MA-StatDig Lecture4 v1.5 11.03.2024 

**7** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

q+1 

p 

## **The Padé** 

## **Approximation** 

- It  is possible to reformulate  the problem  to  solve  a  linear  system of  equations, if we  start from the transfer function H(z) for an ARMA filter and  write the related difference equation we have: 

**==> picture [564 x 93] intentionally omitted <==**

**==> picture [38 x 18] intentionally omitted <==**

**==> picture [42 x 16] intentionally omitted <==**

- We see in the last chapter, we can write this equation using matrix expression with Youle-Walker eq: p+1 

**==> picture [137 x 113] intentionally omitted <==**

**----- Start of picture text -----**<br>
q+1<br>p<br>p<br>**----- End of picture text -----**<br>


MA-StatDig Lecture4 v1.5 11.03.2024 

p 

**8** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **The Padé 1st step** 

- To solve the linear system of equation (4.11) with p+q+1 unknown and p+q+1 equations we need  2 step approach, first we solve the lower part, to find ap coefficients. 

- We could write the same system differently to remove the first line  and replace it by a column vector . 

- And putting the  constant vector to the right side: 

p 

**==> picture [48 x 18] intentionally omitted <==**

MA-StatDig Lecture4 v1.5 11.03.2024 

**==> picture [8 x 10] intentionally omitted <==**

**----- Start of picture text -----**<br>
p<br>**----- End of picture text -----**<br>


= **X a** _−_ **x** _q p q_ +1 D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

(4.14) 

**9** 

## **The Padé 1st step solutions** 

The system (4.14) of linear p equations and p unknown is composed by **X** q non-symmetric Toeplitz matrix. 3 different cases could happens: 

- **Case I** : **X** q is non singular then we can inverse it and a unique solution for the coefficients of Ap(z) exist and given by: 

**a** _p_ = _−_ **X** _[−] q_[1] **[x]** _[q]_[+1] 

- **Case II** : **X** q is singular and multiple solutions for the coefficients of Ap(z) exist and given by the homogenous eq. 

**==> picture [82 x 22] intentionally omitted <==**

**==> picture [48 x 18] intentionally omitted <==**

˜ **a** = **a z** + _p p_ 

- **Case III** : **X** q is singular and no solutions exists.  In the coefficients of Ap(z) we assume ap(0) = 1 as usual but in this case this assumption is incorrect and we  set ap(0) = 0  with this we could  solve the system  to find the coefficients of Ap(z): 

**X a** = 0 _q p_ 

(4.16) 

Since **X** q is singular, there is nonzero solutions to these homogeneous  equations. 

MA-StatDig Lecture4 v1.5 11.03.2024 

**10** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **The Padé 2st step** 

- After solving the  eq (4.14) to find the coefficients ap(k) we apply those values  to the firsts (q+1)  eq of (4.11)  to find  the  coefficients bq(k) : 

p+1 

q+1 

**==> picture [133 x 28] intentionally omitted <==**

**----- Start of picture text -----**<br>
=<br>X a  b<br>0<br>p q<br>**----- End of picture text -----**<br>


**==> picture [43 x 16] intentionally omitted <==**

This  the  same  as the initial eq. (4.10): 

_b n x n ⇤ a n q_ ( ) = ( ) _p_ ( ) 

**==> picture [366 x 46] intentionally omitted <==**

Note  that **if we have  an MA filter in this  case p=0** : 

**==> picture [335 x 21] intentionally omitted <==**

**Note** the error e’(n) = x(n) - h(n)  of the Padé approximation is equal to zero over  the first p+q+1 samples. 

MA-StatDig Lecture4 v1.5 11.03.2024 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

**11** 

## **Padé Example 4.3.2** 

Given for the signal  sequence x(n) the  first 6 samples, we want to modelize with Padé approximation the signal x(n) : 

**==> picture [281 x 18] intentionally omitted <==**

1. First we  take p=2 q=0  AR(2) model ,  as  we have  q=0  we need  to do only  the 1st step of Padé solving the eq (4.13): 

**==> picture [381 x 128] intentionally omitted <==**

The matrix **Xq** is non singular in this case we have an unique solution for **ap** : 

**==> picture [457 x 57] intentionally omitted <==**

We notice  the filter described by H(z) is unstable , but the  impulse response is identical to x(n)  for n= 0,1,2.  After it diverge  and the approximation error  come very large. 

**==> picture [405 x 20] intentionally omitted <==**

MA-StatDig Lecture4 v1.5 11.03.2024 

**12** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **The Prony Approximation** 

- In the Prony approach we  try to minimize  the error of  the approximation using  the least square  error. 

**==> picture [467 x 171] intentionally omitted <==**

The  goal is  to find  the coefficients ap(n)  and  bq(n)  of the  model filter  in order to minimize  the  square error,  an equivalent form  is given also in the  z  domain: 

As we see in the least square direct method the minimisation of  the least square  error produce  a non linear  system of  equations to  solve. We could  redefine another  error  e(n) and  his z transform as: 

**==> picture [335 x 22] intentionally omitted <==**

**==> picture [451 x 24] intentionally omitted <==**

Minimize this error e(n) by least square minimisation of the error  give the  same  result in term of coefficients ap(n)  and bq(n) as minimising the error e’(n)  defined in the direct method. 

MA-StatDig Lecture4 v1.5 11.03.2024 

**13** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **The Prony Approximation** 

We could write the error e(n) for  each value of n considering  that for n > q  bq(n) = 0 . 

**==> picture [568 x 53] intentionally omitted <==**

**==> picture [663 x 227] intentionally omitted <==**

**==> picture [148 x 23] intentionally omitted <==**

**==> picture [38 x 14] intentionally omitted <==**

**X q** is  a  convolution matrix, with p columns  and  N-q raw if N is  the length of the signal, this  system is overdetermined  and  to find  the  leas square approximation of  the  coefficient ap we need  to use the pseudo inverse. 

MA-StatDig Lecture4 v1.5 11.03.2024 

> D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 **14** 

## **The Prony Approximation** 

If  we  multiply  each  side of  the eq (4.51) by **Xq[H]** we see the pseudo inverse  solution:. 

**==> picture [367 x 24] intentionally omitted <==**

**==> picture [221 x 23] intentionally omitted <==**

Note the product  ( **Xq[H] Xq) =  Rx** is the autocorrelation matrix and  the second member **Xq[H ] xq+1 = rx** . 

**==> picture [312 x 24] intentionally omitted <==**

For the bq(n) coefficients  the  method is  the same  as  for the Pade approximation see  eq. (4.17) and (4.18). 

## **X a** = **b** 0 _p q_ 

**Note** : The bq coefficient  are  computed  using only the p values of  the  signal  from x(n-1) to x(n-p)  and they  are not an optimisation with least square  minimisation of the error. 

MA-StatDig Lecture4 v1.5 11.03.2024 

**15** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **The Prony Approximation** 

In term of auto correlation we  could  exprime  the  coefficients, that  is  the theoretic  définition  of the Prony approximation,  and it is useful when the  autocorrelation  is  theoretically  defined : 

**==> picture [500 x 109] intentionally omitted <==**

## With the  matrix  we  could  write: 

**==> picture [360 x 19] intentionally omitted <==**

**Note** : The minimum value (if the ap(k)  coefficients satisfies the normal equation 4.28) of the squared error is given by : 

**==> picture [213 x 43] intentionally omitted <==**

MA-StatDig Lecture4 v1.5 11.03.2024 

**16** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **Prony enhancement Shanks’ method** 

**As mentioned in Prony  approximation** the bq coefficient  are  computed  using only the p values of  the signal  from x(n-1) to x(n-p)  and  they  are not an optimisation with least square  minimisation of the error. An enhanced  version  of Prony is called Shanks’ Method, who  compute the **bq** coefficient by leas square. 

**==> picture [589 x 175] intentionally omitted <==**

MA-StatDig Lecture4 v1.5 11.03.2024 

> D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 **17** 

## **Prony enhancement Shanks’ method** 

The  goal is  to minimize the L2  norm of  the e’(n) error: 

**==> picture [657 x 126] intentionally omitted <==**

## After  the  minimisation of  the  error  we  find finally : 

**==> picture [325 x 53] intentionally omitted <==**

**==> picture [38 x 14] intentionally omitted <==**

## Written in matrix format we have : 

**==> picture [194 x 25] intentionally omitted <==**

MA-StatDig Lecture4 v1.5 11.03.2024 

> D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 **18** 

## **Prony enhancement Shanks’ method** 

## When we don’t have the theory expressions of the correlations  we could use the sample values: 

**==> picture [270 x 52] intentionally omitted <==**

**==> picture [38 x 14] intentionally omitted <==**

**==> picture [38 x 14] intentionally omitted <==**

MA-StatDig Lecture4 v1.5 11.03.2024 

**19** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **Finite Data Records** 

- Suppose the signal x(n) is only known in the finite interval [0,N] and we could find an all-pole  model for x(n) finding the  coefficients ap(k) by minimising the square error : 

**==> picture [652 x 61] intentionally omitted <==**

- In the Prony approximation we considered an infinite data record x(n), and  we minimise the error to find the filter coefficients a_p(k) by leas square minimisation of the error. 

- Practically we rarely dispose of the infinite sequence of data and in any case  we  could not compute with an infinite number of samples. 

- In the case of  the finite number of  the sample we need to suppose  what  about the  values outside  the sample interval 0 to N-1. 

- We consider 2 approaches : the **Autocorrelation method** and the **Covariance method** : 

- In the **Autocorrelation method** we suppose the sample outside the interval [0,N-1] are 0 values. 

- In the **Covariance method** we use only  the samples in the interval [0,N-1] to compute the  filter coefficients by minimising the  squared error. 

MA-StatDig Lecture4 v1.5 11.03.2024 

> D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 **20** 

## **Autocorrelation Method** 

 As explained before, if the signal x(n) is unspecified or unknown outside the interval [0,N], for  the autocorrelation method we assume x(n)=0  for n < 0  and for n > N. 

**==> picture [655 x 51] intentionally omitted <==**

- To compute the  coefficients ap(k) we may define the autocorrelation as (assuming x(n)=0  for n < 0  and for n > N, we  rename x(n), x[~] (n)). 

**==> picture [630 x 50] intentionally omitted <==**

- With this new definition of the autocorrelation rx(k) we could compute the  coefficients ap(k)  as shown in Prony method. 

**==> picture [338 x 51] intentionally omitted <==**

- As we see in the Prony method we could determine the  solution with the least square overdetermined system of equations (4.120) for n>0 . In matrix  form that is: 

**==> picture [108 x 20] intentionally omitted <==**

**==> picture [45 x 14] intentionally omitted <==**

MA-StatDig Lecture4 v1.5 11.03.2024 

**21** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **Autocorrelation Method** 

- The matrix **Xp** with dimensions _(N + p) x p_ and the column vector x1 with dimensions (N + p) x 1 are defined in this case as : 

**==> picture [255 x 19] intentionally omitted <==**

**==> picture [45 x 14] intentionally omitted <==**

## **X** _[H]_ ( _p_ **[X]** _[p]_[)] **[¯a]** _[p]_[=] _[ −]_ **[X]** _[H] p_ **[x]**[1] 

## **¯a** = _−_ **X x** _p pinv_ ( _p_ ) 1 

- The minimum error of the  model is  given by : 

**==> picture [225 x 54] intentionally omitted <==**

MA-StatDig Lecture4 v1.5 11.03.2024 

**22** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **Covariance Method** 

- As explained before, if the signal x(n) is unspecified or unknown outside the interval [0,N], for  the covariance method **we do any assumptions about data outside  the observation interval [0,N]** . 

- The  model  obtained with the  covariance  method is more accurate (closer to the theory model)  than the autocorrelation method. 

- With covariance method  we loos however the Toeplitz structure of the normal equation and  the guaranty of  the stability of the all pole model. 

- To develop the covariance method  we need to reconsider  the expression of  the squared error  of  the Prony approximation: 

**==> picture [615 x 83] intentionally omitted <==**

If we modify the definition of the  squared error to take in account only the data we know: 

**==> picture [223 x 55] intentionally omitted <==**

Minimization of this squared error make any assumption of the data outside the record interval [0,N]. 

MA-StatDig Lecture4 v1.5 11.03.2024 

**23** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **Covariance Method** 

- The covariance normal equations  are  the same of  the Prony  normal equations, the only difference is the definition of the  estimation  of  the autocorrelation sequence rx(k,l). 

**==> picture [411 x 55] intentionally omitted <==**

- With this definition of the autocorrelation we  write the normal equations. Unlike the autocorrelation method  the  covariance  normal equations  are not Toeplitz, the fast resolving algorithms  as LevinsonDurbin  recursion  cannot be used. 

**==> picture [45 x 14] intentionally omitted <==**

##  The covariance modelling error is: 

**==> picture [319 x 55] intentionally omitted <==**

MA-StatDig Lecture4 v1.5 11.03.2024 

**24** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **Covariance Method** 

- From the  data record we could formulate the normal equations  as a least square  approximation problem. If we set the error in (4.120) equal to 0  in the interval n = [p,N] we have a set of N - p + 1 linear equations  as : 

**==> picture [585 x 119] intentionally omitted <==**

**==> picture [121 x 22] intentionally omitted <==**

**==> picture [482 x 72] intentionally omitted <==**

- Practically we  could  build  the matrixes  with the  convolution matrix  using the convmtx Malab function: 

**==> picture [134 x 75] intentionally omitted <==**

MA-StatDig Lecture4 v1.5 11.03.2024 

**25** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **Example  with sinus finite data record** 

##  We consider  a data record  of samples of the sinus function defined by: 

_x_ ( _n_ ) = _Asin_ ( _!_ 0 _n_ + _φ_ ) = _Asin_ (2 _⇡/N_ 0 _n_ + _φ_ ) 

##  By theory the autocorrelation of x(n) is (see ex 3.3.1) : 

**==> picture [427 x 42] intentionally omitted <==**

##  With this  definition we  could  compute  the Prony  model of  a 2nd order  all pole filter : 

**==> picture [295 x 237] intentionally omitted <==**

**==> picture [220 x 40] intentionally omitted <==**

**==> picture [335 x 14] intentionally omitted <==**

**==> picture [360 x 65] intentionally omitted <==**

## MA-StatDig Lecture4 v1.5 11.03.2024 

**26** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **Example  with sinus finite data record** 

MA-StatDig Lecture4 v1.5 11.03.2024 

**27** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **Example  with sinus finite data record** 

## **Autocorrelation Method  to  estimate  the all pole  filter** 

The  estimation of the autocorrelation as  the  Prony Autocorrelation method   is  different: 

**==> picture [252 x 46] intentionally omitted <==**

**==> picture [250 x 33] intentionally omitted <==**

**==> picture [325 x 133] intentionally omitted <==**

**----- Start of picture text -----**<br>
ˆ 0 . 4909 0 . 4582 0 . 4582<br>ˆ<br>Rx = rx =<br>0 . 4582 0 . 4909 0 . 3824<br>" # " #<br>+1 . 0000<br>✏ 2 = 1 . 6882<br>2 3<br>a = − 1 . 6027<br>pacm<br>64+0 . 717075 bq (0) = [p] ✏ 2 = 1 . 2993<br>**----- End of picture text -----**<br>


**==> picture [205 x 45] intentionally omitted <==**

**----- Start of picture text -----**<br>
-0.50 Real Axisie<br>MA-StatDig Lecture4 v1.5<br>11.03.2024<br>**----- End of picture text -----**<br>


**28** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **Example  with sinus finite data record** 

## **Covariance Method  to  estimate  the all pole  filter** 

## Now  try  with  the  Covariance  method: 

**==> picture [246 x 47] intentionally omitted <==**

**==> picture [237 x 30] intentionally omitted <==**

**==> picture [272 x 110] intentionally omitted <==**

## MA-StatDig Lecture4 v1.5 11.03.2024 

**29** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## Stochastic ARMA Models 

So far we have modelled deterministic signals as the unit sample response of a LTI system 

In this section, the goal is to model stochastic signals, as the output of an causal linear shift-invariant filter, given the input is a unit variance white noise sequence. 

An ARMA(p,q) process may be generated by filtering a unit variance white noise v(n) with a causal linear shift-invariant filter having p poles and q zeros 

MA-StatDig Lecture4 v1.5 11.03.2024 

**30** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## Stochastic ARMA Models 

The goal is now to find the missing coefficients by minimizing the mean square error This though will result in a nonlinear problem The autocorrelation sequence of an ARMA(p,q) process satisfies the Yule-Walker equations (Eq. 3.115) Where cq(k) is the convolution of b q(k) and h*(-k) And rx(k) is a statistical autocorrelation 

**==> picture [48 x 12] intentionally omitted <==**

**----- Start of picture text -----**<br>
Eq 3.115<br>**----- End of picture text -----**<br>


MA-StatDig Lecture4 v1.5 11.03.2024 

**31** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## Stochastic ARMA Models 

Since h(n) is causal, then cq(k)=0 for k>q and the YuleWalker equations for k>q are a function only of the coefficients ap(k). 

This can be expressed in matrix form for k=q+1,…,q+p which is a set of p linear equations with p unknowns ap(k). 

These equations are called the Modified YuleWalker equations Hence this approach is called the Modified YuleWalker Equation (MYWE) method 

If the autocorrelation is unknown, then an estimate is used 

MA-StatDig Lecture4 v1.5 11.03.2024 

> D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 **32** 

## **Simplest case of AR(p) process** 

An AR process  is  simpler because  we need only  to find the  ap(k) coefficients of the transfer function: If the input signal _v_ ( _n_ ) of the filter H(z)  is a white noise with  the  variance _σ_[2] with _v_ power _Pv_ ( _z_ ) = _σv_[2] the output power is: 

In term of power density spectrum function of _ω_ : 

The Yule-Walker eq 3.115 is applied  with  q=0 for this AR(p) process with : 

**==> picture [165 x 43] intentionally omitted <==**

**----- Start of picture text -----**<br>
b (0)<br>H ( z ) =<br>1 + ∑ [p] k =1 [a][p] [(] [k] [)] [z] [−] [k]<br>**----- End of picture text -----**<br>


| _b_ (0) |[2] _Px_ ( _z_ ) = _σv_[2] _Ap_ ( _z_ ) _Ap_ * (1/ _z_ ) 

**==> picture [159 x 50] intentionally omitted <==**

**----- Start of picture text -----**<br>
| b (0) | [2]<br>Px ( e [jω] ) =  σv [2]<br>| A ( e [jω] ) | [2]<br>p<br>**----- End of picture text -----**<br>


_c_ 0(0) = _b_ (0) _h_ *(0) = | _b_ (0) |[2] 

_p rx_ ( _k_ ) + ∑ _ap_ ( _l_ ) _rx_ ( _k_ − _l_ ) = _σv_[2][|] _[b]_[(0)][|][2] _[δ]_[(] _[k]_[);] _[ k]_[≥0] _l_ =1 

MA-StatDig Lecture4 v1.5 11.03.2024 

**33** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## **Simplest case of AR(p) process** 

In matrix for  we  have: 

> Here  we can solve  first the _a p_ coif. Ising the  lines  from 1 to p of the linear system of  eq. After we could  solve  the first line  to find b(0) coeff. 

MA-StatDig Lecture4 v1.5 11.03.2024 

> D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 **34** 

## **Example of  of AR(1) process** 

For example  an AR(1) process with _σv_[2][= 1] and the property _rx_ ( _k_ ) = _rx_ (− _k_ ) the system of  eq  is: 

From second eq  we find a(1) : 

And next from first eq we find b(0): 

**==> picture [168 x 20] intentionally omitted <==**

_rx_ (0) _a_ (1) = − _rx_ (1) 

**==> picture [230 x 86] intentionally omitted <==**

The transfer  function is then: 

_r r_[2] _x_ (0)[ _x_[(0) −] _[r] x_[2][(1)]] _H_ ( _z_ ) = _rx_ (0) − _rx_ (1) _z_[−1] 

MA-StatDig Lecture4 v1.5 11.03.2024 

> D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 **35** 

## Stochastic ARMA Models 

After the coefficients ap(k) have been determined, the next step is to find the MA coefficients bq(k) 

One approach is filtering x(n) with A p(z) resulting in y(n) with power spectrum 

Now the moving average coefficients bq(k) may be estimated from y(n) using one of the moving average techniques presented later on. 

MA-StatDig Lecture4 v1.5 11.03.2024 

**36** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## Stochastic ARMA Models 

A direct approach for finding the coefficients bq(k) uses the Yule-Walker equations for k=0,…,q 

Since cq(k)=0 for k>q the sequence cq(k) is then known for all k>=0  (but not for k<0) 

We denote the z-transform of the causal part of cq(k) Similarly the anti-causal part is 

MA-StatDig Lecture4 v1.5 11.03.2024 

**37** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## Stochastic ARMA Models 

Recall 

## Hence 

Multiplying Cq(z) by Ap*(1/z*) results in the power spectrum of the MA(q) process 

Since ap(k)=0 for k<0  , A p*(1/z*) only contains positive powers of z. The causal part of Py(z) therefore. 

MA-StatDig Lecture4 v1.5 11.03.2024 

**38** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## Stochastic ARMA Models 

Although cq(k) is unknown for k<0, the causal part of Py(z) may be computed from the causal part of cq(k) and the coefficients ap(k) 

Using the conjugate symmetry of Py(z) we may then determine Py(z) for all z 

Finally, performing a spectral factorization of Py(z) produces the polynomial Bq(z) 

MA-StatDig Lecture4 v1.5 11.03.2024 

> D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 **39** 

## Stochastic ARMA Example 

The goal is to find an ARMA(1,1) model for a realvalued random process with: The modified Yule-Walker equations are in general 

In this example  p=1, q=1: 

Resulting in : 

This was the easy part, now let’s find the MA coefficients 

…. 

MA-StatDig Lecture4 v1.5 11.03.2024 

**40** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## Stochastic ARMA Example 

In general for ARMA model we can use: In this example  p=1, q=1: 

Resulting in : 

Hence : 

Multiplying with Result in : Hence the casual part of  Py(z): 

MA-StatDig Lecture4 v1.5 11.03.2024 

**41** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

## Stochastic ARMA Example 

Using the symmetry of  Py(z): 

Which, after spectral factorization results in  : 

Which in turn leads to the desired : ARMA(1,1) model 

MA-StatDig Lecture4 v1.5 11.03.2024 

**42** 

D.Lavanchy, M.Tognolini (c) HEIG-VD 2024 

