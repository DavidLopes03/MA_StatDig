## **Adaptive filter Statistical Signal Processing and Modelling** 

Lavanchy David (HEIG-VD) Tognolini Maurizio (HEIG-VD) 

1 

TStatDig- AdaptiveFilter-1.10 17.05.2026 

## **Plan** 

## ● Introduction 

- FIR Adaptive filter 

## ● Recursive Least Square 

2 

## **Introduction** 

## ● Noise cancellation of non stationary noise 

3 

## **Introduction** 

- **In previous** , for signal modeling, Wiener filtering and spectrum estimation, **signals were stationary** 

- In most application will be **non-stationary** 

**==> picture [827 x 218] intentionally omitted <==**

**----- Start of picture text -----**<br>
●<br>One way is  to process in blocks , where  we suppose<br>.<br>stationary x[k]<br>B1 B2 B3 B4<br>k<br>**----- End of picture text -----**<br>


- This approach is limited for several reasons: 

 For rapid varying process, the interval will be too small 

   - Not easily accommodate step change within intervals 

   - Imposes an incorrect model of the data 

- **A better approach is proposed with adaptive filtering** 

4 

## **Introduction** 

● Let’s remind Wiener filter for WSS process 𝑝𝑝−1 𝑤𝑤 𝑘𝑘⋅𝑥𝑥[𝑛𝑛−𝑘𝑘] diml=) [] 𝑘𝑘=0 ● The filter coefficients 𝑤𝑤 7 𝑘𝑘 that minimize the modeling error 2 are 𝑒𝑒 fr) 𝑛𝑛= 𝑑𝑑 𝑛𝑛− 𝑑𝑑[𝑛𝑛][̂] in the mean square sense E{ na 𝑒𝑒 𝑛𝑛 } found by solving the Wiener-Hopf equation 𝑹𝑹𝑥 ⋅𝒘𝒘= 𝒓𝒓 𝑑𝑑𝑥𝑥 ● However, if 𝑑𝑑 fl 𝑛𝑛 and 𝑥𝑥 𝑛𝑛 are **non-stationary,** then the filter 2 coefficients that minimize E{ itd 𝑒𝑒 𝑛𝑛 } will depend on n. 𝑝𝑝−1 𝑤𝑤 𝑘𝑘⋅𝑥𝑥[𝑛𝑛−𝑘𝑘] 𝑛𝑛 d=) 𝑘𝑘=0 ̂𝑑𝑑 [| 𝑛𝑛= 𝒘𝒘 ⋅𝒙𝒙[𝑛𝑛] 𝒏𝒏[𝑻𝑻] 2 ● Minimizing E{ na 𝑒𝑒 𝑛𝑛 } for each n will be very difficult. 

5 

## **Introduction** 

● Problem may be simplified if we relax the requirement that 𝒘𝒘 minimize the mean-square error at each time n and 𝑛𝑛 consider, instead, a coefficient update equation of the form 

**==> picture [576 x 411] intentionally omitted <==**

**----- Start of picture text -----**<br>
Correction coefficient<br>𝒘𝒘 = 𝒘𝒘 + Δ𝒘𝒘<br>𝑛𝑛+1 𝑛𝑛 𝑛𝑛<br>𝑑𝑑[𝑛𝑛]<br>+<br>𝑥𝑥[𝑛𝑛] ̂𝑑𝑑[𝑛𝑛]<br>Wn(z) +<br>-<br>𝑒𝑒[𝑛𝑛]<br>Δ𝑤𝑤<br>𝑛𝑛<br>Adaptive<br>algorithm<br>**----- End of picture text -----**<br>


6 

## **Introduction** 

## ● Adaptive algorithm should 

1. For stationary process, correction should make 𝒘𝒘 converge to the 𝑛𝑛 Wiener-Hopf equation : lim[−1][ ⋅𝒓𝒓][𝑑𝑑𝑥𝑥] 𝑛𝑛→∞[𝒘𝒘][𝑛𝑛][= 𝑹𝑹][𝑥] 2. Don’t need to know the statistics 𝑟𝑟𝑥 [𝑘𝑘] and 𝑟𝑟 [𝑘𝑘] to compute 𝚫𝚫𝒘𝒘 𝑑𝑑𝑥𝑥 𝑛𝑛 3. For non-stationary signals, the filter should be able to adapt to the changing statistics and “track” the evolution as it evolves in time. 

7 

## **Error computation** 

## ● System identification 

## ● Noise cancellation 

8 

## **Plan** 

## ● Introduction 

- FIR Adaptive filter 

## ● Recursive Least Square 

9 

## **Steepest descent** 

# 2 ● Goal is to find 𝒘𝒘 at time n that minimizes: ξ n = E{ 𝑒𝑒 𝑛𝑛 } 𝑛𝑛 

**==> picture [756 x 210] intentionally omitted <==**

**----- Start of picture text -----**<br>
n<br>𝜕𝜕ξ L |<br>●<br>Wiener-Hopf equation is the solution of :<br>𝜕𝜕𝑤𝑤<br>𝑘𝑘 [= 0]<br>n<br>𝜕𝜕ξ L|<br>𝑤𝑤1<br>● n = ⋮<br>The gradient vector is :  ∇ξ<br>n<br>𝜕𝜕ξ L|<br>𝑤𝑤<br>𝑝𝑝<br>**----- End of picture text -----**<br>


- Thus, the update equation is : 

𝑤𝑤 = 𝑤𝑤 −𝜇𝜇⋅∇ξ [n] 𝑛𝑛+1 𝑛𝑛 

Negative because opposite Step size direction of the gradient 

**==> picture [27 x 18] intentionally omitted <==**

**----- Start of picture text -----**<br>
10<br>**----- End of picture text -----**<br>


## **Steepest descent** 

## ● The iterative algorithm that minimize ξ L n | is as follows: 

1. Initialize the algo with an initial estimate 𝒘𝒘0 

2. Evaluate the gradient of ξ L n | at the current estimate 𝒘𝒘 𝑛𝑛 

3. Update the estimate at time n by adding a correction: 

𝒘𝒘 = 𝒘𝒘 −𝜇𝜇⋅∇ξ [n] 𝑛𝑛+1 𝑛𝑛 

4. Go back and repeat 2 and 3. 

11 

## **Convergences** 

● n Let us evaluate the gradient vector : ∇ξ | | ( 𝑤𝑤 is complex): 𝑛𝑛 

2 2 n ∇ ∇ξ | | = ∇𝐸𝐸 Os 𝑒𝑒 𝑛𝑛 |e ee = 𝐸𝐸 ee 𝑒𝑒 𝑛𝑛 | = 𝐸𝐸 𝑒𝑒 𝑛𝑛⋅∇𝑒𝑒 \___,___J[∗] 𝑛𝑛 n - ∇ξ = −𝐸𝐸 𝑒𝑒 𝑛𝑛⋅𝒙𝒙[∗] 𝑛𝑛 𝒙𝒙[∗] 𝑛𝑛 | | tt] oL B [ ] 𝒘𝒘 = 𝒘𝒘 + 𝜇𝜇⋅𝐸𝐸 𝑒𝑒 𝑛𝑛⋅𝒙𝒙[∗] 𝑛𝑛 𝑛𝑛+1 𝑛𝑛 tt] oL BG 

