[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11924427&assignment_repo_type=AssignmentRepo)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

## Answer

$T(\log_{5}n)  \leq c * O(log_{2}n)$ or $T(\log_{2}n)  \leq c * O(log_{5}n)$

By the formal definition of big O: c = $\log_{b}a$ and f(n)= $\log_{a}n$, c = $\log_{a}b$ and f(n) = $\log_{b}n$

To get T(n):

T(n) = c * f(n) = $\log_{b}a$ * $\log_{a}n$ = $\frac{lg_{a}}{lg_{b}} * \frac{lg_{n}}{lg_{a}}$, then we could cancel $\lg_{a}$, left $\frac{lg_{n}}{lg_{b}}$, then $\frac{lg_{n}}{lg_{b}}$ = $\log_{b}n$

T(n) = c * f(n) = $\log_{a}b$ * $\log_{b}n$ = $\frac{lg_{b}}{lg_{a}} * \frac{lg_{n}}{lg_{b}}$, then we could cancel $\lg_{b}$, left $\frac{lg_{n}}{lg_{a}}$, then $\frac{lg_{n}}{lg_{a}}$ = $\log_{a}n$


By the formal definition of big O: c = $\log_{a}b$ and T(n)= $\log_{a}n$, c = $\log_{b}a$ and T(n) = $\log_{b}n$

To get f(n):

f(n) = $\frac{1}{c}$ * T(n) = $\frac{1}{\log_{a}b}$ * $\log_{a}n$ = $\frac{lg_{a}}{lg_{b}} * \frac{lg_{n}}{lg_{a}}$, then we could cancel $\lg_{a}$, left $\frac{lg_{n}}{lg_{b}}$ = $\log_{b}n$

f(n) = $\frac{1}{c}$ * T(n) = $\frac{1}{\log_{b}a}$ * $\log_{b}n$ = $\frac{lg_{b}}{lg_{a}} * \frac{lg_{n}}{lg_{b}}$, then we could cancel $\lg_{b}$, left $\frac{lg_{n}}{lg_{b}}$ = $\log_{a}n$

So, by bidirectional proof T(n) and f(n), $O(\log_{2} n)$ is the same as $O(\log_{5} n)$.


//get help from Dhruv to write special big O format, and help from TA
