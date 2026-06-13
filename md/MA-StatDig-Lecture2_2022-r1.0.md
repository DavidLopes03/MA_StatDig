## **Linear Algebra** 

# Linear Algebra 

In this chapter we will make a reminder from linear algebra applications in signal processing. Linear Algebra is  à powerful tool in the  discrete signal analysis. 

- Random Signal modelling by basis functions and 

- are illustrated. 

Matlab use only vector representation of discretetime signals. 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Vector representation of discrete-time signals** 

# Discrete-time signal could be represented as a N dimension vector in concise way: 

_x_  (0) ⇥ _x_ (1) x = ... _− x N_ ( 1) ⇧⇧⇧⇤ ⌃⌃⌃⌅ **x** is said real vector if  the samples x(n) are real or **x** is said complex vector if x(n) are complex values. 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Transpose and Hermitian transpose** 

x _[T]_ The  transpose       is a row vector: 

**==> picture [826 x 159] intentionally omitted <==**

**==> picture [903 x 51] intentionally omitted <==**

**x** (n) is a vector of N elements that is parametrized by time index n: 

**==> picture [895 x 132] intentionally omitted <==**

## **Norm  distance metric of a vector** 

The Euclidian norm or      is defined for  a vector _L_ 2 **x** of dimension N  by: 

**==> picture [389 x 134] intentionally omitted <==**

**----- Start of picture text -----**<br>
1 / 2<br>N<br>=<br>x x<br>2 i<br>⇥ ⇥ | | [2]<br>⇤<br>i =1 ⇥<br>**----- End of picture text -----**<br>


The     norm is defined as: _L_ 1 

The       norm : _L∞_ 

**==> picture [257 x 116] intentionally omitted <==**

**----- Start of picture text -----**<br>
N<br>=<br>x x<br>1 i<br>⇥ ⇥ | |<br>i =1<br>**----- End of picture text -----**<br>


**==> picture [303 x 41] intentionally omitted <==**

**----- Start of picture text -----**<br>
=<br>x  max x<br>∞ i i<br>⇥ ⇥ | |<br>**----- End of picture text -----**<br>


MA-StatDig Lecture2 v1.0 15.02.2022 

## **Distance and inner product** 

The distance      between two vectors  could be _L_ 2 defined as: 

**==> picture [879 x 258] intentionally omitted <==**

_N_ 

**==> picture [413 x 84] intentionally omitted <==**

For real vectors Hermitian is replaced by transpose 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Inner product and distance** 

The inner product defines the geometrical relation between two vectors. 

= a b a b _cosθ ⟨ , ⇥ ⇤ ⇤⇤ ⇤_ 

Thus two nonzero vectors **a** and **b** are said orthogonal if: 

a b = 0 _⟨ , ⇥ cosθ_ 1 Since                 then: _| | ≤_ 

a b a b _|⇥ , ⇤| ≤⇧ ⇧⇧ ⇧_ is said Cauchy-Schwarz inequity, and we have equity when **a** and **b** are collinear i.e.              .a = _α_ b 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Another Inequality** 

Another useful inequality is the following: 

2 a b a b + _|⇥ , ⇤| ≤⇧ ⇧_[2] _⇧ ⇧_[2] we can find this relation with: a _±_ b _⇥_ 0 _⇤ ⇤_[2] that we expand: 

= _⇧_ a _±_ b _⇧_[2] _⇧_ a _⇧_[2] _±_ 2 _⇤_ a _,_ b _⌅_ + _⇧_ b _⇧_[2] _⇥_ 0 then we know                       and  we find the a _±_ b _⇥_ 0 _⇤ ⇤_[2] inequity. 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Vector space and dimensions of  space** 

Given N vectors: 

> Given N vectors: V = v v v _{_ 1 _,_ 2 _, . . . , N } V_ the set of vectors    that may be formed with a v linear combination of vectors _i_ 

_N_ 

v = _α_ v _i i i_ =1 

This form a _vector space_ and the vectors      are said to v _i span_ the space _V_ 

v _i_ If the vectors      are _linearly independent_ , then they form a _basis of the space_ , and the _V_ number N  is said a _dimension of the space_ . 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Linear independence, Vector Spaces, Basis Vectors** 

v v v A set of n vectors                         is said to be 1 _,_ 2 _, . . . ,_ n linearly independent if : 