## ● Thus, finally: 

- So, the gradient is simplified by the average of the error 𝑒𝑒 | 𝑛𝑛 multiplied by the measured signal 𝒙𝒙[∗] | 𝑛𝑛 

12 

## **Convergence WSS** 

● If 𝑑𝑑 L 𝑛𝑛 | and 𝑥𝑥 L 𝑛𝑛 | are WSS, the gradient can be simplified as: n ∇ξ = −𝐸𝐸 𝑒𝑒 𝑛𝑛⋅𝒙𝒙[∗] 𝑛𝑛 = −(𝐸𝐸 𝑑𝑑 𝑛𝑛⋅𝒙𝒙[∗] 𝑛𝑛 −𝐸𝐸 𝒘𝒘[𝑇𝑇] 𝑛𝑛𝒙𝒙 𝑛𝑛⋅𝒙𝒙[∗] 𝑛𝑛) n 𝑅𝑅 ⋅𝑤𝑤 ∇ξ : = −(𝒓𝒓 ([] −𝑹𝑹 ⋅𝒘𝒘 (B ) tf) 𝑟𝑟 CP £€ CIC] 𝑥𝑥 𝑛𝑛 CB 𝑑𝑑𝑥𝑥 𝑥𝑥 𝑛𝑛 𝑑𝑑𝑥𝑥 ● The steepest descent algorithm become: 𝒘𝒘 = 𝒘𝒘 + 𝜇𝜇⋅ 𝒓𝒓 −𝑹𝑹 ⋅𝒘𝒘 𝑛𝑛+1 𝑛𝑛 𝑑𝑑𝑥𝑥 𝑥𝑥 𝑛𝑛 ● ~~a~~ Property: For WSS process 𝑑𝑑 L 𝑛𝑛 | and 𝑥𝑥 L 𝑛𝑛 | , the steepest descent converge to Wiener-Hopf : lim[−1][ ⋅𝒓𝒓][𝑑𝑑𝑥𝑥] 𝑛𝑛→∞[𝒘𝒘][𝑛𝑛][= 𝑹𝑹][𝑥] 2 0 < 𝜇𝜇< if the step size is: 

