numpy array の初期化

```
# 0で初期化
mask=np.zeros((image.shape[0],image.shape[1]))
# 1で初期化
mask=np.ones((image.shape[0],image.shape[1]))
# 特定の値で初期化
mask=np.full((image.shape[1],image.shape[2]),255)
```