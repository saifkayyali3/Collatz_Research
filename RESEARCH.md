# The Collatz Multiverse: *qn+r* Conjecture Research Log

## Research Tool: The Universal Engine
My research is powered by a custom Python-based ["Deep Search"](Deep-Search.py) tool capable of:
1. **Infinite Precision:** Handling numbers with 1,000,000+ digits.
2. **Cycle Detection:** Tracking every state to find loops in any system.
3. **Divergence Guarding:** Automatically stopping if a number grows exponentially.

## Key Experiments

### 1. The 3n-1 "Mirror" System
Contrary to the 3n+1 Collatz conjecture, 3n-1 contains multiple domains of attraction:
* **The 1-Loop:** The primary target [2, 1].
* **The 5-Loop:** A 5-step cycle [14, 7, 20, 10, 5].
* **The 17-Loop:** A complex 18-step loop. [17, 50, 25, 74, 37, 110, 55, 164, 82, 41, 122, 61, 182, 91, 272, 136, 68, 34].
* **The Negative Mirror:** Discovered the [-4, -2, -1] loop using $n = -773$.

**Conclusion:** $3n-1$ on positive integers is a perfect mirror of $3n+1$ on negative integers, exhibiting identical loop structures with inverted signs.

### 2. High-Magnitude Verification
Tested $2.756 \times 10^{67}$. 
* **Discovery:** Using floating-point notation in GUIs causes a "Precision Cliff," leading to false loops.
* **Verification:** Using full integers, the value successfully reached 1 in **1046 steps**.

### 3. Edge Cases
* **The Centurion Number:** 983,232 reached 1 in exactly **100 steps** in the $3n-1$ conjecture (on GUI it says 101 because it counts an extra step).
* **The Boundary Shift:** 983,233 (only 1 higher) was captured by the 5-loop in **96 steps** in the $3n-1$ conjecture.

## 4. The $4n+8$ "Plummet" Phenomenon
### 4.1 The Mechanism
Every tested negative number follows a predictable two-phase life cycle:

-The Ascent: The $+8$ constant is powerful enough to "lift" negative numbers toward $0$.

-The Breach: If a number reaches $1$, it triggers the $n/2$ rule.

-The Plummet: Once the value crosses into the positive commencement, the $4n+8$ multiplier overpowers the $n/2$ division, causing the number to diverge toward infinity, and all negative numbers interestingly enough plummet in the same trajectory as they all diverge at 1 and go up from there all the same.

### 4.2 Case Study: (-786,678)

*Starting Point: $-786,678$*

#### Behavior: Climbed steadily for over 500,000 steps. (For you nerds, it is 590,011 steps exactly)

#### The Climax: Reached the value $1$.

#### The Terminal Event: Immediately following the success at $1$, the sequence enters a divergent loop where the $4n$ multiplier causes an exponential explosion.

---

## 5 The Interesting $-3n+81$ Conjecture:
### 5.1: The $0$ Attraction:

This attractor is one of the strongest attractors in the below-100 range, but it does disappear gradually as numbers increase.

### 5.2: The $81$ Loop:
Beyond the low-magnitude influence of the 0 Attraction, the system is dominated by Loop 81. 
* Loop Members: $[81, -162, -81, 324, 162, 81]$ which is a 5 step loop. (Note: The $-3n+81$ rule creates a unique positive-to-negative yoyo affect).

* Statistical Weight: In a demographic of $1,000,000$ integers, the $81$ loop captured 79.67% of all trajectories, making it of the strongest attractors in this conjecture.

### 5.3: The $1053$ Loop:
A secondary, more complex attractor exists at 1053:

* Loop Cycle: [1863, -5508, -2754, -1377, 4212, 2106, 1053, -3078, -1539, 4698, 2349, -6966, -3483, 10530, 5265, -15714, -7857, 23652, 11826, 5913, -17658, -8829, 26568, 13284, 6642, 3321, -9882, -4941, 14904, 7452, 3726]

* Statistical Weight: In a demographic of $1,000,000$ integers, the $1053$ loop captured 20.14% of all trajectories, further instilling how strong of an attractor it is.

### 5.4: The Macro-Scale Verification:
To test if there is any possible divergence that may occur, I tested numbers with 1000 decimal digits using a the [Titan Hunter](Titan-Test.py), here are the results:

* Positive Titan: ($2.97 \times 10^{999}$) which reached the $81$ loop in 18,034 steps.

* Negative Titan: ($-2.6 \times 10^{999}$) which reached the $81$ loop in 17,459 steps.

* Conclusion: Even at the cosmic scale, the system is sub-critical. Magnitude is dismantled at a rate of roughly 1 decimal digit every 23.7 steps. No Escape Velocity exists; every giant eventually falls.

### 5.5: The $1,000,000$ and $-1,000,000$ Scales Verification:
This experiment involved testing all numbers from 1 to 1,000,000 and all numbers from -1 to -1,000,000 to see if any divergence may appear, here are the results:

|                            | The 81 Loop |  The 1053 Loop |  The 0 Attraction |
|----------------------------|-------------|----------------|-------------------|
| Negative Million Frequency |  78.1%      |  21.3%         |  0.6%             |
| Positive Million Frequency |  79.67%     |  20.14%        |  0.19%            |
| +- Ratio                   | - 1.57      |  + 1.16        |  + 0.41           |

As we can see from the table, there barely is a difference between the frequency of loops in the positive and negative fields.

Tool used in this experiment: [Million Tester](Million-Test.py)

Conclusion: it doesn't matter the difference in signs in this conjecture due to numbers jumping from negative to positive with each step.



### 5.6: The Twin Monsters:

During this experiment, I tried to see which numbers in both the positive and negative fields took the most steps to get to their respective loops, the results are rather interesting:

| Number   | Number of Steps | Peak Magnitude (Distance from 0) | Coordinate of Peak Magnitude | Loop Number Entered |
|----------|-----------------|----------------------------------|------------------------------|---------------------|
| 700,797  | 397 steps       | 6,384,747,888                    | -6,384,747,888               | 81                  |
| -934,342 | 400 steps       | 6,384,747,888                    | -6,384,747,888               | 81                  |

As we can see, they both had their largest distance from 0 be the same magnitude of $6,384,747,888 $ and even the same coordinate of $-6,384,747,888$ and coincedentally, they entered the same loop but that is expected as on both scales, positive and negative, it is nearly an 80% chance of entering the $81$ loop.

### 5.7: The Conclusion:
All in all, these results clearly show that, at least till the $10^{4}$ range on both the positive and negative scales, there is no divergence and there always is an attraction to either the $81$ loop, $1053$ loop or the number $0$.

---

# Note: The statements above aren't absolutely true, just observations I made 
## Contributions to the Research can be made below via pull requests or forking:
### Note: Please add your Github username next to your topic's title, thanks!
---

# 1: