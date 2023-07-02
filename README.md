# Calculating the Square root of two.
This takes an iterative approach to finding the square root of two. Each step nearly doubles the amount of digits. It is based on the simple statement  
$$\sqrt 2 = {a \over b}+x$$  
where $a\over b$ is a a rational approximation for $\sqrt2$ and we are attempting to calculate $x$.

We want x to be the reciprocal of a natural number, so that we will build a sequence of rational approximations that get closer and closer to $\sqrt2$.  
$$\sqrt 2 \approx {a \over b}+{1\over n}$$  
Squaring gives  
$$2 \approx ({a \over b}+{1\over n})^2$$  
$$2 \approx {a^2 \over b^2}+{2a \over bn}+{1\over n^2}$$  
Rearranging for $1\over n$ gives  
$${1\over n} \approx {b\over 2a}(2-{a^2 \over b^2}-{1\over n^2}) $$  
$${1\over n} \approx {b\over 2a}({2b^2\over b^2}-{a^2 \over b^2})-{b\over 2an^2} $$  
$${1\over n} \approx {2b^2-a^2\over 2ab}-{b\over 2an^2} $$  
Now since ${a\over b}\approx\sqrt2$ we have  
$$a^2 \approx 2b^2$$  
$$2b^2-a^2 \approx 0$$  
Now since it cannot be zero it must be $\pm1$, hence  
$$2b^2-a^2=\pm1$$  
Substituting back we have  
$${1\over n} \approx {1\over 2ab}-{b\over 2an^2} $$
As n gets larger we can ignore the $n^2$ term,  
$${1\over n} = {1\over 2ab}$$
or
$$ n = 2ab$$
which gives us our iterative sequence.  
Starting with $a=1$ and $b=1$ we have $n=2.1.1=2$ and the approximation
$$\sqrt2 \approx {1\over1}+{1\over2}={3\over2}$$
The second iteration using $a=3$ and $b=2$ gives us
$$\sqrt2 \approx {1\over1}+{1\over2}={3\over2}-{1\over 2.3.2}={3\over2}-{1\over12}={17\over12}$$
The third iteration using $a=17$ and $b=12$ gives us
$$\sqrt2 \approx {17\over12}-{1\over2.17.12}={17\over12}-{1\over408}={577\over408}$$
The fourth iteration using $a=577$ and $b=408$ gives us
$$\sqrt2 \approx {577\over408}-{1\over2.577.408}={577\over408}-{1\over470832}={665857\over470832}={2.577^2-1\over2^4.3.17.577}$$
This number agrees with $\sqrt2$ to 11 decimal places.  The next iteration will provide over 22 digits accuracy.
Overall the sequence is
$$\sqrt2 \approx {1\over1}+{1\over2}-{1\over12}-{1\over408}-{1\over470832}- \cdots$$
The integer sequence of the denominators $1,2,12,408,470832,\cdots$ is well known and found at [A051009](https://oeis.org/A051009) on [The On-line Encyclopedia of Integer Sequences](https://oeis.org/).







