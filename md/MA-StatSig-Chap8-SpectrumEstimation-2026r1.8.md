## **Spectrum estimation Statistical Signal Processing and Modelling** 

Lavanchy David (HEIG-VD) Tognolini Maurizio (HEIG-VD) 

1 

TStatDig-SpectrumEstimation-v1.8 01.06.2026 

## **Introduction** 

## ● There are 2 main ways to estimate the spectrum of a process 

**==> picture [179 x 19] intentionally omitted <==**

**----- Start of picture text -----**<br>
Non-Parametric<br>**----- End of picture text -----**<br>


**==> picture [126 x 18] intentionally omitted <==**

**----- Start of picture text -----**<br>
Parametric<br>**----- End of picture text -----**<br>


2026/Statistical Signal Processing and Modeling 

2 

## **Introduction** 

## ● The parametric method is using the signal modeling technics: 

**==> picture [660 x 260] intentionally omitted <==**

**----- Start of picture text -----**<br>
𝑥𝑥[𝑛𝑛] Signal  𝑞𝑞<br>∑ 𝑏𝑏 [ 𝑘𝑘𝑧𝑧 | [−𝑘𝑘]<br>𝑘𝑘=0<br>modeling  𝑋𝑋 𝑧𝑧= 𝑝𝑝<br>1 + ∑ 𝑎𝑎 [ 𝑘𝑘𝑧𝑧 | [−𝑘𝑘]<br>(AR / MA / ARMA) 𝑘𝑘=1<br>𝑧𝑧= 𝑒𝑒 [𝑗]<br>\<br>𝑞𝑞<br>∑ 𝑏𝑏 𝑘𝑘𝑒𝑒 [−𝑗𝑗𝑘𝑘𝑗𝑗2]<br>𝑘𝑘=0<br>=<br>P<br>𝑒𝑒 [𝑗]<br>𝑥𝑥<br>𝑝𝑝<br>1 + ∑ 𝑎𝑎 𝑘𝑘𝑒𝑒 [−𝑗𝑗𝑘𝑘𝑗𝑗2]<br>𝑘𝑘=1<br>**----- End of picture text -----**<br>


- Can integrate process information 

- Better to reject noise if process can be estimated 

- Various method to modelize (AR/MA/ARMA) 

- Not generic approach 

   - For example, AR model is not good to estimate MA process 

**==> picture [399 x 62] intentionally omitted <==**

**----- Start of picture text -----**<br>
4<br>— ,<br>2026/Statistical Signal Processing and Modeling    oO 0.1 0.2 0.3 0.4 0.5 0.6 O.7<br>**----- End of picture text -----**<br>


**==> picture [14 x 18] intentionally omitted <==**

**----- Start of picture text -----**<br>
3<br>**----- End of picture text -----**<br>


## **Introduction** 

## ● The non-parametric method is using Fourier and/or autocorrelation: 

**==> picture [921 x 313] intentionally omitted <==**

**----- Start of picture text -----**<br>
Auto-<br>𝑟𝑟 [k]<br>𝑋𝑋<br>𝑥𝑥[𝑛𝑛]<br>4 THANE ip Wi } Ae nit i bi Wh Y ,{! vt | it ‘WP vty 1 hy i! ye correlation | ‘Y we \ "Hl Wc]<br>-400 y_,<br>-30 -20 -10 0 10 20<br>0 50 100 150 200 250<br>• | \<br>Generic approach<br>•<br>Estimating the power spectrum is  Fourier Fourier<br>equivalent to estimate the autocorrelation<br>2<br>•<br>Easy to compute but limited to produce  𝑋𝑋 𝑓𝑓<br>= 𝑃𝑃<br>𝑃𝑃 𝑥𝑥<br>𝑥𝑥<br>accurate power spectrum, especially for  𝑁𝑁<br>**----- End of picture text -----**<br>


- Easy to compute but limited to produce accurate power spectrum, especially for short data records. 

- Various methods : 

   - periodogram, modified periodogram, Barlett’s, Welch’s, Blackman-Tukey 

2026/Statistical Signal Processing and Modeling 

4 

## **Introduction** 

- 𝑉𝑉[2] 

- ● The **Power Spectrum Density (PSD)** is in of a signal in [𝑉𝑉] . 𝐻 

- ~~a~~ 

- ● and with to It has to be integrated between 2 frequencies 𝑓𝑓1 𝑓𝑓2 𝑓𝑓1 < 𝑓𝑓2 get an estimate of the signal’s power between these 2 frequencies. 

- ● The power spectrum density is defined by: 

**==> picture [323 x 92] intentionally omitted <==**

Where 𝑟𝑟𝑥 [𝑘𝑘] is the autocorrelation function defined as: 𝑟𝑟𝑥 [] 𝑘𝑘= 𝐸𝐸 {1 𝑥𝑥 𝑙𝑙𝑥𝑥[𝑙𝑙+ 𝑘𝑘] ; ● Problem of estimating PSD is equivalent to estimate autocorrelation. Estimation could be biased when the data record is short. 

2026/Statistical Signal Processing and Modeling 

5 

## **Introduction** 

● has a It is well known that a signal with amplitude 𝐴𝐴[𝑉𝑉] **power** 𝐴𝐴[2] of 4[[𝑉𝑉][2][]][ in bilateral spectrum. Let’s see.] 

25  Noisy sinus A= 5V → Power = 4[= 6.25 𝑉𝑉][2] 

 T=37s, F0=1/T=0.027Hz,  Fs = 1 Hz, Nfft = 512, df = 0.002 Hz **Signal PSD** 

**==> picture [786 x 309] intentionally omitted <==**

**----- Start of picture text -----**<br>
!!<br>Gol | > 1600<br>1400<br>1400<br>1200<br>1200<br>_<br>2 1000 | z rons<br>oa<br>600 600<br>400 400<br>200 200 X 0.0234375 a<br>;<br>0.005 0.01 0.015 0.02 0.025 0.03 0.035<br>OO ¥ 14.1406 | \ ¥ 13.4174<br>150 200 250 f[Hz] f[Hz]<br>t [s]<br>2<br>𝑁𝑁−1 0.03<br>1<br>= 𝑘𝑘<br>𝑥𝑥 𝑛𝑛 𝑥𝑥 𝑘𝑘𝑒𝑒 [−𝑗] 𝑓𝑓⋅𝑑𝑑𝑓𝑓≈6.1<br>𝑁𝑁<br>𝑘𝑘=0<br>𝑓𝑓=0.02<br>**----- End of picture text -----**<br>


2026/Statistical Signal Processing and Modeling 

## **Normalization** 

## ● Be careful, the psd is changing in function of the frequency 

domain representation. 

_This signal is a cosinus of 100Hz with a normalized gaussian noise_ 

2026/Statistical Signal Processing and Modeling 

7 

## **Normalization** 

● There are three frequencies domain to show the power spectrum density. But the total power is the same. 

**==> picture [331 x 492] intentionally omitted <==**

𝑑𝑑𝐹𝐹= 1/𝑁𝑁 

𝑑𝑑𝜔𝜔= 2𝜋𝜋/𝑁𝑁 𝑑𝑑𝑓𝑓= 𝐹 /𝑁𝑁 

2026/Statistical Signal Processing and Modeling 

8 

## **Normalization** 

## ● The frequency sampling can as well change the power spectrum density without normalization 

**==> picture [798 x 80] intentionally omitted <==**

**----- Start of picture text -----**<br>
∞ ∞<br>1<br>𝑘𝑘 𝑘𝑘<br>𝑃𝑃𝑥 𝑓𝑓= 𝑟𝑟𝑥 [𝑘𝑘] 𝑒𝑒 [−𝑗] 𝑃𝑃𝑥 𝑓𝑓= 𝑟𝑟𝑥 [𝑘𝑘] 𝑒𝑒 [−𝑗]<br>𝐹<br>𝑘𝑘=−∞ 𝑘𝑘=−∞<br>**----- End of picture text -----**<br>


2026/Statistical Signal Processing and Modeling 

9 

## **Periodogram** 

## ● **Periodogram** is the simplest estimator of the PSD: 

**==> picture [863 x 99] intentionally omitted <==**

**----- Start of picture text -----**<br>
∞<br>𝑁𝑁−1<br>= 𝑘𝑘 = 𝑘𝑘<br>𝑃𝑃𝑥𝑥 𝑒𝑒 [𝑗] 𝑟𝑟𝑥 [𝑘𝑘] 𝑒𝑒 [−𝑗] 𝑝 𝑒𝑒 [𝑗] ̂𝑟𝑟𝑥 [𝑘𝑘] 𝑒𝑒 [−𝑗]<br>𝑘𝑘=−∞ 𝑘𝑘=−𝑁𝑁+1<br>**----- End of picture text -----**<br>


● Therefore, spectrum estimation is, in some sense, an autocorrelation estimation problem. 

2026/Statistical Signal Processing and Modeling 

10 

## **Periodogram** 

● As the signal 𝑥𝑥[𝑛𝑛] is limited, it can be seen as 𝑥𝑥 [𝑛𝑛] as the 𝑁𝑁 product of 𝑥𝑥[𝑛𝑛] with a rectangular window 𝑤𝑤 [𝑛𝑛] 𝑅𝑅 

> 𝑥𝑥 n] _ 𝑥𝑥[𝑛𝑛] 0 ≤𝑛𝑛< 𝑁𝑁 𝑁𝑁 0 𝑜 𝑜𝑒𝑒𝑟𝑟𝑤𝑤𝑜𝑜𝐹𝐹𝑒𝑒 𝑥𝑥 𝑛𝑛= 𝑤𝑤 𝑛𝑛⋅𝑥𝑥[𝑛𝑛] 𝑁𝑁 𝑅𝑅 

## ● The estimated autocorrelation become : 

**==> picture [631 x 190] intentionally omitted <==**

2026/Statistical Signal Processing and Modeling 

11 

## **Periodogram** 

**==> picture [895 x 619] intentionally omitted <==**

12 

## **Periodogram example** 

- If 𝑥𝑥[𝑛𝑛] is white noise with a variance of 𝜎𝜎 , then rx k = 𝜎𝜎 𝛿𝛿[𝑘𝑘] and then the 𝑥𝑥[2] 𝑥𝑥[2] 

- power spectrum is a constant 

**==> picture [139 x 30] intentionally omitted <==**

- Next is showing one realization of noise N=32. 

 Estimated ̂𝑟𝑟 k | is not a 𝜎𝜎 𝛿𝛿[𝑘𝑘] 𝑥𝑥 𝑥𝑥[2] 

 𝑝 𝑒𝑒[𝑗] is approximately equal ) to 𝑃𝑃 (𝑒𝑒[𝑗] ) on the average 𝑥𝑥  Considerable variation in 𝑝 𝑒𝑒[𝑗] as 𝜔𝜔 varies. 

Let’s evaluate the performance of the periodogram! 

2026/Statistical Signal Processing and Modeling 

13 

## **Periodogram (performance)** 

- The unique parameter of the periodogram is N, the observation time. 

- Ideally, as N increase, the periodogram should converge to the power spectrum **(bias):** 

**==> picture [314 x 47] intentionally omitted <==**

- And the **variance** that goes to zero as the data record length goes to infinity 

**==> picture [295 x 46] intentionally omitted <==**

## ● In other words, 𝑃𝑃𝑝 𝑝𝑝 ( 𝑒𝑒[𝑗] ) must be **a consistent estimate** of the power spectrum. 

Let’s evaluate the Bias and Variance of the periodogram! 

2026/Statistical Signal Processing and Modeling 

14 

## **Periodogram (performance)** 

- 𝑥𝑥[𝑛𝑛] is white noise with a variance of 𝜎𝜎 = 4 𝑥𝑥[2] 

● Increasing N is making the average correct ( 𝐸𝐸 𝑃𝑃 𝑒𝑒[𝑗] ≈𝑃𝑃 (𝑒𝑒[𝑗] ) ) 𝑝 𝑝𝑝 𝑥𝑥 but the variance is still high 𝑉𝑉𝑎𝑎𝑟𝑟 𝑃𝑃 𝑒𝑒[𝑗] ≈𝑃𝑃 (𝑒𝑒[𝑗] ) ! 𝑝 𝑝𝑝 𝑥𝑥[2] 

- The variance is not as good as expected. 

**==> picture [59 x 19] intentionally omitted <==**

**----- Start of picture text -----**<br>
N=32<br>**----- End of picture text -----**<br>


**==> picture [99 x 19] intentionally omitted <==**

**----- Start of picture text -----**<br>
N=16384<br>**----- End of picture text -----**<br>


2026/Statistical Signal Processing and Modeling 

15 

## **Periodogram (Bias)** 

● Let’s evaluate the periodogram bias mathematically: 𝑁𝑁−1 𝑁𝑁−1 𝑘𝑘 = 𝑘𝑘 𝐸𝐸 𝑃𝑃 𝑒𝑒[𝑗] = 𝐸𝐸 ̂𝑟𝑟𝑥 [𝑘𝑘] 𝑒𝑒[−𝑗] 𝐸𝐸 ̂𝑟𝑟𝑥 [𝑘𝑘] 𝑒𝑒[−𝑗] 𝑝 𝑝𝑝 𝑘𝑘=−𝑁𝑁+1 𝑘𝑘=−𝑁𝑁+1 { ( ) > Sf 𝑁𝑁−1−𝑘𝑘 𝑁𝑁−1−𝑘𝑘 1 1 𝑁𝑁−𝑘𝑘 = = 𝐸𝐸 ̂𝑟𝑟𝑥 [𝑘𝑘] 𝐸𝐸 𝑥𝑥 𝑛𝑛+ 𝑘𝑘𝑥𝑥[∗] 𝑛𝑛 𝑟𝑟 [𝑘𝑘] = 𝑟𝑟 [𝑘𝑘] 𝑥𝑥 𝑥𝑥 ( } ~~-~~ ) (fF JIB ~~-~~ )> ~~—~~ 𝑁𝑁 𝑁𝑁 𝑁𝑁 𝑛𝑛=0 𝑛𝑛=0 𝑘𝑘= 0,1, … , 𝑁𝑁−1 ● So, it can be written: 𝐸𝐸 { ̂𝑟𝑟𝑥 [𝑘𝑘] 3 = 𝑤𝑤 [𝑘𝑘] ⋅𝑟𝑟 [𝑘𝑘] 𝐵𝐵 𝑥𝑥 𝑤𝑤 [𝑘𝑘] 𝐵𝐵 𝑁𝑁− 𝑘𝑘 Barlett 𝑘𝑘≤𝑁𝑁 Window 𝑤𝑤 𝐵𝐵 𝑁𝑁 0 k | 𝑘𝑘> 𝑁𝑁 + | ~~—~~ -N 0 N 

2026/Statistical Signal Processing and Modeling 

16 

## **Periodogram (Bias)** 

**==> picture [701 x 167] intentionally omitted <==**

**==> picture [304 x 143] intentionally omitted <==**

- Since the sinc-squared pulse converge to a Dirac as N goes to infinity, then the periodogram is asymptotically unbiased 

**==> picture [269 x 39] intentionally omitted <==**

2026/Statistical Signal Processing and Modeling 

17 

## **Periodogram (Bias)** 

- This implies that the periodogram of a pure sine wave, will not be an impulse but the Barlett window centered at the right frequency! 

_Higher is N, thinner is the main lobe and lower are the side lobes!_ 

2026/Statistical Signal Processing and Modeling 

18 

## **Periodogram (Resolution)** 

- Resolution of periodogram, is ability to resolve closely spaced narrowband components which is limited by the Barlett window. 

   - As the width of the main lobe increases when N decreases, there is a limit on how closely two sinusoids may be located. 

   - Defined as the bandwidth of the window as its half power points (-6dB) 

**==> picture [682 x 59] intentionally omitted <==**

Resolution too high! 

N=32 

2 sines waves w=[0.4π,0.45π] with random noise. Need resolution < 0.05 π ≈ 0.16 

N=128 

Resolution ok! 

2026/Statistical Signal Processing and Modeling 

## **Periodogram (variance)** 

● . As seen, the variance of the periodogram does not go to 0 when 𝑁𝑁→∞ 𝑉𝑉𝑎𝑎𝑟𝑟 𝑃𝑃 𝑒𝑒[𝑗] ≈𝑃𝑃 (𝑒𝑒[𝑗] ) 𝑝 𝑝𝑝 𝑥𝑥[2] 

- So, periodogram is **not a consistent estimate** of the power spectrum 

- Example: White Gaussian noise 𝜇𝜇= 0, 𝜎𝜎= 2 ⇒𝑃𝑃 = 𝜎𝜎[2] = 4 𝑥𝑥 

2026/Statistical Signal Processing and Modeling 

20 

## **Modified Periodogram** 

- Instead of using a rectangular window 𝑤𝑤 [𝑛𝑛] to 𝑥𝑥[𝑛𝑛] to make it finite 𝑅𝑅 

- length, we can use other kind of windows. 

- This change of windows gives us the possibility to smooth the periodogram: 

   - Rectangular window has a narrow main lobe compare to others windows 

   - Rectangular has large side lobes that may mask weak narrowband components 

**==> picture [912 x 315] intentionally omitted <==**

2026/Statistical Signal Processing and Modeling 

21 

## **Modified Periodogram** 

## ● The modified periodogram is simply to use a general window 𝑤𝑤 [| 𝑛𝑛. 

**==> picture [678 x 331] intentionally omitted <==**

**----- Start of picture text -----**<br>
∞ 2<br>1<br>= ⋅<br>𝑒𝑒 [𝑗] 𝑥𝑥 𝑛𝑛⋅𝑤𝑤 𝑛𝑛⋅𝑒𝑒 [−𝑗𝑗𝑛𝑛𝑗𝑗]<br>𝑁<br>) — ») rl 01<br>𝑛𝑛=−∞<br>| |<br>Normalization General window<br>𝑁𝑁−1 For a rectangular window:<br>1<br>𝑁𝑁= 𝑤𝑤 𝑛𝑛 2<br>𝑁𝑁= 1<br>i tl &<br>𝑁𝑁<br>𝑛𝑛=0<br>**----- End of picture text -----**<br>


