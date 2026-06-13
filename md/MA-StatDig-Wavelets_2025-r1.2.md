## **Wavelets** 

# Wavelet Processing 

Fourier orthonormal basis 

- Compact support orthonormal basis: Haar 

- functions 

 Wavelet theory. 

 Fast Wavelet transform 

MA-StatDig Wavelets v1.2 

24.03.2025 

**Basis** M— — MASTER OF SCIENCE | IN ENGINEERING **Synthesis Formula** The set of K vectors _W_ = { **x**[(] _[K]_[)] } _k_ =1⋯ _K_ from a subspace P is a base of  this  subspace if : ● The set W is linearly independent ● The span covers completely P: span{W}=P and  we can write for ∈ _P_ could be written as  a linear combination  of **x**[(] _[K]_[)] any **y** { } _k_ =1⋯ _K K_ **y** = _α_ **x**[(] _[K]_[)] _k_ ∑ _k_ =1 Orthogonal and orthonormal basis: in this case the set _W_ = { **x**[(] _[K]_[)] } _k_ =1⋯ _K_ we have the constraint: **x**[(] _[i]_[)] **x**[(] _[j]_[)] _δ i_ − ⟨ , ⟩= [ _j_ ] when i=j  the scalar product is equal1  otherwise  is equal 0. A set of N orthogonal vectors  in a N dimension space is  a base of this space. 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Properties of orthonormal basis** 

 _W_ = { **x**[(] _[K]_[)] } _k_ =1⋯ _K_ is  an orthonormal basis of a subspace P, the properties in this case  are:  : The  coefficients _α_ **Analysis Formula** are obtained for any _k_ vector  of the  subspace P : **y** 

_α_ **x**[(] _[k]_[)] _k_ = ⟨ , **y** ⟩ _K_ = **x**[(] _[k]_[)] ∥ **y** ∥[2] | ⟨ , **y** ⟩ |[2]  **[Parseval Identity: ]** ∑ _k_ =1 

exprime  the  energy conservation 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Properties of orthonormal basis** 

 **Best approximation:** P (K dimensions) is  a subspace of V (N dimensions), we try to approximate  a vector **y** ∈ _V_ with a linear comb. of vector of the subspace P. We need to define the best linear approximation **y** ∈ _P_ of  a vector ∈ _V_ that minimise the  norm −̂ . This  best **y** ∥ **y y** ∥ approximation is obtained  projecting **y** onto the orthonormal basis of P as: _K_ **y** = _αk_ ⋅ **x**[(] _[k]_[)] ∑ _k_ =1 ●The error **d** = −̂ **y y** is orthogonal to the  approximation **y** ●The approximation minimize the  square norm of **d** 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Finite Euclidian Spaces** 

**==> picture [823 x 297] intentionally omitted <==**

 if  we  arrange  a transformation matrix M (NxN) **w**[(] _[k]_[)] we containing  at  each  line k the n line vector  ( _n_[)*] _α_ could  compute  the  vector  with analysis formula: _α_ = _My_ 

Inversely  we  could  retrieve  the y signal using the synthesis  formula: _M_[−1] _α_ = _M[H] α_ = _y_ 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Limitations of Fourier Basis** 

- Fourier Basis is  a infinite support orthonormal basis. ● Adapted  for infinite duration signals or periodic signals 

- ● In case of discontinuity of the  signal, Gibs phenomena. 

- Due to the infinite support of Fourier transforms basis, each one with a fix frequency we lose the time. ● after the transformation we lose the time at which this frequency appear into the signal. 

   - If we cut the signal in several sequences (periodogram) the product between the sequences duration and the frequency  resolution  of the  spectrum  is a constant value. 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Compact support orthonormal basis** 

 The wavelets are a family of orthonormal functions with finite duration (compact support). 

- Example of the Haar wavelets: 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Haar wavelet transform** 

##  To illustrate the transform we take a  finite sampled signal of N = 8 samples: 

## Scale coefficients: 

## Detail coefficients: 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Reconstruction** 

##  From the detail coeff. dj[k] and scale coeff. aj[k] we 

reconstruct the initial signal x(t). 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Multiresolution** 

 In order to represents the details (fastest variations) to the  slowest characteristics of the signal  we use the multi resolution. 

 After  the first step of the decomposition from a signal x(t) or  a sampled signal x[n] with N samples we obtain set of coefficients aj[k] and dj[k] with N/2 values each. 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Recursive Multiresolution** 

- For the next step we consider the coefficient aj[k] as a new signal with N/2 samples. 

- We compute  a new set of  coefficients a(j-1)[k]  and d(j-1)[k] decomposing the “signal” aj[k] with  the scale  function  and the wavelet function: 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Compute wavelet coeff. without wavelet** 

- The previous algorithm is in fact a composition of  the discrete convolution and the decimation. 

- Two FIR filter are used each one with his impulse response. 

   - A low pass filter H with  the  impulse response h[n] derived from the scale function phi. 

   - An high pass filter G with the impulse response g[n] derived  from the wavelet function psi. 

   - Those 2 filters  have particular properties (quadrature filters) ans they  are related  with  the wavelets function as: 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Fast Wavelet Transform** 

## **FWT** 

- The computation of  the Wavelet coefficients aj[k] and dj[k] for  every  stage J are computed by FWT: 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Backward Wavelet Transform** 

 The backward wavelet transform reconstruct the signal f[n] from the coefficients dj[n] using each scale j from 0 where  a0  is a single real constant.  The recursive algorithm from scale j to scale j+1 uses  upsample by 2 and FIR  filter with impulse ¯ ¯ _h n h n_ and _n n_ . responses [ ] = [− ] _g_ [ ] = _g_ [− ] 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Backward Wavelet Transform** 

## Functional diagram: 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Other  wavelets** 

## **functions** 

- Daubechies wavelets is a generalisation of the Haar wavelets, by using longer filters impulse response, producing smother scale function  and wavelets . _ϕ ψ_ 

- Larger number  of coefficients p=2M of the filter , the higher is the number M of vanishing moments. ● Choosing the best wavelet, and thus choosing M, adapted to given  class of signals. 

   1. The filter with M=1 vanishing moments correspond to the Haar filter. 

   2. The filter with M=2  vanishing moments  corresponds to the famous D4 wavelets , which compresses perfectly linear signals 

   3. The filter with M=3 vanishing moments  compresses perfectly quadratic signals. 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Applications** 

- The first application is the compression of signals or images: 

   - After FWT we conserve only the coefficients  of  each scale j  greater  than a threshold |dj| > Th anew pu the other to 0. 

   - During the reconstruction with backward transform  we reconstitue an approximation of the original signal and the error is greater  if Th is greater. 

   - Another  method is  to use only a part of the scales from 0 to J_max. 

- Today the main use is for the images with 2D FWT, and  the JPEG 2000  compression use it. 

MA-StatDig Wavelets v1.2 24.03.2025 

## **Applications** 

- Another  application is the de-noising of  signals or images : 

   - Depending of the nature of the noise  we could conserve  only  a part of the dj coefficients. For exemple to suppress  HF noise  we could use only dj coefficients with j< J_max. 

   - Some wavelets  functions  are  able to suppress constants (offsets) , or   polynomial with degree k (moments) , for  example  linear trends…. 

MA-StatDig Wavelets v1.2 24.03.2025 

