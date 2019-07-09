# Neural network

## peceptron training 

- before exam
- wirte down the whole prcepton training 

和liner regression类似

```
a(m,n)
b(m,n)
a*b > 0
m1*m2 + n1*n2 > 0 
it denpends on the angle between a b 

```
```
dot的分类取决于其与法向量的夹角
> 90 -1
<= 90 1
```

# perceptron algorithem

1. inital the weight w = (w0,w1,w2,.....,wn)

2. cycle through all the dateset 
   - (a) if sum(w_i * x) > 0  x -> p do nothing classify correct
   - (b) if sum(w_i * x) < 0  x -> n do nothing classify correct
   - (c) if sum(w_i * x) > 0  x -> n make angle bigger  which means that w = w - x_i
   - (d) if sum(w_i * x) > 0  x -> n make angle smaller  which means that w = w + x_i