2 0 < 𝜇𝜇< 𝜆𝜆𝑚 𝑥𝑥 

so 𝜆𝜆𝑚 is the maximum eigenvalue of autocorrelation 𝑅𝑅 𝑥𝑥 𝑥𝑥 dependent of the signal amplitude! 

13 

## **LMS algorithm** 

- Previously, we saw the weight vector update for the steepest descent: 

𝑤𝑤 = 𝑤𝑤 + 𝜇𝜇⋅𝐸𝐸 Cf] 𝑒𝑒 𝑛𝑛⋅𝒙𝒙[∗] 0B 𝑛𝑛 𝑛𝑛+1 𝑛𝑛 ● Expectation 𝐸𝐸 G is generally unknown, so it is replaced by: 𝐿𝐿−1 1 ∗ = 𝑛𝑛 𝑒𝑒 𝑛𝑛−𝑘𝑘⋅𝒙𝒙 𝑛𝑛−𝑘𝑘 Mem-x(B ~~-~~ >) ff If J 𝐿𝐿 𝑘𝑘=0 ● **LMS is simply using a single sample mean (L=1):** 

𝒘𝒘 = 𝒘𝒘 + 𝜇𝜇⋅𝑒𝑒 fr) 𝑛𝑛⋅𝒙𝒙[∗] 4 𝑛𝑛 𝑛𝑛+1 𝑛𝑛 

It is not as efficient as the averaging but much simpler and good enough for most of the cases. 

14 

## **LMS algorithm** 

● The simplicity of the algorithm comes from the fact that the update for the _k_ th coefficient: 

