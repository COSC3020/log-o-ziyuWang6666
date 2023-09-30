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

$O(log_{2}n) = O(log_{5}n)$

===============================The first part===============================================

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

$T(n) \in O(log_{2}n) \iff \exists c, n_0: T(n) \leq c \cdot (log_{2}n) \forall n \geq n_0$

According to log base change rule: $\log_{b}a = \frac{log_{n}a}{log_{n}b}$, any base n. If n=5, $\log_{b}a = \frac{log_{5}a}{log_{5}b} = \frac{1}{log_{5}b} * \log_{5}a$

$T(n) \in O(log_{2}n) \iff \exists c, n_0: T(n) \leq c \cdot (\frac{1}{log_{5}2} * log_{5}n) \forall n \geq n_0$

$c*\ (\frac{1}{log_{5}2})$, c is constant, c times a constant is still a constant. We set constant d = $c*\ (\frac{1}{log_{5}2})$

$T(n) \in O(log_{2}n) \iff \exists c, n_0: T(n) \leq （d * log_{5}n) \forall n \geq n_0$

$T(n) \in O(log_{2}n) \iff \exists c, n_0: T(n) \in O(log_{5}n) \forall n \geq n_0$

$\forall T(n) \in O(log_{2}n) \implies T(n) \in O(log_{5}n) $


===============================The second part===============================================



$T(n) \in O(log_{5}n) \iff \exists c, n_0: T(n) \leq c \cdot (log_{5}n) \forall n \geq n_0$

According to log base change rule: $\log_{b}a = \frac{log_{n}a}{log_{n}b}$, any base n. If n=2, $\log_{b}a = \frac{log_{2}a}{log_{2}b} = \frac{1}{log_{2}b} * \log_{2}a$

$T(n) \in O(log_{5}n) \iff \exists c, n_0: T(n) \leq c \cdot (\frac{1}{log_{2}5} * log_{2}n) \forall n \geq n_0$

$c*\ (\frac{1}{log_{2}5})$, c is constant, c times a constant is still a constant. We set constant d = $c*\ (\frac{1}{log_{2}5})$

$T(n) \in O(log_{5}n) \iff \exists c, n_0: T(n) \leq （d * log_{2}n) \forall n \geq n_0$

$T(n) \in O(log_{5}n) \iff \exists c, n_0: T(n) \in O(log_{2}n) \forall n \geq n_0$

$\forall T(n) \in O(log_{5}n) \implies T(n) \in O(log_{2}n) $


=================================Conclusion==========================================================

So, by bidirectional proof T(n) and f(n), $O(\log_{2} n)$ is the same as $O(\log_{5} n)$.


//get help from the professor, TA, and help from Dhruv to write special big O formats
