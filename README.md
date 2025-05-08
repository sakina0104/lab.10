import math

def f(x):
    return x + math.log(x) - 0.5

def df(x):
    return 1 + 1/x

x0 = 0.5
eps = 1e-6
max_iter = 100

for i in range(max_iter):
    x1 = x0 - f(x0) / df(x0)
    if abs(x1 - x0) < eps:
        break
    x0 = x1

print("Təqribi kök:", x1)