𝑤𝑤 [𝑘𝑘] = 𝑤𝑤 [𝑘𝑘] + 𝜇𝜇⋅𝑒𝑒 [| 𝑛𝑛⋅𝑥𝑥[∗] | 𝑛𝑛−𝑘𝑘 𝑛𝑛+1 𝑛𝑛 

requires only one multiplication and one addition. The value for 𝜇𝜇⋅𝑒𝑒 L 𝑛𝑛 | need only to be computed once and may be used for all the coefficients. 

15 

## **Example of convergence** 

**==> picture [72 x 480] intentionally omitted <==**

**----- Start of picture text -----**<br>
(L = 30)<br>Gradient descent<br>LMS<br>(L = 1)<br>**----- End of picture text -----**<br>


_src : Ex9.2.1_LMSLinearPrediction.mlx_ 

16 

## **LMS with reduced complexity** 

● LMS algorithm to update weight can be even more optimized to reduce the calculation. 

𝒘𝒘 = 𝒘𝒘 + 𝜇𝜇⋅𝑒𝑒 [| 𝑛𝑛⋅𝒙𝒙[∗] od 𝑛𝑛 𝑛𝑛+1 𝑛𝑛 

- The product between the signal and the error is “time consuming” (not true today) because it is floating point. One : 

- simplification is **sign-error algorithm** 

𝒘𝒘 = 𝒘𝒘 + 𝜇𝜇⋅𝑠 𝑠𝑠𝑛𝑛(𝑒𝑒 I] 𝑛𝑛) ⋅𝒙𝒙[∗] OE 𝑛𝑛 𝑛𝑛+1 𝑛𝑛 1 ∶𝑒𝑒 L 𝑛𝑛> 0 𝑠 0 𝑠𝑠𝑛𝑛 (| 𝑒𝑒 𝑛𝑛 D= ∶𝑒𝑒 L 𝑛𝑛= 0 | −1 ∶𝑒𝑒 L 𝑛𝑛< 0 

- Of course less efficient than LMS but faster to compute. or 

- Others simplifications exists as **sign-data sign-sign.** 

17 

## **Normalized LMS** 

● One difficulty with LMS is the selection of the step size 𝜇𝜇 which define the rapidity of convergence. 

**==> picture [131 x 25] intentionally omitted <==**

**----- Start of picture text -----**<br>
𝜇𝜇 too small :<br>**----- End of picture text -----**<br>


**==> picture [89 x 26] intentionally omitted <==**

**----- Start of picture text -----**<br>
𝜇𝜇 good :<br>**----- End of picture text -----**<br>


**==> picture [120 x 25] intentionally omitted <==**

**----- Start of picture text -----**<br>
𝜇𝜇 too high :<br>**----- End of picture text -----**<br>


- Unfortunately, this value is signal dependent. It will depend of its amplitude and variance. A solution is NLMS. 

18 

## **Normalized LMS algo** 

● The Normalized LMS algorithm called NLMS is given by: 

**==> picture [417 x 78] intentionally omitted <==**

Where the signal is scaled by its squared norm. 

- Where 𝛽𝛽 is now bounded by : 0 < 𝛽𝛽< 2 

- ● If ε ≈1 ⋅10[−4] nel 𝑥𝑥 𝑛𝑛 is too small, we can use a constant 𝒙𝒙[∗] . 𝑛𝑛 

- 𝒘𝒘 = 𝒘𝒘 + 𝛽𝛽⋅ 𝑛𝑛 𝑛𝑛+1 𝑛𝑛 2[⋅𝑒𝑒] ε + ~~lim~~ 𝒙𝒙 𝑛𝑛 |° 2 

- ● NLMS requires more calculation because of nel 𝒙𝒙 𝑛𝑛 but can be evaluated recursively. 

**==> picture [689 x 34] intentionally omitted <==**

19 

## **Plan** 

- Introduction 

- FIR Adaptive filter 

## ● Recursive Least Square 

20 

## **Recursive Least Squares** 

- In previous adaptive filtering methods, the gradient descent is **minimizing the mean-square error** : 

2 n ξ [] = E{ IC 𝑒𝑒 𝑛𝑛 } n 𝒘𝒘 = 𝒘𝒘 −𝜇𝜇⋅∇ξ : 𝑛𝑛+1 𝑛𝑛 

● The difficulty with these methods is that they all require knowledge of the autocorrelation of the input process 𝑹𝑹 and 𝑥𝑥 the cross-correlation between the input and the desired output 𝒓𝒓 𝒅𝒅𝑥𝑥 n ∇ξ | | = −𝐸𝐸 tL] 𝑒𝑒 𝑛𝑛⋅𝒙𝒙 o6UL[∗] 𝑛𝑛 DG = −(𝐸𝐸 ttl 𝑑𝑑 𝑛𝑛⋅𝒙𝒙[∗] €B 𝑛𝑛 −𝐸𝐸 t 𝒘𝒘[𝑇𝑇] LIT) 𝑛𝑛𝒙𝒙 𝑛𝑛⋅𝒙𝒙[∗] tb 𝑛𝑛) 

**==> picture [67 x 28] intentionally omitted <==**

**==> picture [60 x 29] intentionally omitted <==**

21 

## **Recursive Least Squares** 

- When this statistical information is unknown, we have been forced to estimate these statistics from the data. 

- In the LMS adaptive filter, these ensemble averages are **estimated** using instantaneous values : 

