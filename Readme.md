

[Matlab Tutorial](https://www.tutorialspoint.com/matlab/index.htm)

[Matlab Command](https://www.tutorialspoint.com/matlab/matlab_commands.htm)


| Function  | Description | Function  | Description |
|---|-----|---|-----|
| exp(x) | ![](https://latex.codecogs.com/gif.latex?e^x) | factorial(x) | x! |
| sqrt(x) | ![](https://latex.codecogs.com/gif.latex?\sqrt{x}) | nthroot(x,n) | ![](https://latex.codecogs.com/gif.latex?\sqrt[n]{x}) |
| log(x) | ![](https://latex.codecogs.com/gif.latex?lnx) | log10(x) | ![](https://latex.codecogs.com/gif.latex?log_{10}{x}) |
| sin(x) | sin(pi/2) | sind(x) | sind(90) |
| rem(x,y) | remainder | | | 

<hr>

## Matrix Creation

 
variable = [i:k:j]  = [i, i+k, ... ,j]


variable = linespace(i,j,n) = [i, ... ,j] , length = n



transpose operation : variable' 


```
arr = [1:2:12;linspace(2,12,6)]

arr = 
     1     3     5     7     9    11
     2     4     6     8    10    12 

arr(1:2,2:3) = 
     3     5
     4     6
     
arr([1,2],[1,5]) = 
     1     9
     2    10   
     
arr(3,1) = 22
     1     3     5     7     9    11
     2     4     6     8    10    12
    22     0     0     0     0     0
    
>> arr(3,:) = []
     1     3     5     7     9    11
     2     4     6     8    10    12
    
```

<hr>

## Matrix Operation

* Invert 
 
```
>> A = [1 2; 3 4];
>> B = inv(A);
>> A*B

ans =

    1.0000         0
    0.0000    1.0000
```

* Left division
AX = B
X = inv(A)*B = A \ B

* Right division
XC = B
X = B*inv(C) = B / C

```
>> A = [1 2; 3 4];
>> B = [5;11];
>> A\B

ans =

     1
     2
```

* Element-by-element operation

```
>> A = [1 2; 3 4];
>> B = [2 3; 4 2];
>> A.*B

ans =

     2     6
    12     8
```     
    
```
>> A = [1 2; 3 4];
>> B = [2 3; 4 2];
>> A./B

ans =

    0.5000    0.6667
    0.7500    2.0000

>> A.\B

ans =

    2.0000    1.5000
    1.3333    0.5000
``` 

## Polynominal
* polyval()

![](https://latex.codecogs.com/gif.latex?x^2+2x+3) 
``` 
>> p = [1 2 3];
>> polyval(p,2)
  11
``` 


## Symbolic Math
* syms
``` 
>> syms f g h x
>> f = x/4
>> g = x/3
>> h = f+g
   h = (7*x)/12   
```
   
* collect / factor / expand
```
>> expand(sin(x-y))
   cos(y)*sin(x) - cos(x)*sin(y)
```

* simplify / simple
```
>> simplify((x^2+2*x*y+y^2)/(x+y)) 
   x + y
```

* solve
```
>> syms S;
>> S = x^2+2*x+1;
>> solve(S)
  -1
  -1
```