_α_ 1v1 + _α_ 2v2 + _. . ._ + _αn_ vn = 0 _α_ = 0 _∀i i_ implies that _α_ if  a nonzero     can be found then the set is _i_ linearly dependent. At least one of the vectors may be expressed as a linear combination of the others vectors: 

= v v v _. . ._ v 1 _β_ 2 2 + _β_ 3 3 + + _βn_ n 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Exemple 2.3.2** 

1 1 Given the two vectors:  ⇥  ⇥ = = v 2 v 0 1 2 1 1 ⇤ ⌅ ⇤ ⌅ we write the linear independent test : 1 1 0  ⇥  ⇥  ⇥ = = _α_ 1v1 + _α_ 2v2 _α_ 1 2 + _α_ 2 0 0 1 1 0 ⇤ ⌅ ⇤ ⌅ ⇤ ⌅ 2 _α_ = 0 1 _α α_ = 0 1 + 2 

# Given the two vectors: 

we write the linear independent test : 

then we have: 

= _α α_ = 0 and  we found                       that mean the two 1 2 vectors are linearly independent. 

MA-StatDig Lecture2 v1.0 

15.02.2022 

|— MASTERIN ENGINEERING OF SCIENCE **Definitions: Subspace, Span Subspace** : A subspace of **V** is defined as  a subset _P_ ⊆ _V_ that satisfies the properties: 

∀ x,y ∈ _P_ ⇒ x+y ∈ _P_ ∀ x ∈ _P α_ ∈ _S_ ⇒ _α_ x ∈ _P_ , ∀ 

S is  a scalar space 

**Span** : Given an arbitrary set of M vectors _W_ = {x[(] _[m]_[)] } _m M_ =1,2,⋯, the span of these vectors is defined as: 

**==> picture [463 x 75] intentionally omitted <==**

The span of W is the set of all possible linear  combinations of the vectors in W. The set of vectors W is called  linearly independent if the following holds: 

**==> picture [553 x 80] intentionally omitted <==**

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Basis Synthesis Formula** 

> The set of K vectors _W_ = {x[(] _[K]_[)] } _k_ =1⋯ _K_ from a subspace P is a base of  this  subspace if : 

● The set W is linearly independent ● The span covers completely P: span{W}=P and  we can write for ∈ _P_ could be written as  a linear combination  of x[(] _[K]_[)] any y { } _k_ =1⋯ _K K_ y = _α_ x[(] _[K]_[)] _k_ ∑ _k_ =1 Orthogonal and orthonormal basis: in this case the set _W_ = {x[(] _[K]_[)] } _k_ =1⋯ _K_ we have the constraint: **x**[(] _[i]_[)] **x**[(] _[j]_[)] _δ i_ − ⟨ , ⟩= [ _j_ ] when i=j  the scalar product is equal1  otherwise  is equal 0. A set of N orthogonal vectors  in a N dimension space is  a base of this space. 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Properties of orthonormal basis** 

_W_ = {x[(] _[K]_[)] } _k_ =1⋯ _K_ is  an orthonormal basis of a subspace P, the properties in this case  are: : The  coefficients _α_ **Analysis Formula** are obtained for any _k_ 

vector  of the  subspace P : **y** _α_ **x**[(] _[k]_[)] _k_ = ⟨ , **y** ⟩ _K_ = **x**[(] _[k]_[)] **Parseval Identity:** ∥ **y** ∥[2] | ⟨ , **y** ⟩ |[2] ∑ _k_ =1 exprime  the  energy conservation 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Properties of orthonormal basis** 

**Best approximation:** P (K dimensions) is  a subspace of V (N dimensions), we try to approximate  a vector **y** ∈ _V_ with a linear comb. of vector of the subspace P. We need to define the best linear approximation **y** ∈ _P_ of  a vector ∈ _V_ that minimise the  norm −̂ . This  best **y** ∥ **y y** ∥ approximation is obtained  projecting **y** onto the orthonormal basis of P as: _K_ **y** = _αk_ ⋅ **x**[(] _[k]_[)] ∑ _k_ =1 ●The error **d** = −̂ **y y** is orthogonal to the  approximation **y** ●The approximation minimize the  square norm of **d** 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Finite Euclidian Spaces** 

**==> picture [796 x 297] intentionally omitted <==**