2026/Statistical Signal Processing and Modeling 

22 

## ● Also asymptotically **unbiased** 

## **Modified Periodogram (performance)** 

**==> picture [468 x 60] intentionally omitted <==**

**==> picture [587 x 45] intentionally omitted <==**

● Modified periodogram is simply the periodogram of a window data sequence, the **variance** of 𝑃𝑃 𝑒𝑒[𝑗] will be approximately the same as 𝑀𝑀 ( ) periodogram: 𝑉𝑉𝑎𝑎𝑟𝑟 (( 𝑃𝑃𝑀𝑀 𝑒𝑒[𝑗] } ≈𝑃𝑃𝑥𝑥[2] ©) 𝑒𝑒[𝑗] 

2026/Statistical Signal Processing and Modeling 

23 

## **Windows** 

## ● Commonly used windows have a wider main lobes but smaller sidelobe 

2026/Statistical Signal Processing and Modeling 

24 

## **Modified Periodogram (example)** 

- Example of application: random process with 2 closes sinusoids (N=128) + sin 

- 𝑥𝑥 𝑛𝑛= 0.1 ⋅sin 𝑛𝑛𝜔𝜔1 + 𝜙𝜙1 𝑛𝑛𝜔𝜔2 + 𝜙𝜙2 + 𝑣𝑣 𝑛𝑛 𝜔𝜔1 = 0.2𝜋𝜋, 𝜔𝜔2 = 0.3𝜋𝜋 

