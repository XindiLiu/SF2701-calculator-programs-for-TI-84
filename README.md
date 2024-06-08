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
- $\Delta t$: The length of time step in years.
- $\sigma$: The volatility per annum.
- $r$: The continuouns compounding interest rate per annum.

| Variable | Description |
| -- | ----------- |
| $\Delta t$ | Length of time step in years. |
| $\sigma$ | Volatility per annum. |
| $r$ | Continuouns compounding interest rate per annum. |

#### Output
$u$, $d$, $q$, $1+R$.

#### Example

### APRICEST
Computes the price tree of the risky asset in a binomial model with discrete proportional dividends. 
#### Input variables
| Variable | Description |
| -- | ----------- |
| $T$ | Number of periods. |
| $s$ | Initial price of the risky asset. |
| $\delta$ | Dividends rate per time step. Set to 0 if there is no dividends. |

- $T$: The number of periods.
- $s$: The initial price of the risky asset.
- $\delta$: The dividends rate per time step. Set to 0 if there is no dividends.

#### Output
The price tree of the risky asset, starting from $t=0$. Each row represents one scenario in the format $\\{S_{t-} / S_t \\}$. "---" represents that this time step is done and you need to press enter to start the next time step.

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

- $T$: The number of periods.
- $s$: The initial price of the risky asset.
- $\delta$: The dividends rate per time step. Set to 0 if there is no dividends.

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

- $T$: The number of periods.
- $s$: The initial price of the risky asset.
- $\delta$: The dividends rate per time step. Set to 0 if there is no dividends.

#### Output
The replicating portfolio of the selected option, starting from $t=T$. Each row represents one scenario in the format $\\{x_t / y_t \\}$.
"---" represents that this time step is done and you need to press enter to start the next time step.

## Example part 1