if  we  arrange  a transformation matrix M (NxN) w[(] _[k]_[)] we containing  at  each  line k the n line vector  ( _n_[)*] _α_ could  compute  the  vector  with analysis formula: _α_ = _My_ Inversely  we  could  retrive  the y signal using the synthesis  formula: _M_[−1] _α_ = _M[H] α_ = _y_ 

MA-StatDig Lecture2 v1.0 15.02.2022 

|— MASTERIN ENGINEERING OF SCIENCE **Application on signal representation** The set of real signals of the form _T_ x = _x x x_ 1 _,_ 2 _, . . . , N_ ⇥ _R[N]_ that forms a N-dimensional vector space       that is spanned by the basis vectors: 

**==> picture [335 x 127] intentionally omitted <==**

Canonical Base defines   an Hilbert space 

u = 0 0 _N_ [0 _, , , . . . ,_ 1] _[T]_ 

_T_ v = _v v v_ any vector                                     in       may 1 _,_ 2 _, . . . , N_ ⇥ _R[N] N_ decomposed: v = _v_ u _i i i_ =1 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Symmetric and Hermitian** 

## **matrix** 

For a square matrix **A** if the matrix is equal its transpose: 

A = A _[T]_ 

## then **A** is said to be _symmetric_ . 

For the  complex matrices the _Hermitian transpose_ **A** : is the complex conjugate of the transpose of 

A _[H]_ A _[∗]_ A _[T]_ = ( ) _[T]_ = ( ) _[∗]_ **A** is said _Hermitian_ A = A _[H]_ If a square matrix                  , 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Property of Hermitian** 

## **transpose** 

A few property of the Hermitian transpose  are: 

> 1. = (A _[H]_ ) _[H]_ A 

> 2. = A B A _[H]_ B _[H]_ + + ( ) _[H]_ = 3.  ( **AB** ) _[H]_ **B** _[H]_ **A** _[H]_ 

The same property for the transpose may be obtained by replacing H with T. 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Rank of the Matrix** 

Let be **A** an n x m matrix with m columns  we can partition as: 

**==> picture [493 x 49] intentionally omitted <==**

A The rank of **A** ,         is defined to be the number _ρ_ ( ) **A** . of linearly independent columns in 

- The rank of A is equal to the rank of is Hemitian 

- transpose. A A _[H]_ 

- _ρ_ ( ) = _ρ_ ( ) 

- We can do the same with the  rows  and we can A 

- say:        is defined to be the number of linearly _ρ_ ( ) **A** . 

- independent rows in 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Inverse  matrix** 

Then we can give the useful property: A AA _[H]_ A _[H]_ A _ρ_ ( ) = _ρ_ ( ) = _ρ_ ( ) 

If **A** is  an _n x m_ matrix then the rank of **A** : 

- _ρ_ (A) _≤ min_ ( _m, n_ ) 

- If **A** is a _nxm_ matrix and                                , then _ρ_ (A) = _min_ ( _m, n_ ) 

- **A** is  said _full rank_ . If **A** is square ( _n=m_ )  and full rank, then we have  a unique matrix called the _**inverse of A**_ such that: 

= A _[−]_[1] A = AA _[−]_[1] I 

1 0 0 _. . ._ 0  ⇥ 0 1 0 _. . ._ 0 I = ... ... ... ... 0 0 0 _. . ._ 1 ⇧⇧⇧⇤ ⌃⌃⌃⌅ 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Inverse matrix properties** 

If **A A** is said _invertible_ or . is full rank , _nonsingular_ If **A A** is said _noninvertible_ or is not full rank , _singular_ . And **A** does not have an inverse. If **A** and **B** are invertible then 

= AB B _[−]_[1] A _[−]_[1] ( ) _[−]_[1] The inverse of the Hermitian transpose: 

A _[H]_ A _[−]_[1] ( ) _[−]_[1] = ( ) _[H]_ 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Determinant** 

The  determinant  of  a 1x1 matrix      A = _a_ is 11 _{ }_ defined as                      . _det_ A _a_ 11 ( ) = The determinant of a (n x n) matrix is obtained recursively by a  matrix of (n-1)x(n-1). For any j: 

_det_ (A) = 

_n i_ =1 

_−_ ( 1) _[i]_[+] _[j] aijdet_ (A _ij_ ) 

A _ij_ where         is the  (n-1)x(n-1) matrix formed by deleting   the **i** row  and the **j** column of **A** . 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Exemple 2.3.4** 

