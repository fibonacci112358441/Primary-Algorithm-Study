###递归方程求解代价
----
$A(n)=\left(n-1\right)+\frac{1}{n}\displaystyle\sum_{i=0}^{n-1}[A(i)+A(n-i-1)].$
$对称性可得A(n)=\left(n-1\right)+\frac{2}{n}\displaystyle\sum_{i=1}^{n-1}A[i].$
$因为\displaystyle\sum_{i=0}^{n-1}[A(i)+A(n-i-1)]=[A(0)+A(n-1)]+[A(1)+A(n-2)]+……+[A(n-1)+A(0)]形式对称，所以可得上式.$
$利用guess\quad and\quad prove思想，$
$猜测并假设每次递归后的划分是均匀的,$
$可知A(n)=(n-1)+2A(n/2),然后利用Master定理,$
$可得A(n)=\theta(nlogn).$
$然后在递归式中进行归纳假设，证明存在$$c_1和$$c_2$$满足：$$c_2ilni\le$$A(i)$$\le$$c_1ilni$
$即证明A(n)\in$$O(nlogn)$$又\in\Omega(nlogn).$
$利用放缩，\displaystyle\sum_{i=1}^{n-1}ilni\le\displaystyle\int_1^{n-1}xlnx{\rm d}x$$且\displaystyle\sum_{i=2}^{n}ilni\geq\displaystyle\int_1^{n}xlnxdx，将\displaystyle\sum_{i=1}^{n-1}ilni写为\displaystyle\sum_{i=2}^{n}ilni-nlnn.$
$列递归方程，解递归，结合递归树：$
![](images/2022-10-01-20-28-52.png)

