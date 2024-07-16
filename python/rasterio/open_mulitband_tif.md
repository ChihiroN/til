rasterioでマルチバンドtif画像を開く

install
```
pip install rasterio
```

code
```
import numpy as np
import rasterio

with rasterio.open(image_path) as image:
    image = image.read()
    print(image.shape[0])
    print(image.dtype)
    image=np.array(image)
    print(image.shape)
#output
# 6
# uint8
# (6, 256, 256) # C,W,H
```