**==> picture [891 x 405] intentionally omitted <==**

**----- Start of picture text -----**<br>
a a a<br>11 12 13<br> ⇥<br>A = a  = a a a<br>21 22 23<br> { ij}<br>a a a<br>31 32 33<br>⇤ ⌅<br>a a a a a a<br>22 23 21 23 21 22<br>−<br>det (A) =  a 11 det a 12 det +  a 13 det<br>a a a a a a<br>32 33 31 33 31 32<br>⇥ ⇥ ⇥<br>a a a a a a a a a a<br>33  − 23 32 21 33  − 23 31 21 32  − 22<br>] [ ] [<br>**----- End of picture text -----**<br>


_a a a a_ 22 33 _−_ 23 32 [ ] 

_a a a a_ 21 32 _−_ 22 31 [ ] 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Property of the determinant** 

# An (n x n) matrix **A** is invertible if  and only if : 

## _det_ (A) _̸_ = 0 

_det_ (AB) = _det_ (A) _det_ (B) _det_ (A _[T]_ ) = _det_ (A) _det_ ( _α_ A) = _α[n] det_ (A) 

_det_ (A _[−]_[1] ) = 

1 _det_ (A) 

**==> picture [260 x 110] intentionally omitted <==**

**----- Start of picture text -----**<br>
n<br>tr A a<br>ii<br>( ) =<br>i =1<br>**----- End of picture text -----**<br>


MA-StatDig Lecture2 v1.0 15.02.2022 

## **Linear equations** 

# Consider the  system of n equation and m unknowns: 

= a11 x1 + a12 x2 + . . . + a1 _m_ x _m_ b1 = a21 x1 + a22 x2 + . . . + a2 _m_ x _m_ b2 ... 

= a _n_ 1 x1 + a _n_ 2 x2 + . . . + a _nm_ x _m_ b _m_ 

## We can write the system  as: 

Ax = b 

Where **x** is the m-dimension vector containing the _unknowns_ , and **b** a n-dimension vector containing the bi. 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Square Matrix m=n** 

It could be written vector **b** as  a linear combination of the  column vectors **ai** of **A** : 

**==> picture [178 x 93] intentionally omitted <==**

A _[−]_[1] If A is nonsingular then        exist and  it  is  an uniquely solution defined by: 

x = A _[−]_[1] b 

If **A** is  singular  then          do not exist and they may be A _[−]_[1] either _no solution_ (inconsistent) or _many solutions_ . 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Homogeneous  solution** 

In the case of singular **A** the columns of **A** are linearly dependent and there exist  nonzero solution to  homogeneous equations: Az = 0 = _k n −_ A There will                            linearly independent solutions to _ρ_ ( ) the homogeneous equations. 

x **Ax = b** There is at least one vector      that solve the system 0 , then any vector of the form, 

x = x0 + _α_ 1z1 + _. . ._ + _αk_ z _k_ z will also be a solution where the     are linearly independent _i_ solution of the homogeneous equation 

Az = 0 

MA-StatDig Lecture2 v1.0 15.02.2022 

**==> picture [905 x 689] intentionally omitted <==**

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Rectangular Matrix n<m Underdetermined** 

If n<m there are fewer equations than unknowns, if the system is not inconsistent there  are many vectors **x** that satisfy the equations. One method is often used to define a unique solution is to find the vector that satisfy: 

_min_ x such that Ax = b _∥ ∥_ If the rank of **A** is n (n rows linearly independent) then the nxn matrix            is invertible and  the AA _[H] minimum norm  solution_ is: 

= x A _[H]_ AA _[H]_ b 0 ( ) _[−]_[1] The  matrix        is called A[+] pseudo inverse of the matrix **A** 

= A[+] A _[H]_ AA _[H]_ ( ) _[−]_[1] 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Exemple 2.3.6** 

## Consider the system: 

_x x x x_ = 1 1 _−_ 2 + 3 _−_ 4 

> In the matrix  form: Ax _−_ 1 1 _−_ x = b = [1 _, , ,_ 1] 

> where             and b = 1 **x** contains the unknown. If  we apply the previous relation: 

x = A _[H]_ AA _[H]_ b AA _[H]_ = 4 ( ) _[−]_[1] 

Then the minimum norm solution is: 

1  _−_ ⇥ 1 x =[1] 1 4 _−_ 1 ⇧⇧⇤ ⌃⌃⌅ 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Exemple** 

## If  we  have one more equation: 

**==> picture [467 x 61] intentionally omitted <==**

## Then the matrix **A** and the vector **b** : 

**==> picture [817 x 96] intentionally omitted <==**

## Then the minimum L2 norm solution is now: 

**==> picture [714 x 192] intentionally omitted <==**

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Rectangular matrix: m<n Over determined** 

- If m<n there are more  equations than unknowns, and in no solutions exists. 

- genera In this case the system is _inconsistent_ and the solution _overdetermined_ : 

**Geometrical exemple:** In a 3 dimensional vector space we have 2 vectors, say **a1** and **a2** included in a plane  and  a third vector **b** outside the plane. The problem is : How  to compose (linearly)  the vectors **a1** and **a2** to obtain the best approximation **b[^]** with the **e** b minimum error | |. e a1 ˆb a2 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Geometrical exemple** 

> Ll **b^** as: We can exprime the best approximation of _m_ ˆb = _x_ a **Ax** = **b[ˆ] A** _i i_ or, with, _i_ =1 

**A a a** = [ **1** _,_ **2** ] 

we can write the norm of the error e: 

**==> picture [324 x 46] intentionally omitted <==**

From the previous drawing we  can write: 

**==> picture [209 x 29] intentionally omitted <==**

In order to obtain the minimum error norm the vector **e** must be orthogonal to **a1** and **a2** (columns of **A** ) then: A _[H]_ e = 0 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Geometrical exemple** 

## Which could be written: 

A _[H]_ e = A _[H]_ b _−_ A _[H]_ Ax = 0 

A _[H]_ Ax = A _[H]_ b Which is known  as _normal equation_ . If **A[H] A** is full rank the  we : can solve the equation and find the _least squares solution_ x A _[H]_ A A _[H]_ b 0 = ( ) _[−]_[1] = x A[+] b 0 

Where        is the pseudo-inverse of the matrix A[+] **A** for the overdetermined problem. 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Projection matrix** 

ˆb Thes best approximation    is given by  the projection of vector **b** onto the subspace spanned  by **a1** and **a2** . ˆb = Ax = A A[H] A A[H] b 0 ( ) _[−]_[1] 

## ˆb = P b A 

P is called A _projection matrix_ . Finally using the _orthogonality condition_ we find the _minimum last square error_ : 

_min_ e = b[H] e = b[H] b _−_ b[H] Ax 0 _⇥ ⇥_[2] 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Example 2.3.7** 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Example ellipses** 

Soit un nuage de points  que l’on veut approcher par une courbe elliptique. L’équation générale d’une conique  centrée est: _ax_[2] + + _cx_ + + = 1 _by_[2] _dy exy_ 

on peut écrire cette equation pour chaque point _P x_ , les paramètres a,b,c,d,e sont à trouver ( _i, yi_ ) Si on écrit le vecteur des paramètres  comme: ⇥= [ _a, b, c, d, e_ ] _[T]_ = **A⇥ b** et le système des équations: avec:                                      et _A x_[2] **b** 1 _· · ·_ = [1 _, ,_ ] _[T]_ = [ _i[, y] i_[2] _[, x][i][, y][i][, x][i][y][i]_[]] Le vecteur aux sens des moindres carrés **⇥ A[T] A A[T] b 0** = ( ) _[−]_ **[1]** 

MA-StatDig Lecture2 v1.0 15.02.2022 

## Paramètres  de l’ellipse sans le bruit 

**==> picture [288 x 216] intentionally omitted <==**

**----- Start of picture text -----**<br>
0 . 0199<br>2 3<br>0 . 0574<br>−<br>⇥= 0 . 0171<br>−<br>0 . 0120<br>−<br>0 . 0454<br>66664 77775<br>**----- End of picture text -----**<br>


## Paramètres  avec  le bruit comme sur figure 

0 _._ 0195 2 3 0 _._ 0559 _−_ = ⇥ 0 _._ 0169 _N −_ 0 _._ 0113 _−_ 0 _._ 0440 66664 77775 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Exemple de-bruitage signal** 

Un signal mesuré x[n] avec N = 100000 éch. (fichier Regression1.mat) 

Ce  signal contient un sinus  déphasé avec F1 = 12 Hz et A1 = 10mV ainsi que un drift linéaire et un offset. Ce  signal est fortement bruité. 

Trouver la meilleure  approximation  du sinus  déphasé utilisant  les moindres  carrées. 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Eigen Values and Eigen Vectors** 

Eigen values and Eigen Vectors provides important informations about  the matrix. Let a  square matrix **A** of dimension _n x n_ and consider  a set of linear equations: 

Av = _λ_ v 

> Where       is a constant . We may equivalently  be expressed _λ_ as a system of homogeneous linear equations of the  form: A _− λ_ I v = 0 ( ) 

v In order to have nonzero vector     as solution it is necessary for the matrix                to be singular.(A _− λ_ I) 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Find  Eigenvalues** 

_λ_ A _− λ_ I The determinant        of                is a n order _p_ ( ) ( ) _λ_ polynomial in   . This  polynomial is called the _λ_ of **A** and  the n roots _i characteristic polynomial_ are the _eigenvalues_ of **A** . 

_λ det_ A _− λ_ I _p_ ( ) = ( ) = 0 

A _− λ_ I For each eigenvalues     the matrix                   will be singular _λi_ ( _i_ ) v _i_ and at least one nonzero vector      that solve the equation : = Av _λ_ v _i i i_ These vectors     are called  v of **A** _i eigenvectors_ 

v v v **Property 1** : The nonzero eigenvectors                            corre-1 _,_ 2 _, . . . n λ_ sponds to distinct eigenvalues                          are linearly 1 _, λ_ 2 _, . . . λn_ independent. 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Exemple 2.3.8** 

Eigenvalues and eigenvector  of  2x2 symmetric matrix. 

**==> picture [981 x 526] intentionally omitted <==**

**==> picture [191 x 25] intentionally omitted <==**

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Exemple 2.3.8** 

- v _α_ v 1 1 

- If     is a  Eigen vector  then        is  also an eigenvector, in 

- general we normalize the norm of the eigenvector to one: 

**==> picture [129 x 35] intentionally omitted <==**

**A** are: In our case, the normalized  values of 

**==> picture [670 x 96] intentionally omitted <==**

In general eigenvectors  are linearly independent and in this exemple  they are orthonormal. 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Singular matrix and eigenvalues** 

If A is an **n x n** singular matrix, then there  are nonzero solutions to the homogeneous equation: 

Av = 0 i 

> and             is an eigenvalue of _λ_ = 0 **A** . Furthermore if  rank of = **A** is           then there will be                           linearly _ρ_ (A) _k n − ρ_ (A) independent solutions to the previous equation. There it follows that **A** will have          nonzero A _ρ_ ( ) = _k n −_ A 

> eigenvalues and                           eigenvalues that are _ρ_ ( ) equal to zero. 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Property related to eigenvalues and eigenvectors** 

2.The eigenvalues of a Hermitian matrix are real. 3.A Hermitian matrix is positive definite, **A** >0, if and only if the eigenvalues of **A** are positive. 

4.Determinant of  a matrix is related to eigenvalues as _n det_ A _λ_ ( ) = _i i_ =1 

5.The eigenvectors of a Hermitian matrix corresponding to distinct eigenvalues are = _λ λ_ v v = 0 orthogonal.              then _i j ⟨ i, j⇥_ 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Eigenvalues decomposition** 

For any **n x n** matrix **A** having a set of **n** linearly independent _eigenvectors_ we may perform an _eigenvalue_ **A** as : _decomposition_ that express 

A = VΛV _[−]_[1] 

where **V** is a matrix that contains eigenvectors of **A** and     is  Λ a diagonal matrix that contain the eigenvalues. 

v Λ = _λ_ n]] _diag{_ 1 _, λ_ 2 _, . . . , λn}_ = Av _λ_ v _k_ = 1 2 _k k k_ ; _, , . . . , n_ 

