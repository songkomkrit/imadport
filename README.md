# IMADPort
```IMADPort``` is portfolio software to obtain bounds on optimal portfolios when future asset returns are bounded and the risk measure is the mean absolute deviation (MAD).

## Interval Portfolio Theory
A financial asset not limited to a stock has a change in its value over time and can generate either a loss or a profit. Since its future, usually one-period ahead, price is not perfectly predictable, the investment risk which measures the deviation, using its historical asset returns dating back time periods, of its realized return from its expected value plays an important role in asset selection. A portfolio including multiple assets of different characteristics aims to mitigate this particular risk.

In addition to a future asset return, its expected value is also uncertain. This is attributable to the existence of several good estimates beyond the arithmetic mean of past asset returns. All of these candidates may form a closed interval, optimal portfolios exist, and asset allocation is suggested through bounds, not single values as usual. Intuitively, a good investment strategy should guarantee a minimum rate of return specified by an investor. This becomes a portfolio constraint. An optimal portfolio usually attains a return more than this threshold.

A portfolio risk should also be minimized because an investor prefers an actual return as close to an expected return as possible. Any value of this magnitude is equally important; therefore, the mean absolute deviation (MAD) should be employed as a risk measure. The rigorous derivation of bounds on optimal MAD portfolios (Chaiyakan & Thipwiwatpotjana, [2019](https://link.springer.com/chapter/10.1007/978-3-030-14815-7_19), [2021](https://link.springer.com/article/10.1007/s10287-021-00392-x)) heavily relies on mathematical tools such as the foundation of interval linear programming (see [Fiedler, Nedoma, Ramík, Rohn, & Zimmermann, 2006](https://link.springer.com/book/10.1007/0-387-32698-7); Hladík, [2009](https://link.springer.com/article/10.1007/s10700-009-9060-7), [2012](https://kam.mff.cuni.cz/~hladik/doc/2012-conf-MME-ILPcontr.pdf), for example) and the concept of basis stability ([Hladík, 2014](https://link.springer.com/article/10.1007/s11590-012-0589-y); [Rohn, 1993](https://www.sciencedirect.com/science/article/abs/pii/016763779390077T)).

## Releases
As the initial versions, the ```IMADPort``` software is built dynamically and lacks a graphical user interface (GUI) to hightlight its mere functionality and, more importantly, to have small file size. MATLAB runtime (MCR)&mdash;a set of shared libraries&mdash;must be loaded into memory at the start of the program, leading to the slightly slow initial load time of the program. Furthermore, the CLI deployment provides more flexibility than the sole GUI; it facilitates through scripting the automation of obtaining bounds on optimal portfolios of different types.

The program can run on all three 64-bit operating systems: Windows (AMD64 or x64), macOS (Apple Silicon), and Linux (AMD64 or x64). It requires the following components of the MATLAB runtime (MCR) R2026a: MATLAB Base Runtime, MATLAB Standard Runtime Addon, MATLAB Graphics Runtime Addon, and Optimization Toolbox Runtime Addon.

Developed by MathWorks, MATLAB R2026a, if preinstalled, comes with this runtime. Unlike the MATLAB software, the [official MCR](https://www.mathworks.com/products/compiler/matlab-runtime.html) itself is available for free. Nonetheless, the MCR under this approach is considerably large and has a size of at least 10 GB because all components beyond requirements are installed. To save disk space, the *minimal* online MCR installer is also separately provided by the developer of the ```IMADPort``` software. Through this installation method, only four MCR dependencies above with a total size of approximately 2 GB are fetched from MathWorks servers and installed.

The ```IMADPort``` directory and the MCR directories should be prepended to the PATH and library path environment variables, respectively. This setup varies based on an operating system. Paths are separated by a semicolon on Windows but a colon on both macOS and Linux. Please refer to the *latest user manual* for path setup and program usage in detail.

## References
Chaiyakan, S., & Thipwiwatpotjana, P. (2019). Mean absolute deviation portfolio frontiers with interval-valued returns. In H. Seki, C. H. Nguyen, V. N. Huynh, & M. Inuiguchi (Eds.), *Lecture notes in computer science: Vol. 11471. Integrated uncertainty in knowledge modelling and decision making* (pp. 222–234). Springer.

Chaiyakan, S., & Thipwiwatpotjana, P. (2021). Bounds on mean absolute deviation portfolios under interval-valued expected future asset returns. *Computational Management Science, 18*(2), 195–212.

Fiedler, M., Nedoma, J., Ramík, J., Rohn, J., & Zimmermann, K. (2006). *Linear optimization problems with inexact data*. Springer.

Hladík, M. (2009). Optimal value range in interval linear programming. *Fuzzy Optimization and Decision Making, 8*(3), 283–294.

Hladík, M. (2012). An interval linear programming contractor. In J. Ramík & D. Stavárek (Eds.), *Proceedings of 30th international conference mathematical methods in economics* (pp. 284–289). Silesian University in Opava.

Hladík, M. (2014). How to determine basis stability in interval linear programming. *Optimization Letters, 8*(1), 375–389.

Mathworks. (2026). *Set MATLAB runtime path for deployment*. Retrieved February 10, 2026, from
https://www.mathworks.com/products/compiler/matlab-runtime.html

Rohn, J. (1993). Stability of the optimal basis of a linear program under uncertainty. *Operations Research Letters, 13*(1), 9–12.