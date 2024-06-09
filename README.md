# SF2701 TI-84 calculator programs

This repository contains TI-84 calculator programs for the course SF2701 Financial Mathematics, Basic Course at KTH Royal Institute of Technology. The programs are highly aligned to the exam questions and could save a lot of time for you in your exam. All progrmas are my original work. Use the programs on your own risk, the author takes no resonsibility.

## How to use
1. Download **TI Connect™ CE** from the [official website](https://education.ti.com/en/products/computer-software/ti-connect-ce-sw) and install it on your computer.
2. Follow the instructions to transfer the programs to your calculator.
3. On your calculator, press **PRGM** to display the **PRGM EXEC** menu. The programs in your calculator will appear in this menu. Select the program you want to use and press **ENTER**.
4. Enter the value of variables of your question. See specific instructions for the programs below. 
5. Get the answer. 

## Program 
All programs starting with "A" are for the binomial models which is usually the first exam quesion.


### ACOMP
**This program must be executed first before executing any other programs for binomial models, since the other programs rely on the variables defiend by this program.**

Convert continuous compounding interest rate to the variables used in the binomial model. 
#### Input variables
| Variable | Description |
| -- | ----------- |
| $\Delta t$ | Length of time step in years. |
| $\sigma$ | Volatility per annum. |
| $r$ | Continuouns compounding interest rate per annum. |

#### Output
$u$, $d$, $q$, $1+R$.

### APRICEST
Computes the price tree of the risky asset in a binomial model with discrete proportional dividends. 
#### Input variables
| Variable | Description |
| -- | ----------- |
| $T$ | Number of periods. |
| $s$ | Initial price of the risky asset. |
| $\delta$ | Dividends rate per time step. Set to 0 if there is no dividends. |

#### Output
The price tree of the risky asset, starting from $t=0$. Each row represents one scenario in the format $\\{S_{t-}, S_t \\}$. "---" represents that this time step is done and you need to press enter to start the next time step.

### APRICEX
Computes the price tree of an European/American call/put option in a binomial model with discrete proportional dividends.

For American call options, exercise will always happend before dividend payment.\
For American put options, exercise will always happend after dividend payment.
#### Input variables
| Variable | Description |
| -- | ----------- |
| $T$ | Number of periods. |
| $s$ | Initial price of the risky asset. |
| $K$ | Strike. |
| $\delta$ | Dividends rate per time step. Set to 0 if there is no dividends. |

#### Output
The price tree of the selected option, starting from $t=T$. Each row represents one scenario. 
For American options the first number is price if exercise and the second number is the price if keep the option.
You need to figure out by yourself when to exercise.
"---" represents that this time step is done and you need to press enter to start the next time step.
The price at $t=0$ is the last displyed number.


### APORT
Computes the replicating portfolio of an European/American call/put option in a binomial model **without** dividends.

For American call options, exercise will always happend before dividend payment.\
For American put options, exercise will always happend after dividend payment.
#### Input variables
| Variable | Description |
| -- | ----------- |
| $T$ | Number of periods. |
| $s$ | Initial price of the risky asset. |
| $K$ | Strike. |

#### Output
The replicating portfolio of the selected option, starting from $t=T$. Each row represents one scenario in the format $\\{V^h_t, x_t,  y_t \\}$.
"---" represents that this time step is done and you need to press enter to start the next time step.




### BBS
Computes the price of an European call or put option under the Black Scholes market model.

### BIMPVOL
Estimates the volatility of the Black Scholes market model using the price of a European call option.

### CZR2ZP
Computes zero bond prices from term structure.

### CBP2ZR
Computes the term structure from price of zero coupon bonds and fixed coupon bonds.

### CINTDEVS
There are multiple functions
- Zero coupon bond price: Compute the price of a zero coupon bond with maturity $T$ and strike $K$
- Fixed coupon bond price: Compute the price of a fixed coupon bond with maturity $T$, strike $K$ and coupon $c$
- FRA price: Compute the price of forward rate agreement (FRA) with continuous rate $r$ where money is borrowed at $T_1$ and returned at $T_2$.
- Fixed coupon rate: Computes the continuous spot rate $r$ of a fixed coupon bound given maturity $T$, strike $K$ and price of the fixed coupon bond $P$.
- FRA rate: Computes the continuous rate $r$ of a forward rate agreement.
- Swap price: Computes the value of a swap viewed from the part paying fixed coupon. $R$ is the simple annual swap rate; $Tmax-t$ is the number of remaining payments. $r(t,T)$ from $T=t+1$: zero rates for the remaining payments.
- Swap rate: Computes the swap rate of a swap quoted per annum using simple annual compounding.

## Examples
### Homework 1 spring 2018 1(a)
![image](https://github.com/XindiLiu/SF2701-calculator-programs-for-TI-84/assets/84523198/e4d93a6c-5992-4501-bd85-5efe1d94d267)

| Progam screenshot | Official solution |
| -- | -- |
|![!](/examples/2018HW1-1a-ACOMP1.png) ![!](/examples/2018HW1-1a-ACOMP2.png)|![image](https://github.com/XindiLiu/SF2701-calculator-programs-for-TI-84/assets/84523198/4a1826e6-dd2f-488f-a143-73835051a0c2)|
|![!](/examples/2018HW1-1a-APRICEST1.png) ![!](/examples/2018HW1-1a-APRICEST2.png) ![!](/examples/2018HW1-1a-APRICEST3.png) ![!](/examples/2018HW1-1a-APRICEST4.png) ![!](/examples/2018HW1-1a-APRICEST5.png)|![image](https://github.com/XindiLiu/SF2701-calculator-programs-for-TI-84/assets/84523198/f3fa88a8-1384-48ed-b4b8-e239ca45dbc6)|
|![!](/examples/2018HW1-1a-APRICEX1.png) ![!](/examples/2018HW1-1a-APRICEX2.png) ![!](/examples/2018HW1-1a-APRICEX3.png) ![!](/examples/2018HW1-1a-APRICEX4.png) ![!](/examples/2018HW1-1a-APRICEX5.png) ![!](/examples/2018HW1-1a-APRICEX6.png)|![image](https://github.com/XindiLiu/SF2701-calculator-programs-for-TI-84/assets/84523198/92543a94-c384-47ea-bf98-a4245f41edb5)|
|![!](/examples/2018HW1-1a-APORT1.png) ![!](/examples/2018HW1-1a-APORT2.png) ![!](/examples/2018HW1-1a-APORT3.png) ![!](/examples/2018HW1-1a-APORT4.png) ![!](/examples/2018HW1-1a-APORT5.png)|![image](https://github.com/XindiLiu/SF2701-calculator-programs-for-TI-84/assets/84523198/c2ad4e78-b8fe-433f-8ca1-b16a0c772859)|

### Exam 2020-05-27 3
![image](https://github.com/XindiLiu/SF2701-calculator-programs-for-TI-84/assets/84523198/e987043f-fd61-4883-b52c-c1ac5b0e2bd2)

a) Use CBP2ZR

![!](/examples/20200527-3A-CBP2ZR1.png)
![!](/examples/20200527-3A-CBP2ZR2.png)
![!](/examples/20200527-3A-CBP2ZR3.png)
![!](/examples/20200527-3A-CBP2ZR4.png)
![!](/examples/20200527-3A-CBP2ZR5.png)
![!](/examples/20200527-3A-CBP2ZR6.png)
![!](/examples/20200527-3A-CBP2ZR7.png)

Answer: $r(0, 1) = 0.030, r(0, 2) = 0.035, r(0, 3) = 0.040$

b) Use CINTDEVS, FRA rate

![!](/examples/20200527-3B-CINTDEVS1.png)
![!](/examples/20200527-3B-CINTDEVS2.png)

Answer: $0.049$

c) Use CINTDEVS, Swap price

![!](/examples/20200527-3C-CINTDEVS1.png)

Answer: $-15468$