∗ Ef{e[n]-x [ 𝑛𝑛 }} = 𝑒𝑒[𝑛𝑛] ⋅𝒙𝒙[∗] [ 𝑛𝑛 

- In some applications, this gradient may not converge rapidly or high excess mean-square error. 

22 

## **Recursive Least Squares** 

- An alternative is to consider error measures that do not include expectation and that maybe computed directly from the data. For example **minimizing a least-square error:** 

**==> picture [264 x 83] intentionally omitted <==**

- or 

- Requires no statistical information about x[n] d[n] and may be evaluated directly from x[n] and d[n] 

23 

## **Recursive Least Squares** 

## ● Can be slightly faster on stationary process than LMS 

24 

𝑇𝑇 

## **Exponentially weighted RLS** 

- Let us consider the design of a FIR filter 

**==> picture [390 x 39] intentionally omitted <==**

**==> picture [517 x 49] intentionally omitted <==**

- On non-stationary process, the **last samples are more important than the previous** . To deal with it, the **exponentially weighted least square error** is developed: 

**==> picture [656 x 73] intentionally omitted <==**

Where 0 < 𝜆𝜆≤1 is an exponential weighting (forgetting factor). 

25 

## **Exponentially weighted RLS** 

● 

To find the coefficients, we proceed in the same way than for LMS: 𝑛𝑛 𝑛𝑛 n 𝜕𝜕𝜀𝜀 𝜕𝜕𝑒𝑒 𝑠𝑠 ∗ 𝜆𝜆[𝑛𝑛−𝑖𝑖] 𝑒𝑒 𝑠𝑠 ∗ 𝜆𝜆[𝑛𝑛−𝑖𝑖] 𝑒𝑒 𝑠𝑠 𝑥𝑥[∗] [𝑠𝑠−𝑘𝑘] ~~a~~ ) ~~es~~ ) 𝜕𝜕𝑤𝑤𝑛𝑛[𝑘𝑘] 𝑖𝑖=0 𝜕𝜕𝑤𝑤𝑛𝑛[𝑘𝑘] 𝑖𝑖=0 𝑛𝑛 𝑝𝑝 = 𝜆𝜆[𝑛𝑛−𝑖𝑖] 𝑤𝑤 𝑙𝑙𝑥𝑥[𝑠𝑠−𝑙𝑙] 𝑥𝑥[∗] [𝑠𝑠−𝑘𝑘] 𝑛𝑛 » 𝑖𝑖=0 bata) - Y° 𝑙𝑙=0 7 𝑝𝑝−1 𝑛𝑛 𝑛𝑛 ⇒ 𝑤𝑤 𝑙𝑙 𝜆𝜆[𝑛𝑛−𝑖𝑖] 𝑥𝑥 𝑠𝑠−𝑙𝑙𝑥𝑥[∗] [𝑠𝑠−𝑘𝑘] 𝜆𝜆[𝑛𝑛−𝑖𝑖] 𝑑𝑑 𝑠𝑠𝑥𝑥[∗] [𝑠𝑠−𝑘𝑘] 𝑛𝑛 » 𝑙𝑙=0 aly 𝑖𝑖=0 _ =>. 𝑖𝑖=0 7 \-_>——__—_ 𝒓𝒓 [𝑛𝑛] 𝑹𝑹 [| 𝑛𝑛 𝒅𝒅𝒙𝒙 𝒙𝒙 𝑛𝑛 𝑛𝑛 𝒓𝒓 𝜆𝜆[𝑛𝑛−𝑖𝑖] 𝑑𝑑 𝑠𝑠𝒙𝒙[∗] [𝑠𝑠] 𝑹𝑹 𝜆𝜆[𝑛𝑛−𝑖𝑖] 𝒙𝒙[∗] 𝑠𝑠𝒙𝒙[𝑇𝑇] [𝑠𝑠] 𝒅𝒅𝒙𝒙 𝒙𝒙 in] =) C1 In] = > 7 𝑖𝑖=0 𝑖𝑖=0 [p x 1] [p x p] n — 𝜕𝜕𝜀𝜀 ∗ 𝑹𝑹 𝑛𝑛⋅𝒘𝒘 = 𝒓𝒓 [𝑛𝑛] 𝒙𝒙 𝒏𝒏 𝒅𝒅𝒙𝒙 𝜕𝜕𝑤𝑤 [𝑘𝑘][= 0 ⇒] 𝑛𝑛 

26 

## **Exponentially weighted RLS** 

