# Calculating the gradient 

Numerical differentiation
dE/dw = (E(w + hei) - E(w)) / h

f'(x) = lim{h->0} ( f(x+h) - f(x) ) / h

programming languages don't usually have a lim construct so let h be a small number

f'(x) = ( f(x+h) - f(x) ) / h

where h = 1/10^9

Efficiency - gradient has m components, so you would have to calculate the above m times. 

Time complexity - O(cal. E).O(cal. m) - It is not efficient

Working with floating point numbers:

1. do not add very small and large numbers.
2. do not subtract numbers of similar sizes.

The above method violates both these rules.

## Back Propagation
Space: Takes up a lot of space.

Operation Count: For each primitive function the derivative must be calculated. At worst this will be a small constant vector more work.

Exact: It is exact up to floating point issues.

See Images/lecture-04 for descriptions of back propagation with unary and binary functions and functions which have one input and two outputs.

## Disjoint Networks
Have a series of networks computing the same problem. If they are all making the same predictions, the probability they are getting the correct result is higher than if they are making difference predictions.
