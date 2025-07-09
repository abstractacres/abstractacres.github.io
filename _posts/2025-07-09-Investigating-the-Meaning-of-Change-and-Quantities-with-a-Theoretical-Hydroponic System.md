![alt text](/assets/hydro-garden.png)
## Introduction to the Problem
As I work my way through Khan Academy's Calculus 2 curriculumn, I intend to take the parts that inspire me and apply them to the field of agriculture by designing and solving a problem with the help of Gemini AI.

In the Khan Academy article, ["Exploring accumulation of change"](https://www.khanacademy.org/math/calculus-2/cs2-integrals-review/cs2-accumulations-of-change-introduction/a/accumulation-and-net-change-in-context), there is a reminder to distinguish between the net change of a quantity and the value of an actual quantity.

Consider a farmer monitoring nitrate (NO<sub>3</sub><sup>-</sup>) concentrations in their hydroponic system. Over the course of 24 hours, let $R(t)$ be the rate nitrate is added to the system and let $C(t)$ be the rate nitrate is consumbed by plants and is lost to evaporation. 

$$R(t) = 0.5 + 0.3sin(\frac{\pi t}{12})\:ppm/hr$$

$$C(t) = 0.2 + 0.1cos(\frac{\pi t}{6})\:ppm/hr$$

![alt text](/assets/nutrient_rates_plot.png)

With this information you can calculate the **change** in concentration of nitrate in the system, for any period of time in between $t=0$ and $t=24$, but you cannot know the **quantity** of nitrate in the system at any point in time without knowing the initial concentration of nitrate or the **initial condition**.

Assuming the initial concentration of NO<sub>3</sub><sup>-</sup> in the system at $t=0$ was 150 ppm of NO<sub>3</sub><sup>-</sup>, what is the actual NO<sub>3</sub><sup>-</sup> concentration at noon ($t=12$)?

## Subtracting functions

To calculate the net change of NO<sub>3</sub><sup>-</sup> concentration in the system, we can employ algebra to substract the rate NO<sub>3</sub><sup>-</sup> is leaving the system from the rate NO<sub>3</sub><sup>-</sup> is entering the system. 

Net rate of change: 

$$N(t) = R(t) - C(t)$$

$$= (0.5 + 0.3sin(\frac{\pi t}{12})) - (0.2 + 0.1cos(\frac{\pi t}{6}))$$

$$= 0.3 + 0.3sin(\frac{\pi t}{12}) - 0.1cos(\frac{\pi t}{6})$$

## Using the Sum and Difference Rule to Integrate Terms in a Function Seperately

The sum and difference rule tells us the difference or sum of functions is the difference or sum of their individual derivatives. This also applies to integration. According to Open Stax's Calculus 1 book, [Section 4.10 Antiderivatives](https://openstax.org/books/calculus-volume-1/pages/4-10-antiderivatives?query=%22sum%20and%20difference%22&target=%7B%22index%22%3A0%2C%22type%22%3A%22search%22%7D#fs-id1165043393659), if $F$ and $G$ are antiderivatives of $f$ and $g$, and $k$ is any real number then:

$$\int f(x) \pm g(x) dx = F(x) \pm G(x) + C$$

The sum and difference rule allows us to break down one long integration problem

$$\int_0^{12} N(t)\, dt= \int_0^{12} 0.3 + 0.3sin(\frac{\pi t}{12}) - 0.1cos(\frac{\pi t}{6})\, dt$$

into three sizeable chunks:

$$= \int_0^{12} 0.3\,dt+ \int_0^{12} 0.3sin(\frac{\pi t}{12})\,dt + \int_0^{12} 0.1cos(\frac{\pi t}{6})\, dt$$

For now, we'll surpress the bounds:

$$= \int 0.3\,dt+ \int 0.3sin(\frac{\pi t}{12})\,dt + \int0.1cos(\frac{\pi t}{6})\, dt$$

## Using the Constant Rule for Integration

To integrate the first term in  our Net Change in NO<sub>3</sub><sup>-</sup> Concentration function, we must use the constant rule for integration. If $k$ is a constant, then:

$$\int k\,dx = kx + C$$

Therefore:

$$\int 0.3\, dt= 0.3t + C$$

We can ignore the constant $C$ because we are evaluating a definite integral. Remember, we are temporarily surpessing the bounds of our integral, $t=0$ and $t=12$.

## Focusing on the Derivation Component of U-Substition

To integrate the second term of the function, we must use $u$ substitution. 

Let $u= \frac{\pi t}{12}$

For the function to be completely in terms of $u$, we must find the derivative of $u$.

$\frac{d}{dx}\left[\frac{\pi t}{12}\right] = du$

To make the constant more of apparent we can the rewrite the expression as the following:

$\frac{d}{dx}\left[(\frac{\pi}{12})t\right] = du$

The power rule states that for any function $f(x)=x^n$, the derivative is:

$$\frac{d}{dx}\left[x^n\right] = nx^{(n-1)}$$

Therefore:

$$\frac{d}{dx}\left[(\frac{\pi}{12})t\right] = 1 * \frac{\pi}{12} t^{(1-1=0)}= \frac{\pi}{12}$$

Our value for $du$ is $\frac{\pi}{12}$ and in differntial form it is written as

$$du= \frac{\pi}{12}dt$$

which can be rearranged to 

$$dt= \frac{12}{\pi}du$$

## Integrating the 2nd and Final Term

The second term, $\int 0.3sin(\frac{\pi t}{12})\,dt$, in terms of $u$ is the following:

$$\int 0.3 sin(u)\frac{12}{\pi}\,du$$

We can bring the constants in front of the integral due to the [rule of linearity](https://math.mit.edu/~djk/calculus_beginners/chapter03/section03.html):

$$0.3* \frac{12}{\pi}\int sin(u)\frac{12}{\pi}\,du$$

Knowledge of basic integration functions such as

$$\int sin(x)dx = -cos(x) +C$$

allows us to arrive to

$$-\frac{3.6}{\pi} cos(u)$$

and to finish the process of integration we resubstitute $\frac{\pi}{12}$ for $u$:

$$-\frac{3.6}{\pi}cos(\frac{\pi}{12})$$

The process we used to integrate the second term of our Net Change in NO<sub>3</sub><sup>-</sup> Concentration function, can be used to integrate the final term.

$$\int -0.1cos(\frac{\pi t}{6})\, dt = -\frac{0.6}{\pi}sin(\frac{\pi t}{6})$$

## Combining Antiderivatives and Evaluating the Integral

To evalulate the integral of our Net Change in NO<sub>3</sub><sup>-</sup> Concentration function, we must combine our three antiderivatives.

$$\left[0.3t - \frac{3.6}{\pi}cos(\frac{\pi t}{12})-\frac{0.6}{\pi}sin(\frac{\pi t}{6})\right]_0^{12}$$

Using a calculator and rounding to the nearest tenth place, at $t=0$ (the beginning of the day) the value is $-1.15$ ppm. At $t=12$ (the afternoon) the value is $4.75$ ppm. Substracting the value at $t=12$ from the value at $t=0$ will result in the Net Change in NO<sub>3</sub><sup>-</sup> Concentration.

$$ 4.75 - (-1.15) = 5.9\: ppm$$

## Remembering the Initial Condition

The original question asks for the actual quantity of NO<sub>3</sub><sup>-</sup> concentration in the hydroponic system at noon. $5.9$ ppm is the quantity of change. We must add the initial condition, $150$ ppm, to the quantity of change to solve for the actual quantity. Our final answer is:

$$155.9\,ppm$$

## Conclusion

I did not orignally imagine this blogpost would be as expansive as it is, and still I skipped many oppurtunties to explain my thinking. My math courses thus far have not required us to explain what we understand, but only perform. If there are any errors in my work, I welcome feedback. Additionally, if there are any nuances or complexities to be added to our theoretical hydroponics system, please share. 






