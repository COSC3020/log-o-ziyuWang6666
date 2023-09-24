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

I am a little bit do not know how to write in big O format. The following are just mathematical calculations with what I thought big O.

$T(\log_{5}n)  \leq O(log_{2}n)$

$T(\log_{5}n)  \leq c * O(log_{2}n)$ 

$if\ c = log_{5}2\$

$T(\log_{5}n) \leq O(log_{5}2$ * $\log_{2}n)$ 

$\log_{5}2$ * $\log_{2}n$ = $\frac{lg_{2}}{lg_{5}} * \frac{lg_{n}}{lg_{2}}$, then we could cancel $\lg_{2}$, left $\frac{lg_{n}}{lg_{5}}$

$\frac{lg_{n}}{lg_{5}}$ = $\log_{5}n$

So, $T(\log_{5}n)  \leq  O(log_{5}n)$ , $O(\log_{5}n) = O(log_{5}n)$, $O(\log_{2} n)$ is the same as $O(\log_{5} n)$.
