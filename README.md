[![Build Status](https://travis-ci.com/jverzani/ImplicitEquations.jl.svg?branch=master)](https://travis-ci.com/jverzani/ImplicitEquations.jl)


# ImplicitEquations


In a paper, [Tupper](https://doi.org/10.1145/383259.383267)
presents a method for graphing two-dimensional implicit equations and
inequalities. This package gives an
implementation of the paper's basic algorithms to allow
the `Julia` user to naturally represent and easily render graphs of
implicit functions and equations.


We give one example, others may be viewed as an `IJulia` notebook ([here](http://nbviewer.ipython.org/github/jverzani/ImplicitEquations.jl/blob/master/docs/examples.ipynb)).

The
[Devils curve](http://www-groups.dcs.st-and.ac.uk/~history/Curves/Devils.html)
is graphed over the default region as follows:

```
using Plots
pyplot()
using ImplicitEquations

a,b = -1,2
f(x,y) = y^4 - x^4 + a*y^2 + b*x^2
plot(f ⩵ 0)  # \Equal[tab]
```

![DevilsCurve](http://i.imgur.com/LChTzC1.png)