2026/Statistical Signal Processing and Modeling 

25 

## **Barlett’s (Averaging)** 

- As seen, periodogram and modified periodogram are not consistent, ie variance does not go to 0 as 𝑁𝑁→∞. 

- Solution is the Barlett’s method. 

Segment a signal in K L. segments of length Where N = 𝐾𝐾⋅𝐿𝐿 

**==> picture [972 x 132] intentionally omitted <==**

**----- Start of picture text -----**<br>
One segment: Barlett (average of segment):<br>2 2<br>𝐿𝐿−1 𝐾𝐾−1 𝐾𝐾−1 𝐿𝐿−1<br>1 1 1<br>𝑖𝑖 𝑗 𝑛𝑛 = 𝑖𝑖 = 𝑛𝑛<br>𝑝 (𝑒𝑒 ) = 𝑥𝑥𝑖𝑖 𝑛𝑛𝑒𝑒 [−𝑗] 𝑒𝑒 [𝑗] 𝑝 𝑒𝑒 [𝑗] 𝑥𝑥 𝑛𝑛+ 𝑜𝑜⋅𝐿𝐿𝑒𝑒 [−𝑗]<br>𝐿𝐿 𝐾𝐾 𝑁𝑁<br>© y 𝑛𝑛=0 o fd) - 𝑖𝑖=0 E OC) - 𝑖𝑖=0 E[E 𝑛𝑛=0<br>**----- End of picture text -----**<br>


2026/Statistical Signal Processing and Modeling 

26 

## **Barlett’s (performance)** 

## ● It gives also an asymptotically unbiased estimate: 

**==> picture [399 x 37] intentionally omitted <==**

● = 0 But it gives a consistent estimator ( 𝐾𝐾→∞⇒𝑉𝑉𝑎𝑎𝑟𝑟 𝑃𝑃 𝑒𝑒[𝑗] ) { 𝐵𝐵 ( JJ 

**==> picture [327 x 65] intentionally omitted <==**

● However, the resolution increase because Barlett window is larger : 

**==> picture [184 x 69] intentionally omitted <==**

2026/Statistical Signal Processing and Modeling 

27 

## **Barlett’s (example)** 

● Example : random process of two sinusoids in unit variance noise (N=512) 

10 ⋅sin + sin 𝑥𝑥 𝑛𝑛= 𝑛𝑛𝜔𝜔1 + 𝜙𝜙1 𝑛𝑛𝜔𝜔2 + 𝜙𝜙2 + 𝑣𝑣 𝑛𝑛 𝜔𝜔1 = 0.2𝜋𝜋, 𝜔𝜔2 = 0.25𝜋𝜋 

2026/Statistical Signal Processing and Modeling 

28 

## **Welch’s (modified + overlap)** 

● In 1967, Welch proposed two modifications to Barlett’s method: 

1. Allow the sequences to overlap 

2. Allow data window 𝑤𝑤[𝑛𝑛] to be applied to each sequence (as modified periodograms) Overlay btw 

**==> picture [794 x 457] intentionally omitted <==**

**----- Start of picture text -----**<br>
Overlay btw<br>sequences: L-D<br>D(K-1) N<br>D<br>L L L L L<br>𝑥𝑥1[𝑛𝑛] 𝑥𝑥2[𝑛𝑛] 𝑥𝑥3[𝑛𝑛]<br>𝑁𝑁−𝐿𝐿<br>K is the number of sequence to cover all the signals:  [𝐾𝐾=] + 1<br>| 𝐷𝐷<br>𝑁𝑁−𝐿𝐿<br>D can be defined as a % of L (Ov : Overlay):  𝐾𝐾= [+ 1]<br>—— 𝐿𝐿(1 −𝑂𝑂𝑣𝑣)<br>𝐾𝐾−1<br>1<br>(𝑖𝑖)<br>=<br>Welch’s periodogram is simply :  𝑒𝑒 [𝑗] 𝑒𝑒 [𝑗]<br>𝐾𝐾<br>𝑖𝑖=0<br>**----- End of picture text -----**<br>


2026/Statistical Signal Processing and Modeling 

29 

## **Welch’s (performance)** 

## ● It gives also an asymptotically unbiased estimate: 

**==> picture [464 x 59] intentionally omitted <==**

- Variance is more difficult to compute since, with overlapping sequences, the modified periodograms **cannot be assumed to be uncorrelated** . With 50% overlap, the variance is approximately: 

**==> picture [443 x 109] intentionally omitted <==**

2026/Statistical Signal Processing and Modeling 

30 

## **Welch’s (example)** 

● 10 ⋅sin + sin 𝑥𝑥 𝑛𝑛= 𝑛𝑛𝜔𝜔1 + 𝜙𝜙1 𝑛𝑛𝜔𝜔2 + 𝜙𝜙2 + 𝑣𝑣 𝑛𝑛 

𝜔𝜔1 = 0.2𝜋𝜋, 𝜔𝜔2 = 0.25𝜋𝜋 

## **Periodogram** 

## **Welch** 

_Example826.mlx_ 

2026/Statistical Signal Processing and Modeling 

31 

## **Others non parametric method** 

● Blackman-Tukey Method 

 Window on the autocorrelation as the extreme autocorrelation values are noisy 𝑟𝑟 ( 𝑘𝑘 ) where | 𝑘𝑘≈𝑁𝑁 | 𝑥𝑥 

𝑀𝑀[) =] ̂𝑟𝑟 𝑘𝑘𝑤𝑤 𝑘𝑘𝑒𝑒[−𝑗𝑗𝑘𝑘𝑗𝑗] 𝐵𝐵[(𝑒𝑒][𝑗] 𝑥𝑥 »~ OC) 𝑘𝑘=−𝑀𝑀 

**==> picture [825 x 187] intentionally omitted <==**

**----- Start of picture text -----**<br>
tl. SN.<br>—it via<br>-M M<br>**----- End of picture text -----**<br>


2026/Statistical Signal Processing and Modeling 

32 

## **Others non parametric method** 

## ● Minimum Variance Spectrum Estimation 

 Design a bank of bandpass filter with a bandwidth ∆ and a center frequency 𝜔𝜔 and filter the signal with each filters. 𝑖𝑖 

𝐸𝐸 𝑦𝑦 𝑛𝑛 2 𝑖𝑖 𝑖𝑖 = 𝑒𝑒[𝑗] () ~~tL CDI 3~~ ∆/2𝜋𝜋 

## ● Maximum Entropy Method (MEM) 

 Extrapolation of the autocorrelation 

2026/Statistical Signal Processing and Modeling 

33 

