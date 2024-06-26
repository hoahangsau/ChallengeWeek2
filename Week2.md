# Quadratic Residues
## Description
- Find the quadratic residue and then calculate its square root. Of the two possible roots, submit the smaller one as the flag.

## Problem solve
<pre>
p = 29
ints = [14, 6, 11]
for a in range(28):
    if any(pow(a, 2, p) == x for x in ints):
        print(a)
</pre>
Chúng ta gọi x là Quadratic Residue nếu tồn tại một số a sao a^2 ≡ x mod p -> cho a^2 %p sẽ ra được số đồng dư còn lại.
![image](https://hackmd.io/_uploads/HJhaxceTp.png)


# Legendre Symbol
## Description
- Given the following 1024 bit prime and 10 integers, find the quadratic residue and then calculate its square root; the square root is your flag. Of the two possible roots, submit the larger one as your answer.
## Problem solve
<pre>
p = ...
int = [...]
for a in ints:
    legendre = pow(a,(p-1)//2,p)
    if (legendre == 1):
        print(pow(a,(p+1)//4,p))
</pre>

Legendre Symbol được sử dụng để tìm Quadratic Residues module p . Sau đó ta tìm square root bằng công thức Tonelli-Shanks
<pre>
  pow(a,(p+1)//4,p)
</pre>
 
