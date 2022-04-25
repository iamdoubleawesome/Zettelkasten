#09Apr2022

# torch division

`torch.div(a, b)` : divides each element of tensor `a` by tensor/scaler `b` 

## 1D dividend 

```python
import torch
a = torch.tensor([2, 4, 6, 8])

print(torch.div(a, 2))
# tensor([1., 2., 3., 4.])

print(torch.div(a, torch.tensor([2])))
# tensor([1., 2., 3., 4.])

print(torch.div(a, torch.tensor([1, 2, 3, 4])))
# tensor([2., 2., 2., 2.])

print(torch.div(a, torch.tensor([[1, 2, 3, 4], [2, 2, 2, 2]])))
# tensor([[2., 2., 2., 2.],
#        [1., 2., 3., 4.]])
```



## 2D dividend

```python
import torch
a = torch.tensor([[2, 4], [6, 8]])

print(torch.div(a, 2))
# tensor([[1., 2.],
#        [3., 4.]])

print(torch.div(a, torch.tensor([2])))
# tensor([[1., 2.],
#        [3., 4.]])

print(torch.div(a, torch.tensor([[1, 2], [3, 4]])))
# tensor([[2., 2.],
#        [2., 2.]])
```



---

#python #torch #pytorch #div

---

Source:

- https://www.tutorialspoint.com/how-to-perform-element-wise-division-on-tensors-in-pytorch#:~:text=We%20can%20also%20divide%20a,tensor%20will%20a%202D%20tensor.