V v v v = [ 1 _,_ 2 _, . . . ,_ n]] Demonstration: 

A v v v v _λ_ v _λ_ v _λ_ [ 1 _,_ 2 _, . . . ,_ n] = [ 1 1 _,_ 2 2 _, . . . ,_ n n] 

AV = VΛ 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Spectral Theorem** 

For a Hermitian matrix, the harmonic decomposition assumes a special form. For a Hermitian matrix we can always find  a set of orthonormal eigenvectors. Therefore, if **A** is Hermitian, then **V** is unitary  and  the eigenvalue decomposition  becomes : 

_n_ = A = VΛV[H] _λ_ v v _[H] i i i i_ =1 

. **Spectral Theorem** Any Hermitian matrix A may be decomposed as: 

= A = VΛV[H] _λ_ v v _[H]_ 1 1 1[+] _[ λ]_[2][v][2][v] 2 _[H]_[+] _[ . . .]_[ +] _[ λ][n]_[v] _[n]_[v] _n[H] λ_ **A** and     are a set of v where       are eigenvalues of _i i_ **orthonormal** eigenvectors. 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Inversion with spectral theorem** 

Suppose that **A** is nonsingular Hermitian matrix, then: 

**==> picture [738 x 36] intentionally omitted <==**

_n_ 1 v v _[H] i i λ i i_ =1 