● Since 𝑹𝑹 [| 𝑛𝑛 and 𝒓𝒓 [𝑛𝑛] depend on n, instead of solving the 𝑥𝑥 𝑑𝑑𝑥𝑥 deterministic normal equations, we will derive a recursion solution: 

𝒘𝒘 = 𝒘𝒘 + Δ𝒘𝒘 𝑛𝑛 𝑛𝑛−1 𝑛𝑛−1 

Where Δ𝒘𝒘 is a correction applied to solution at time n-1. Since: 𝑛𝑛−1 𝒘𝒘 = 𝑹𝑹 [| 𝑛𝑛𝒓𝒓 [𝑛𝑛] 𝑛𝑛 𝑥𝑥[−1] 𝒅𝒅𝒙𝒙 

The recursion is obtained by expressing 𝒓𝒓 [𝑛𝑛] in terms of 𝒓𝒓 [ 𝑛𝑛−1 𝑑𝑑𝑥𝑥 𝑑𝑑𝑥𝑥 and 𝑹𝑹 [| 𝑛𝑛 in terms of 𝑹𝑹 [ 𝑛𝑛−1 J and the new data vector 𝒙𝒙[𝑛𝑛] : 𝑥𝑥[−1] 𝑥𝑥[−1] 

𝒓𝒓 [| 𝑛𝑛= 𝜆𝜆𝒓𝒓 f 𝑛𝑛−1 J + 𝑑𝑑 C1] 𝑛𝑛⋅𝒙𝒙[∗] C1 𝑛𝑛 𝒅𝒅𝒙𝒙 𝒅𝒅𝒙𝒙 𝑹𝑹 [} 𝑛𝑛= 𝜆𝜆𝑹𝑹 Cf 𝑛𝑛−1 J + 𝒙𝒙[∗] C1 𝑛𝑛⋅𝒙𝒙[𝑇𝑇] 01 𝑛𝑛 𝑥𝑥 𝑥𝑥 

27 

## **Woodbury’s identity** 

● This mathematical Woodbury identity (eq 2.29, p.29, Stat. Dig., . Monson H.Hayes) is the central element in RLS efficiency. It can update the inverse covariance matrix without computing the complete inversion at each iteration : 

𝐴𝐴[−1] 𝑢𝑢𝑣𝑣[𝑇𝑇] 𝐴𝐴[−1] − ( 𝐴𝐴+ 𝑢𝑢𝑣𝑣[𝑇𝑇−1] ) = 𝐴𝐴[−1] __ 1 + 𝑣𝑣[𝑇𝑇] 𝐴𝐴[−1] 𝑢𝑢 B 𝑹𝑹 rf} 𝑛𝑛= C 𝜆𝜆𝑹𝑹 —T 𝑛𝑛−1 od + 𝒙𝒙[∗] td) 𝑛𝑛⋅𝒙𝒙[𝑇𝑇] ED 𝑛𝑛 −1 𝑥𝑥[−1] 𝑥𝑥 ee ee 𝑢𝑢 𝑣𝑣[𝑇𝑇] 𝐴𝐴 To simplify the notation, we write : 𝑷𝑷 Cy 𝑛𝑛= 𝑹𝑹 [𝑛𝑛] 𝑥𝑥[−1] 𝜆𝜆[−1] 𝑷𝑷 𝑛𝑛−1 𝑥𝑥 𝑛𝑛𝑥𝑥[𝑇𝑇] [𝑛𝑛]𝜆𝜆[−1] 𝑷𝑷 𝑛𝑛−1 − 𝑹𝑹 fr) 𝑛𝑛= 𝑷𝑷 𝑛𝑛= 𝜆𝜆[−1] 𝑷𝑷 𝑛𝑛−1 rT] — 𝑥𝑥[−1] po) St 1 + 𝑥𝑥[𝑇𝑇] [𝑛𝑛]𝜆𝜆[−1] 𝑷𝑷 𝑛𝑛−1 𝜆𝜆[−1] 𝑷𝑷 𝑛𝑛−1 𝑥𝑥 𝑛𝑛 − 𝑹𝑹 𝑛𝑛= 𝑷𝑷 𝑛𝑛= 𝜆𝜆[−1] 𝑷𝑷 𝑛𝑛−1 𝑛𝑛−1 𝑥𝑥[−1][𝑥𝑥][𝑇𝑇][[𝑛𝑛] 𝑷𝑷] 1 + 𝑥𝑥[𝑇𝑇] [𝑛𝑛]𝜆𝜆[−1] 𝑷𝑷 𝑛𝑛−1 f] oI ir | —— | 

## **Exponentially weighted RLS** 

**==> picture [519 x 105] intentionally omitted <==**

## ● And finally, the filter coefficients are: 

**==> picture [225 x 33] intentionally omitted <==**

