def f(n):
    if n <= 2:
        return 1 
    else:
        return f(n-1) + f(n-2)

print f(11) % 20132013



a = 1
b = 1
for i in range(1, 11):
    c = (a + b) % 20132013
    a = b
    b = c
print a