The invertibility of **A** guarantees that              so the _λi_ = 0 sum is well defined. 

In many signal processing the matrix **B** is singular or ill conditioned. In this case  we can stabilize the problem by adding a constant to each term of the diagonal. 

A = B + _α_ I 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **ill conditioned matrix** 

**inversion** The  effect to add  a constant of each term of the diagonal of  the matrix is the leave the eigenvector of **B** _λ_ unchanged while changing the eigenvalues from      to _k ⇥ α k_ + = Av Bv _α_ v _⇥ α_ v k k + _k k_ + _k_ = ( ) 

Property 5 : Let **B** be an n x n matrix with eigenvalues and let **A** be a matrix that is related to **B** as follows _λ i_ A = B + _α_ I then A and B have the same eigenvectors and the 

_⇥ α i_ + 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Exemple 2.3.9** 

Let be **A** an n x n Hermitian matrix of the form... and **B** is a noninvertible Hermitian matrix of rank one: A = B + _α_ I since B has a rank of one , it is only one nonzero eigenvalue then we can write: B = _λ_ u u _[H]_ 1 1 

u with      a unit norm vector, and  1 _λ ̸_ = 0 = Bu _λ_ u u _[H]_ 1 1[=] _[ λ]_[u][1][(][u] _[H]_ ( 1[)][u][1] 1[u][1][) =] _[ λ]_[u][1] u **B** we see that      is an eigenvector of 1 with eigenvalue _λ_ This vector is also eigenvector of A with eigenvalue _⇥_ + _α_ Using the spectral theorem: 

