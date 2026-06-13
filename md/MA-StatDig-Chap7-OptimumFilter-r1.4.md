## **Optimum Filter Statistical Signal Processing and Modelling** 

Lavanchy David (HEIG-VD) Tognolini Maurizio (HEIG-VD) 

1 

TStatDig-OptimumFIlter-1.4 10.04.2026 

## **Plan** 

## ● FIR Wiener filter 

## ● Kalman filter 

2026/Statistical Signal Processing and Modeling 

2 

## **Introduction** 

- The goal of an optimal filter is to **estimate one signal from another one** is , such that the resulting **mean square error** 

- as small as possible 

- There are many applications to this idea, such as estimating the real signal from a noisy observation in medicine (ECG, MRI, etc.) and other fields: 

 Filtering 

 Smoothing 

- Prediction 

- Deconvolution 

- System Identification 

2026/Statistical Signal Processing and Modeling 

3 

## **Application : Filtering** 

2026/Statistical Signal Processing and Modeling 

4 

## **FIR Wiener filter** 

## ● Wiener filtering problem 

desired signal measured Wiener filter estimated d(n) signal (to be found) signal Error estimation x(n) oe d(n) -¢ e(n) 𝑥𝑥 f] 𝑛𝑛= 𝑑𝑑 [1 𝑛𝑛+ 𝑣𝑣[𝑛𝑛] desired measured noise signal signal 

## ● Goal : Find an optimal FIR filter W(z) 

**==> picture [464 x 178] intentionally omitted <==**

2026/Statistical Signal Processing and Modeling 

6 

## **FIR Wiener filter** 

- It is assumed that and are x[n] d[n] **jointly wide-sense** 

- **stationary (WSS)** 

- Goal is to find an optimal FIR filter (coefficients of the filter w[n]) which results in the **smallest mean squared error** between the desired signal and the estimated signal 

2 2 = 𝜉𝜉= 𝐸𝐸 𝑒𝑒 𝑛𝑛 𝐸𝐸 𝑑𝑑 𝑛𝑛− 𝑑𝑑[̂] 𝑛𝑛 (ty {tl ti} 

2026/Statistical Signal Processing and Modeling 

7 

## **FIR Wiener Filter** 

● To find the smallest mean square error, all derivative must be equal to 0 (for k=0,1,.., p-1). 

**==> picture [784 x 188] intentionally omitted <==**

𝜕𝜕𝑒𝑒[∗] [𝑛𝑛] ● It gives for the derivative term :[= ⋯= −𝑥𝑥][∗][[𝑛𝑛−𝑘𝑘]] 𝜕𝜕𝑤𝑤[∗] [𝑘𝑘] 

● And finally: 

**==> picture [379 x 70] intentionally omitted <==**

_Leads to the orthogonality principle : data used for the estimation x[n] is orthogonal to the error e[n] and so their dot product is null._ 

2026/Statistical Signal Processing and Modeling 

8 

## **FIR Wiener filter** 

- Based on this orthogonality results, the equations to derive the filter coefficients can be determined: 

> 𝐸𝐸 (1 𝑒𝑒 𝑛𝑛 𝑥𝑥[∗] [𝑛𝑛−𝑘𝑘] = 0 k = 0, 1,…, p-1 

𝑝𝑝−1 = 0 𝐸𝐸 𝑤𝑤 𝑙𝑙⋅𝑥𝑥[𝑛𝑛−𝑙𝑙] 𝑥𝑥[∗] [𝑛𝑛−𝑘𝑘] Coa 𝑙𝑙=0 𝑝𝑝−1 − = 0 𝐸𝐸 𝑑𝑑 𝑛𝑛 𝑥𝑥[∗] 𝑛𝑛−𝑘𝑘 𝑤𝑤[𝑙𝑙] 𝐸𝐸 𝑥𝑥[𝑛𝑛−𝑙𝑙]𝑥𝑥[∗] [𝑛𝑛−𝑘𝑘] (fl f DB > ( 𝑙𝑙=0 \___,___] \________,_____ 𝑟𝑟𝑑 [𝑘𝑘] 𝑟𝑟 [𝑘𝑘−𝑙𝑙] 𝑑𝑑 𝑝𝑝−1 𝑤𝑤[𝑙𝑙] 𝑟𝑟 𝑘𝑘−𝑙𝑙= 𝑟𝑟𝑑 [𝑘𝑘] 𝑑𝑑 𝑙𝑙=0 

## ● It gives the final results 

2026/Statistical Signal Processing and Modeling 

9 

## **FIR Wiener filter** 

## ● The previous equation can be written on matrix shape 

**==> picture [878 x 344] intentionally omitted <==**

**----- Start of picture text -----**<br>
𝑝𝑝−1<br>𝑤𝑤[𝑙𝑙] 𝑟𝑟 𝑘𝑘−𝑙𝑙= 𝑟𝑟𝑑 [𝑘𝑘]<br>𝑑𝑑<br>𝑙𝑙=0<br>…<br>𝑙𝑙= 0 𝑙𝑙= 1 𝑙𝑙= 𝑝𝑝−1<br>⋯<br>𝑘𝑘= 0 𝑟𝑟 [0] 𝑟𝑟 [1] 𝑟𝑟 [𝑝𝑝−1] 𝑤𝑤[0] 𝑟𝑟𝑑 [0]<br>𝑑𝑑 𝑑𝑑 𝑑𝑑<br>…<br>𝑟𝑟 [1] 𝑟𝑟 [0] 𝑟𝑟 [𝑝𝑝−2] 𝑤𝑤[1] 𝑟𝑟𝑑 [1]<br>𝑘𝑘= 1 𝑑𝑑 𝑑𝑑 𝑑𝑑 =<br>⋮ ⋮ ⋱ ⋮ ⋮ ⋮<br>⋮<br>𝑘𝑘= 𝑝𝑝−1 𝑟𝑟 [𝑝𝑝−1] 𝑟𝑟 [𝑝𝑝−2] … 𝑟𝑟 [0] 𝑤𝑤[𝑝𝑝−1] 𝑟𝑟𝑑 [𝑝𝑝−1]<br>𝑑𝑑 𝑑𝑑 𝑑𝑑<br>𝒘𝒘 𝒓𝒓𝑑<br>Toeplitz matrix! 𝑹𝑹<br>𝑑𝑑<br>**----- End of picture text -----**<br>


## ● And finally in compact shape also called the **Wiener-Hopf equation** 

𝑹𝑹𝑑𝑑 ⋅𝒘𝒘= 𝒓𝒓𝑑 

2026/Statistical Signal Processing and Modeling 

10 

## **FIR Wiener filter** 

● Finally, the coefficients **(w[k])** that minimize the minimum mean square error are obtained from the Wiener-Hopf equations 

**==> picture [141 x 33] intentionally omitted <==**

**----- Start of picture text -----**<br>
𝑹𝑹𝑑𝑑 ⋅𝒘𝒘= 𝒓𝒓𝑑<br>**----- End of picture text -----**<br>


- As the correlation matrix 𝑹𝑹 is Toeplitz, the inversion can be 𝑑𝑑 

- easily computed with Levinson-Durbin 

𝒘𝒘= 𝑹𝑹𝑑𝑑[−𝟏𝟏] ⋅𝒓𝒓𝑑 

2026/Statistical Signal Processing and Modeling 

11 

## **FIR Wiener filter** 

## ● 

## The **estimated** : **mean-square error** in the estimate of d[n] may be 

**==> picture [919 x 610] intentionally omitted <==**

2026/Statistical Signal Processing and Modeling 

## **FIR Wiener filter** 

- The Wiener-Hopf equation requires the autocorrelation ( 𝑹𝑹 ) 𝑑𝑑 

- and cross-correlation 𝒓𝒓𝑑 which are most of the time unknown. 

𝑹𝑹𝑑𝑑 ⋅𝒘𝒘= 𝒓𝒓𝑑 

- So they have to be estimated on the signal: 

𝑑𝑑[⋅𝒘𝒘=] 𝑑 

- The quality of the estimation will affect the Wiener filter coefficients 

𝑁𝑁−1 1 ̂𝑟𝑟𝑑 [𝑘𝑘] = 𝑑𝑑 𝑛𝑛⋅𝑥𝑥[∗] [𝑛𝑛−𝑘𝑘] 𝑁𝑁 𝑛𝑛=0 

2026/Statistical Signal Processing and Modeling 

13 

## **Filtering Application** 

## ● In filtering, d[n] is observed from a noise corrupted observation 

**==> picture [196 x 26] intentionally omitted <==**

- An usual assumption is that the noise has zero mean and is uncorrelated with the signal 

**==> picture [223 x 26] intentionally omitted <==**

- **The goal is to find the filter W(z) to estimate** 𝒅𝒅[𝒏𝒏] 

2026/Statistical Signal Processing and Modeling 

14 

## **Filtering** 

- The Wiener-Hopf equation can be modified for this application 

𝑹𝑹𝑑𝑑 ⋅𝒘𝒘= 𝒓𝒓𝑑 

● become: The cross-correlation by using 𝑥𝑥 𝑛𝑛= 𝑑𝑑 𝑛𝑛+ 𝑣𝑣[𝑛𝑛] LJ] 6 6oE] 𝑟𝑟𝑑 [𝑘𝑘] = 𝐸𝐸 (fli 𝑑𝑑 𝑛𝑛 𝑥𝑥[∗] 𝑛𝑛−𝑘𝑘 DB = 𝐸𝐸 €lll 𝑑𝑑 𝑛𝑛 𝑑𝑑[∗] 𝑛𝑛−𝑘𝑘 B + 𝐸𝐸 €lll 𝑑𝑑 𝑛𝑛 𝑣𝑣 𝑛𝑛−𝑘𝑘 ⇒𝑟𝑟𝑑 𝑘𝑘= 𝑟𝑟 [𝑘𝑘] 𝑑𝑑 𝑟𝑟 [𝑘𝑘] = 0 because assumption 𝑑𝑑 

= 0 because assumption noise is uncorrelated to signal 

## ● And the auto-correlation become: 

𝑟𝑟 [𝑘𝑘] = 𝐸𝐸 (F 𝑥𝑥 𝑛𝑛+ 𝑘𝑘𝑥𝑥 Jib[∗] 𝑛𝑛 = 𝐸𝐸 ae 𝑑𝑑 𝑛𝑛+ 𝑘𝑘+ 𝑣𝑣[𝑛𝑛+ 𝑘𝑘] 4 Hl) 𝑑𝑑 𝑛𝑛+ 𝑣𝑣[𝑛𝑛] 03[∗] 𝑑𝑑 ⇒𝑟𝑟 rl 𝑘𝑘= 𝑟𝑟 𝑘𝑘+ 𝑟𝑟 [𝑘𝑘] 𝑑𝑑 𝑑𝑑 𝑣𝑣 

- The **Wiener-Hopf equation become** : 

𝑹𝑹 + 𝑹𝑹 ⋅𝒘𝒘= 𝒓𝒓 𝑑𝑑 𝑣𝑣 𝑑𝑑 

2026/Statistical Signal Processing and Modeling 

15 

## **Example Filtering (7.2.1)** 

- AR(1) process : 𝑑𝑑 𝑛𝑛= 0.8𝑑𝑑 𝑛𝑛−1 + 𝑤𝑤[𝑛𝑛] 

- ● Measured in noisy environment : 𝑥𝑥 𝑛𝑛= 𝑑𝑑 𝑛𝑛+ 𝑣𝑣[𝑛𝑛] 

- ● Wiener filter obtained (p=1) : 𝒘𝒘= 0.405, 0.238 

2026/Statistical Signal Processing and Modeling 

16 

## **Noise cancellation** 

## ● Similar to filtering problem but, this time, an auxiliary noise 𝑣𝑣2[𝑛𝑛] correlated with measurement noise 𝑣𝑣1[𝑛𝑛] is used to estimate original signal 𝑑𝑑[𝑛𝑛] 

baby, lowdynamics Pollution of the Remove Heart beat of the foetus oa heart beat mother —_— estimated v1 [Nn on the heart beat pollution foetus Unknown transfer function Wiener Heart beat of the mother filter 

Estimation of the pollution 

2026/Statistical Signal Processing and Modeling 

17 

## **Noise cancellation** 

## ● Hence the Wiener-Hopf equation can be formulated again 

**==> picture [97 x 18] intentionally omitted <==**

**----- Start of picture text -----**<br>
unknown<br>**----- End of picture text -----**<br>


𝑹𝑹𝑑𝑑 ⋅𝒘𝒘= 𝒓𝒓𝑑 ⇒𝑹𝑹𝑣𝑣2 ⋅𝒘𝒘= 𝒓𝒓𝑣𝑣1𝑣𝑣2 

## unknown 

2026/Statistical Signal Processing and Modeling 

18 

## **Noise cancellation** 

● The cross-correlation can be expressed as: 

𝑟𝑟 [1] 𝑘𝑘= 𝐸𝐸 ¢ 𝑣𝑣1 1 𝑛𝑛 𝑣𝑣2∗ 𝑛𝑛−𝑘𝑘 3B = 𝐸𝐸 tl 𝑥𝑥 𝑛𝑛−𝑑𝑑[𝑛𝑛] It 𝑣𝑣2∗ 𝑛𝑛−𝑘𝑘 𝑣𝑣1𝑣𝑣2 = 𝐸𝐸 f 𝑥𝑥[𝑛𝑛]𝑣𝑣2∗ [ 𝑛𝑛−𝑘𝑘 B −𝐸𝐸 tf 𝑑𝑑[𝑛𝑛]𝑣𝑣2∗ Cf 𝑛𝑛−𝑘𝑘 BD \—___,—_J = 0 because signal and noise are uncorrelated 

**==> picture [487 x 33] intentionally omitted <==**

## ● Finally, the Wiener-Hopf equations become: 

𝑹𝑹 𝑣𝑣2 ⋅𝒘𝒘= 𝒓𝒓𝑑𝑑𝑣𝑣2 

2026/Statistical Signal Processing and Modeling 

19 

## **Example Noise cancellation (7.2.6)** 

- Desired signal is : 𝑑𝑑 𝑛𝑛= sin 𝑛𝑛𝜔𝜔0 + 𝜙𝜙 

- Measured  signal : 𝑥𝑥 𝑛𝑛= 𝑑𝑑 𝑛𝑛+ 𝑣𝑣1[𝑛𝑛] 

- ● Noise measured : 𝑣𝑣2 𝑛𝑛= −0.6𝑣𝑣2[𝑛𝑛−1] + 𝑣𝑣[𝑛𝑛] 

2026/Statistical Signal Processing and Modeling 

20 

## **Linear Prediction** 

● The goal is to **predict future samples x[n+1]** as a linear combination of past ones: 

**==> picture [205 x 85] intentionally omitted <==**

**----- Start of picture text -----**<br>
𝑝𝑝−1<br>=<br>𝑤𝑤 𝑘𝑘𝑦𝑦[𝑛𝑛−𝑘𝑘]<br>𝑘𝑘=0<br>**----- End of picture text -----**<br>


2026/Statistical Signal Processing and Modeling 

21 

## **Linear Prediction** 

● **The Wiener-Hopf equation can be modified for this application** by using 𝑦𝑦 I! 𝑛𝑛= 𝑥𝑥 66E 𝑛𝑛+ 𝑣𝑣[𝑛𝑛] | where 𝑥𝑥 L 𝑛𝑛 | and zero mean white noise 𝑣𝑣[𝑛𝑛] with variance 𝜎𝜎 are uncorrelated 𝑣𝑣[2] ● The cross-correlation by using 𝑑𝑑 L 𝑛𝑛= 𝑥𝑥[𝑛𝑛+ 𝛼𝛼] | where 𝛼𝛼 is the shifted prediction index become ( 𝛼𝛼= 1 for one step) 𝑟𝑟 𝑘𝑘= 𝐸𝐸 𝑑𝑑 𝑛𝑛 𝑦𝑦[∗] 𝑛𝑛−𝑘𝑘 = 𝐸𝐸 𝑥𝑥 𝑛𝑛+ 𝛼𝛼 𝑥𝑥[∗] 𝑛𝑛−𝑘𝑘 + 𝐸𝐸 𝑥𝑥 𝑛𝑛+ 𝛼𝛼 𝑣𝑣[∗] 𝑛𝑛−𝑘𝑘 𝑑𝑑𝑦𝑦 lL] 6©t fllh UG Ut Pio6U tL Ito = 𝑟𝑟 [𝛼𝛼+ 𝑘𝑘] 𝑑𝑑 \____,____J = 0 because assumption noise is uncorrelated to signal ● The auto-correlation become 𝜎𝜎 𝛿𝛿[𝑘𝑘] 𝑣𝑣[2] 𝑟𝑟 𝑘𝑘= 𝐸𝐸 𝑦𝑦 𝑛𝑛 𝑦𝑦[∗] 𝑛𝑛−𝑘𝑘 = 𝐸𝐸 𝑥𝑥 𝑛𝑛 𝑥𝑥[∗] 𝑛𝑛−𝑘𝑘 + 𝐸𝐸 𝑣𝑣 𝑛𝑛 𝑣𝑣[∗] 𝑛𝑛−𝑘𝑘 = 𝑟𝑟 𝑘𝑘+ 𝑟𝑟 [𝑘𝑘] 𝑦𝑦 𝑑𝑑 𝑣𝑣 Ti re Oe eseS Ob Oe Py ● It gives the new Wiener-Hopf equation for multi-step prediction 

⇒ 𝑹𝑹 ⋅𝒘𝒘= 𝒓𝒓 𝑦𝑦 𝑑𝑑𝑦𝑦 𝑹𝑹 + 𝜎𝜎 𝑰𝑰⋅𝒘𝒘= 𝒓𝒓 (𝛼𝛼) 𝑑𝑑 𝑣𝑣[2] 𝑑𝑑 

2026/Statistical Signal Processing and Modeling 

22 

## **Linear Prediction** 

● The Wiener-Hopf equation can be expressed with matrix as: 

𝑹𝑹 + 𝜎𝜎 𝑰𝑰⋅𝒘𝒘= 𝒓𝒓 (𝛼𝛼) 𝑑𝑑 𝑣𝑣[2] 𝑑𝑑 

**==> picture [831 x 138] intentionally omitted <==**

**----- Start of picture text -----**<br>
⋯<br>0<br>𝑟𝑟 + 𝜎𝜎 𝑟𝑟 [1] 𝑟𝑟 [𝑝𝑝−1] 𝑤𝑤[0] 𝑟𝑟 [𝛼𝛼]<br>𝑑𝑑 𝑣𝑣 [2] 𝑑𝑑 𝑑𝑑 𝑑𝑑<br>𝑟𝑟𝑑𝑑[1] 𝑟𝑟𝑑𝑑[0] + 𝜎𝜎𝑣𝑣 [2] … 𝑟𝑟𝑑𝑑[𝑝𝑝−2] 𝑤𝑤[1] = 𝑟𝑟𝑑𝑑[𝛼𝛼+ 1]<br>⋮ ⋮ ⋱ ⋮ ⋮ ⋮<br>𝑟𝑟 [𝑝𝑝−1] 𝑟𝑟 [𝑝𝑝−2] … 𝑟𝑟 [0] + 𝜎𝜎 𝑤𝑤[𝑝𝑝−1] 𝑟𝑟𝑑𝑑[𝛼𝛼+ 𝑝𝑝−1]<br>𝑑𝑑 𝑑𝑑 𝑑𝑑 𝑣𝑣 [2]<br>**----- End of picture text -----**<br>


● = 0 If the noise v[n] is null ( 𝜎𝜎 ), the Wiener-Hopf is simplified 𝑣𝑣[2] as : 

𝑹𝑹 ⋅𝒘𝒘= 𝒓𝒓 (𝛼𝛼) 𝑑𝑑 𝑑𝑑 

2026/Statistical Signal Processing and Modeling 

23 

## **Example Linear Prediction (7.2.2)** 

● AR(1) process : 𝑥𝑥 𝑛𝑛= −0.7𝑥𝑥 𝑛𝑛−1 + 𝑤𝑤[𝑛𝑛] ● Measured **without noise** environment : 𝑦𝑦 𝑛𝑛= 𝑥𝑥 𝑛𝑛 ● Wiener predict obtained (p=1) : 𝒘𝒘= 0.6117, 0.0704 

2026/Statistical Signal Processing and Modeling 

24 

## **Example Linear Prediction (7.2.3)** 

● AR(1) process : 𝑥𝑥 𝑛𝑛= −0.7𝑥𝑥 𝑛𝑛−1 + 𝑤𝑤[𝑛𝑛] ● Measured **with noise** environment : 𝑦𝑦 𝑛𝑛= 𝑥𝑥 𝑛𝑛+ 𝑣𝑣[𝑛𝑛] ● Wiener predict obtained (p=1) : 𝒘𝒘= 0.405, 0.238 

2026/Statistical Signal Processing and Modeling 

25 

## **Plan** 

## ● FIR Wiener filter 

## ● Kalman filter 

2026/Statistical Signal Processing and Modeling 

26 

## **Kalman filter** 

- The goal of the _Kalman filter_ is to estimate the unknown state vector of a dynamic system 𝑿𝑿[𝑛𝑛] based on the measurement 𝑧𝑧[𝑛𝑛] and others parameters. 

● Kalman filter is heavily used in tracking problem, sometimes with Image processing. For example DeepSort tracking: 

2026/Statistical Signal Processing and Modeling 

27 

## **Example Kalman Body in gravitation** 

## ● Estimation of a noisy measurement 

2026/Statistical Signal Processing and Modeling 

28 

## **Example Kalman truck** 

## **on rail** 

## ● Estimation of the position and speed of a truck with a noisy input and measurement 

2026/Statistical Signal Processing and Modeling 

29 

## **Kalman filter** 

● With FIR Wiener, 𝑑𝑑[𝑛𝑛] can be estimated with a FIR filter 

0 1 + ⋯ ̂𝑑𝑑 f} 𝑛𝑛= 𝑤𝑤 C1 ⋅𝑥𝑥 (1 𝑛𝑛+ 𝑤𝑤 tit ⋅𝑥𝑥 𝑛𝑛−1 J 

## ● With IIR Wiener, 𝑑𝑑[𝑛𝑛] can be estimated with a IIR filter 

**==> picture [882 x 122] intentionally omitted <==**

2026/Statistical Signal Processing and Modeling 

30 

## **Kalman filter** 

- **Wiener** is optimum if x[n] and d[n] are WSS. 

- Another way to filter a signal is to **use the knowledge of the process** ( 𝐻𝐻(𝑧𝑧) ) and the **knowledge of the measurement system.** 

- ● This approach is known as **Kalman filter** and does not require that x[n] and d[n] are WSS. 

**==> picture [771 x 207] intentionally omitted <==**

**----- Start of picture text -----**<br>
𝑥𝑥[𝑛𝑛] 𝑧𝑧[𝑛𝑛] x[n|<br>𝑤𝑤[𝑛𝑛] 𝑑𝑑[𝑛𝑛] 𝑥𝑥[𝑛𝑛] ̂𝑑𝑑 𝑛𝑛<br>Kalman<br>𝐻𝐻(𝑧𝑧)<br>Measurement Filter<br>Process  Process  Estimated<br>noise state state<br>𝑣𝑣[𝑛𝑛]<br>Measurement<br>noise<br>**----- End of picture text -----**<br>


- **Unfortunately, the notation used for Kalman is different in the literature!** 

2026/Statistical Signal Processing and Modeling 

31 

## **Kalman filter** 

● and are Let’s say that x[n] is an AR(1) driven process ( 𝑤𝑤[𝑛𝑛] 𝑣𝑣[𝑛𝑛] uncorrelated white noise process): 

𝑥𝑥 tL] 𝑛𝑛= 𝑎𝑎 6d 1 𝑥𝑥 𝑛𝑛−1 + 𝑤𝑤[𝑛𝑛] and 𝑧𝑧 tL] 𝑛𝑛= 𝑥𝑥 6 60] 𝑛𝑛+ 𝑣𝑣[𝑛𝑛] ● Even if we know 𝑎𝑎[1] , it is not possible to predict 𝑥𝑥[𝑛𝑛] as we don’t know 𝑤𝑤[𝑛𝑛] 

- For example, suppose we have : 

= 𝑥𝑥 | 𝑛𝑛−1 

- : 

- And you want to predict 𝑥𝑥[𝑛𝑛] by knowing 𝑎𝑎[1] 

- As 𝑤𝑤[𝑛𝑛] is a white noise, 𝑥𝑥 L 𝑛𝑛 | cannot be estimated perfectly 

2026/Statistical Signal Processing and Modeling 

32 

## **Kalman filter** 

● However, the measure 𝑧𝑧[𝑛𝑛] contains the information of 𝑤𝑤[𝑛𝑛] but unfortunately also a measurement noise 𝑣𝑣[𝑛𝑛] 

**==> picture [678 x 141] intentionally omitted <==**

● If the measurement noise is null 𝑣𝑣 L 𝑛𝑛= 0 | , the best estimated of 𝑥𝑥[𝑛𝑛] is : 

**==> picture [561 x 62] intentionally omitted <==**

2026/Statistical Signal Processing and Modeling 

33 

## **Kalman filter** 

- In reality, we don’t know 𝑎𝑎[1] and 𝑣𝑣 L 𝑛𝑛 | is not null. 

- ● To compensate, a Kalman gain **K** is added in factor to the new information brought by z[n] 

̂𝑧𝑧 L 𝑛𝑛 | ̂𝑧𝑧 L 𝑛𝑛 | a ItH—__ I − 1 + **K** ⋅ 1 𝑎𝑎 [| |-X[n—-1] CL] 𝑧𝑧 𝑛𝑛 𝑎𝑎 [ /in-1) Kalman gain 𝛼𝛼[𝑛𝑛] = 𝑧𝑧 L 𝑛𝑛−̂𝑧𝑧[𝑛𝑛] | Noisy Error (Innovation process) measurement 

Best estimate of x[n] without noise 

- If x[n] and z[n] are not stationary, the equation is written : 

**==> picture [612 x 36] intentionally omitted <==**

2026/Statistical Signal Processing and Modeling 

34 

## **Kalman filter** 

## ● If x[n] is an AR( **p** ) driven process, then it becomes: 𝑝𝑝 𝑥𝑥 L 𝑛𝑛= ∑ | 𝑎𝑎 al 𝑘𝑘𝑥𝑥 𝑛𝑛−𝑘𝑘+ 𝑤𝑤[𝑛𝑛] | and 𝑧𝑧 [] 𝑛𝑛= 𝑥𝑥 [] 𝑛𝑛+ 𝑣𝑣[𝑛𝑛] 𝑘𝑘=1 

## ● Or in the matrix notation 

**==> picture [836 x 454] intentionally omitted <==**

**----- Start of picture text -----**<br>
𝑥𝑥[𝑛𝑛] … 𝑥𝑥[𝑛𝑛−1]<br>𝑎𝑎[1] 𝑎𝑎[2] 𝑎𝑎[𝑝𝑝] 𝑤𝑤[𝑛𝑛]<br>𝑥𝑥[𝑛𝑛−1] 1 0 … 0 𝑥𝑥[𝑛𝑛−2] 0<br>=<br>0 1 … 0 + 0<br>𝑥𝑥[𝑛𝑛−2] 𝑥𝑥[𝑛𝑛−3]<br>⋮ ⋮ ⋮ ⋱ ⋮ ⋮ ⋮<br>0 0 … 1 0<br>𝑥𝑥[𝑛𝑛−𝑝𝑝+ 1] 𝑥𝑥[𝑛𝑛−𝑝𝑝]<br>𝒘𝒘[𝑛𝑛]<br>𝒙𝒙[𝑛𝑛] 𝑭𝑭 𝒙𝒙[𝑛𝑛−1]<br>Noise process<br>New state Transition matrix Previous state<br>𝑥𝑥 [J 𝑛𝑛<br>𝑥𝑥 𝑛𝑛−1<br>1 0 … 0<br>𝑧𝑧 𝑛𝑛= + 𝑣𝑣[𝑛𝑛]<br>⋮<br>Measurement<br>Noise measurement<br>[1 [ | 𝑥𝑥 𝑛𝑛−𝑝𝑝+ 1 :<br>\__,—___J |____——__J<br>Measurement matrix<br>𝑯𝑯 𝒙𝒙[𝑛𝑛]<br>**----- End of picture text -----**<br>


2026/Statistical Signal Processing and Modeling 

35 

New state 

## **Kalman filter** 

## ● Using the matrix, notation, we obtain: 

**==> picture [622 x 287] intentionally omitted <==**

**----- Start of picture text -----**<br>
New  Transition  Previous  Noise<br>state matrix state<br>process<br>ae NO /<br>𝒙𝒙 𝑛𝑛= 𝑭𝑭⋅𝒙𝒙 𝑛𝑛−1 + 𝒘𝒘 𝑛𝑛<br>se en ee<br>𝒛𝒛 CJ 𝑛𝑛= 𝑯𝑯⋅𝒙𝒙 CJ 𝑛𝑛+ 𝒗𝒗[𝑛𝑛]<br>yo \<br>Measurement  Noise<br>Measurement<br>matrix disturbance<br>**----- End of picture text -----**<br>


## ● So, the best estimate of x[n] is: 

**==> picture [98 x 34] intentionally omitted <==**

**----- Start of picture text -----**<br>
+ 𝑲𝑲[𝑛𝑛]<br>**----- End of picture text -----**<br>


2026/Statistical Signal Processing and Modeling 

36 

## **Kalman filter** 

## ● A more heavy notation can be found 

**==> picture [525 x 145] intentionally omitted <==**

Estimation of x[n] Innovation or Estimation of x[n] knowing up to measurement knowing up to sample n residual sample n-1 

[qx1] [qxp] [pxp] [px1] ̂𝑧𝑧 | 𝑛𝑛 | = 𝑯𝑯⋅ F-x|[n—-1| \__,_J \_____,__ ̂𝑧𝑧 | 𝑛𝑛|𝑛𝑛−1 = 𝑯𝑯⋅ x|[n|n Estimation of z[n] knowing sample up to n-1 

2026/Statistical Signal Processing and Modeling 

37 

## **Kalman filter** 

## ● Finally, the Kalman predictor is: 

## ● With the corresponding error: 

**==> picture [363 x 101] intentionally omitted <==**

## ● And the **covariance matrices errors** are: 

[pxp] [px1] [1xp] 𝑷𝑷 L 𝑛𝑛|𝑛𝑛= 𝐸𝐸 | it 𝒆𝒆 𝑛𝑛|𝑛𝑛𝒆𝒆 J[𝑯𝑯] t 𝑛𝑛|𝑛𝑛 8 𝑷𝑷 | 𝑛𝑛|𝑛𝑛−1 1 = 𝐸𝐸 tl 𝒆𝒆 𝑛𝑛|𝑛𝑛−1 | 𝒆𝒆[𝑯𝑯] | 𝑛𝑛|𝑛𝑛−1 

2026/Statistical Signal Processing and Modeling 

38 

## **Kalman filter** 

● It can be shown that 𝑷𝑷 | 𝑛𝑛|𝑛𝑛−1 can be also obtained recursively : [pxp] [pxp] [pxp] [pxp] [pxp] 𝑷𝑷 | 𝑛𝑛|𝑛𝑛−1 = 𝑭𝑭⋅𝑷𝑷 | 𝑛𝑛−1|𝑛𝑛−1 ⋅𝑭𝑭[′] + 𝑸𝑸 𝑤𝑤 ● The Kalman gain is obtained by minimizing the quadratic error : 𝜕𝜕𝜉𝜉 𝑛𝑛 ⇒ = 0 𝜉𝜉 𝑛𝑛= 𝑡𝑡𝑟𝑟 𝑷𝑷[𝑛𝑛|𝑛𝑛] = 𝐸𝐸 𝒆𝒆[𝑛𝑛|𝑛𝑛[2] LJ it y ill | 5 ~~==~~ 𝜕𝜕𝑲𝑲 [pxp] [pxq] [qxp] [pxp] [pxq] [qxq] −1 ⇒ 𝑲𝑲[𝑛𝑛] = 𝑷𝑷 rl 𝑛𝑛𝑛𝑛−1 J 𝑯𝑯[𝐻𝐻] ~ 𝑯𝑯⋅𝑷𝑷 flo] 𝑛𝑛𝑛𝑛−1 ⋅𝑯𝑯[𝐻𝐻] + 𝑸𝑸𝑣𝑣 [ 𝑛𝑛 J] 

● The covariance of the error 𝑒𝑒[𝑛𝑛|𝑛𝑛] can be rewritten : 

> 𝑷𝑷 LI] 𝑛𝑛𝑛𝑛= [ 𝑰𝑰−𝑲𝑲 L 𝑛𝑛𝑯𝑯⋅𝑷𝑷[𝑛𝑛|𝑛𝑛−1] | | 

Where 𝑸𝑸 [𝑛𝑛] is the covariance matrix of the measurement noise v[n] and 𝒗𝒗 𝑸𝑸 [𝑛𝑛] is the covariance matrix of the process noise 𝒘𝒘 

2026/Statistical Signal Processing and Modeling 

39 

## **Kalman filter** 

● To summarize, the implementation of the Kalman filter is recursive : 

_For n=1,2,… compute :_ 

## Prediction 

Update 

> 𝑷𝑷 |l 𝑛𝑛|𝑛𝑛−1 = 𝑭𝑭⋅𝑷𝑷 𝑛𝑛−1|𝑛𝑛−1 ⋅𝑭𝑭[𝑯𝑯] + 𝑸𝑸 [𝑛𝑛] 𝒘𝒘 −1 

> 𝑲𝑲[𝑛𝑛] = 𝑷𝑷 | 𝑛𝑛𝑛𝑛−1 | 1 𝑯𝑯[𝐻𝐻] | 𝑯𝑯⋅𝑷𝑷 | 𝑛𝑛𝑛𝑛−1 | ⋅𝑯𝑯[𝐻𝐻] + 𝑸𝑸𝑣𝑣 [ 𝑛𝑛 J X[n|n| = X[n|n — 1] + K[n| |z[n] —H-x|n|n—- 1] 

> 𝑷𝑷 LI] 𝑛𝑛𝑛𝑛= | 𝑰𝑰−𝑲𝑲 LJ 𝑛𝑛𝑯𝑯⋅𝑷𝑷[𝑛𝑛|𝑛𝑛−1] | 

2026/Statistical Signal Processing and Modeling 

40 

## **Kalman filter** 

- All that needs to be done to complete the recursion is to initialize at time n=0. The initial estimate is very often chosen 

## x|0|0] = 𝐸𝐸{𝒙𝒙 ( 0 ) } 𝑷𝑷 [| 0|0 = 𝐸𝐸{𝒙𝒙 () 0 𝒙𝒙[𝐻𝐻] ©) 0 } 

## ● **Important observation:** 

- K[n] and P[n|n] do not depend of x[n]. Therefore, they can be computed off-line prior to any new measurement. 

2026/Statistical Signal Processing and Modeling 

41 