● By replacing 𝑹𝑹 [𝑛𝑛] and 𝒓𝒓 [ 𝑛𝑛 | by the recursive version : 𝑥𝑥[−1] 𝒅𝒅𝒙𝒙 𝑹𝑹 [] 𝑛𝑛= 𝑷𝑷 ©] 𝑛𝑛 and 𝒓𝒓 [ 𝑛𝑛= 𝜆𝜆𝒓𝒓 | rf 𝑛𝑛−1 J] + 𝑑𝑑 €) 𝑛𝑛⋅𝒙𝒙[∗] © 𝑛𝑛 𝑥𝑥[−1] 𝒅𝒅𝒙𝒙 𝒅𝒅𝒙𝒙 ● The filter coefficients are then computed : 

**==> picture [881 x 180] intentionally omitted <==**

## **Exponentially weighted RLS** 

● Finally, recognizing that 𝑷𝑷 Cr 𝑛𝑛−1 J] 𝒓𝒓 — 𝑛𝑛−1 J = 𝒘𝒘 it follows that 𝒅𝒅𝒙𝒙 𝑛𝑛−1 𝑻𝑻 𝒘𝒘𝑛𝑛 = 𝒘𝒘𝑛𝑛−1 + 𝒈𝒈[𝑛𝑛] | 𝑑𝑑 [ 𝑛𝑛−𝒘𝒘𝑛𝑛−1𝒙𝒙[𝑛𝑛] | 

## ● Which may be written as 

𝒘𝒘 = 𝒘𝒘 + 𝛼𝛼 𝑛𝑛⋅ 𝒈𝒈[𝑛𝑛] 𝑛𝑛 𝑛𝑛−1 

## Where: 

𝑻𝑻 𝛼𝛼 L 𝑛𝑛 | is the a priori error (using previous coeff.): 𝛼𝛼 [ 𝑛𝑛= 𝑑𝑑 | [ 𝑛𝑛−𝒘𝒘 | 𝒙𝒙[𝒏𝒏] 𝒏𝒏−𝟏𝟏 𝒈𝒈[𝑛𝑛] is the gain vector 

30 

## **Exponentially weighted RLS implementation** 

## Parameters: 

 p : number of coefficient (filter order +1) 

 λ : Exponential weighting factor 

 𝛿𝛿 : value used to initialize **P** [0] Initialization: 

 𝒘𝒘0 = 𝟎𝟎 

 𝑷𝑷[0] = 𝛿𝛿[−1] 𝑰𝑰 

## Computation: 

## For n = 1,2,… compute 

𝐳𝐳 [1] 𝑛𝑛= 𝑷𝑷 [ 𝑛𝑛−1 1] ⋅𝒙𝒙[∗] 01 𝑛𝑛 _ 𝑝𝑝𝑥𝑥1 = [𝑝𝑝𝑥𝑥𝑝𝑝] [𝑝𝑝𝑥𝑥1] [𝑝𝑝𝑥𝑥1] 𝒛𝒛 L 𝒏𝒏 | = _#gain vector_ 𝒈𝒈 L 𝑛𝑛 [𝑝𝑝𝑥𝑥1] = __ [1 𝑥𝑥1] + [1 𝑥𝑥𝑝𝑝][𝑝𝑝𝑥𝑥1] | 𝜆𝜆+𝒙𝒙[𝑇𝑇] ~~LIU]~~ 𝑛𝑛𝒛𝒛 𝒏𝒏 𝑻𝑻 = _#a priori error_ 𝛼𝛼 𝑛𝑛= 𝑑𝑑 𝑛𝑛−𝒘𝒘 𝒙𝒙[𝑛𝑛] 1 𝑥𝑥1 1 𝑥𝑥1 −[1 𝑥𝑥𝑝𝑝][𝑝𝑝𝑥𝑥1] 𝑛𝑛−1 LJ 6 6L] cr JtJ = + 𝒘𝒘 = 𝒘𝒘 + 𝛼𝛼 𝑛𝑛𝒈𝒈 𝑛𝑛 𝑝𝑝𝑥𝑥1 𝑝𝑝𝑥𝑥1 1 𝑥𝑥1 𝑝𝑝𝑥𝑥1 _#filter coefficient update_ 𝑛𝑛 𝑛𝑛−1 LJ U4] f J f£ JE Wt J 1 _#inverse autocorrelation_ 𝑝𝑝𝑥𝑥𝑝𝑝= 𝑝𝑝𝑥𝑥𝑝𝑝−[𝑝𝑝𝑥𝑥1][1 𝑥𝑥𝑝𝑝] 𝑷𝑷 𝑛𝑛= 𝑷𝑷 𝑛𝑛−1 −𝒈𝒈 𝑛𝑛⋅𝒛𝒛[𝑻𝑻] 𝑛𝑛 Cf] ~~-~~ 𝜆𝜆 [t J C1 Cie ie _matrix update_ 

31 

## **Example Linear Prediction non stationary process example (9.4.2)** 

## ● Comparison between LMS and RLS for non-stationary process 

32 

## **LMS versus RLS** 

## ● This table summarizes the key differences between the two types of algorithms: 

|**LMS algorithm**|**RLS algorithm**|
|---|---|
|**Simple and can be easily applied**|**Increased complexity and computational cost**|
|**Takes longer to converge**|**Faster to converge**|
|Adaptation is based on the gradient-based approach<br>that updates filter weights to converge to the minimum<br>filter weights|Adaptation is based on the recursive approach that finds<br>the filter coefficients that minimize a weighted linear<br>least squares cost function relatingto the input signals.|
|Larger steady state error with respect to the unknown<br>system.|Smaller steady state error with respect to unknown<br>system.|
|**Does not account for past data.**|**Accounts for past data from the beginning to the**<br>**current datapoint.**|
|Objective is to minimize the current mean square error<br>between the desired signal and the output.|Objective is to minimize the total weighted squared error<br>between the desired signal and the output.|
|No memory involved. Older error values play no role in<br>the total error considered.|Has infinite memory. All error data is considered in the<br>total error. Using the forgetting factor, the older data can<br>be de-emphasized compared to the newer data.<br>Since 0 ≤_λ_< 1, applying the factor is equivalent to<br>weighting the older error.|



## _src :  Mathworks_ 

33 

## **Sliding window RLS** 

2 ● **When** 𝝀𝝀= 𝟏𝟏 **,** RLS algo has a growing window and each I 𝑒𝑒 Ll 𝑠𝑠 , 𝑠𝑠= n 0, … , 𝑛𝑛 are equally weighted, being the current time index 2 ● **When** i that are 𝝀𝝀< 𝟏𝟏 **,** IL 𝑒𝑒 𝑠𝑠 dl become less important form values of n small compared to (forgetting factor). 

- In both case, RLS algo **requires infinite memory** in the sense that all the data beginning from time n=0 will affect the coefficients w[n] 

- Example of non-stationary process where 𝜆𝜆= 1 is not able to track. 

_src : figure926_*.mlx_ 

34 

## **Sliding window RLS** 

- **For non-stationary process** , a small value of 𝜆𝜆 (small horizon) is necessary. Or minimizing the squared error on a finite length : L 

**==> picture [674 x 121] intentionally omitted <==**

- If L= 0 → it results to LMS algorithm 

- This small modification by introducing L is adding more complexity in the calculations than RLS (see next page). 

- It requires about **twice the number of multiplications** and additions, and requires p+L values of x[n] to be stored. 

35 

## **Sliding window RLS** 

## ● 

## The sliding window is modifying the update equation: 

**Step 1** 

𝑷𝑷 𝑛𝑛−1 𝒙𝒙[∗] 𝑛𝑛 = 𝒈𝒈 Ld 𝑛𝑛+ 1 rod 1 + 𝒙𝒙[𝑇𝑇] fll. 𝑛𝑛𝑷𝑷 𝑛𝑛−1 4 𝒙𝒙[𝑛𝑛][+][ 𝒈𝒈] 𝑛𝑛⋅ 𝑑𝑑 𝑛𝑛−𝒘𝒘 ⋅𝒙𝒙[∗] 𝑛𝑛 w 𝑛𝑛[=][ 𝒘𝒘] 𝑛𝑛−1 CL] [0] 𝑛𝑛−1 [ ]| = − Pnti] 𝑷𝑷 £— 𝑛𝑛−1 | 𝒈𝒈 C1 𝑛𝑛 𝒙𝒙[𝑇𝑇] TI 𝑛𝑛𝑷𝑷[𝑛𝑛−1] 

**Step 2** 

**==> picture [642 x 183] intentionally omitted <==**

36 