**==> picture [494 x 94] intentionally omitted <==**

**----- Start of picture text -----**<br>
n<br>1 1<br>=<br>A [−] [1]<br>1 [+] i<br>α  +  ⇥ [u][1][u] [H] α [v] [i] [v] [H]<br>i =2<br>**----- End of picture text -----**<br>


MA-StatDig Lecture2 v1.0 15.02.2022 

## **Exemple 2.3.9** 

**==> picture [841 x 194] intentionally omitted <==**

_i_ =1 we can write the second term of the previous equation: 

**==> picture [406 x 94] intentionally omitted <==**

## and finally the inverse of **A** becomes: 

1 _⇥_ = A _[−]_[1][1][1] 1[+] 1[=] 1 _α_ + _⇥_[u][1][u] _[H] α_[I] _[ −] α_[1][u][1][u] _[H] α_[I] _[ −] α α_ + _⇥_ ( )[u][1][u] _[H]_ 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Application** 

It will be useful in the development of adaptive filtering algorithms to be able to characterize the geometry of the surface described by the equation, where **A** is symmetric and positive definite **[[T]]** 

**x[[T]] Ax** = **1** 

With a change of variables (rotate the coordinate system, so it is aligned with the eigenvectors) **[[T]][[T]]** 

**x[[T]] V⇤V[[T]] x** = **1** ( ) 

This can be written as which is an ellipse in n dimensions that is centered at the origin yy vi x 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Application** 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Exercises** 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Exercises** 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Solution** 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Exercise** 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Solution** 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Exercise** 

MA-StatDig Lecture2 v1.0 

15.02.2022 

## **Solution** 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Exercise** 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Solution** 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Solution** 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Exercise** 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Solution** 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Exercise** 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **Solution** 

MA-StatDig Lecture2 v1.0 15.02.2022 

## **References** 

## Matrix Analysis and Applied Linear Algebra Carl D. Meyer SIAM 

MA-StatDig Lecture2 v1.0 

15.02.2022 

