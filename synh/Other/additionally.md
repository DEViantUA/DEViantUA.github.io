## Fix bug with async:

Windows users may experience an error: ```RuntimeError: Event loop is closed``` if this occurs, then you must set the variable ```FIX_ASYNCIO_WIN = True```

### Example
```python 
from enkanetworkcard import encbanner

ENC = encbanner.EnkaGenshinGeneration() 
ENC.FIX_ASYNCIO_WIN = True
```

## Updating enkanetwork.py data:
```python 
from enkanetworkcard import upload
upload() 
```


## Template example:

### The result of a custom images and adaptation (template= 1).
<img src="https://raw.githubusercontent.com/DEViantUA/EnkaNetworkCard/main/img/Example1.png" width='300' alt="Example1"/> <img src="https://raw.githubusercontent.com/DEViantUA/EnkaNetworkCard/main/img/Example2.png" width='300' alt="Example2"/> 

### Usual result (template= 1).
<img src="https://raw.githubusercontent.com/DEViantUA/EnkaNetworkCard/main/img/Example3.png" width='300' alt="Example3"/> <img src="https://raw.githubusercontent.com/DEViantUA/EnkaNetworkCard/main/img/Example4.png" width='300' alt="Example4"/> 

### The result of a custom images and adaptation (template= 2).
<img src="https://raw.githubusercontent.com/DEViantUA/EnkaNetworkCard/main/img/Example5.png.png" width='300' alt="namecard = True"/> <img src="https://raw.githubusercontent.com/DEViantUA/EnkaNetworkCard/main/img/Example6.png.png" width='300' alt="namecard = False"/> 

### Usual result (template= 2).
<img src="https://raw.githubusercontent.com/DEViantUA/EnkaNetworkCard/main/img/Example8.png.png" width='300' alt="namecard = True"/> <img src="https://raw.githubusercontent.com/DEViantUA/EnkaNetworkCard/main/img/Example7.png.png" width='300' alt="namecard = False"/> 

### Usual result (template= 3).
<img src="https://raw.githubusercontent.com/DEViantUA/EnkaNetworkCard/main/img/Венти_11_12_2022 17_15.png" width='300' alt="namecard = True"/> <img src="https://raw.githubusercontent.com/DEViantUA/EnkaNetworkCard/main/img/Чжун%20Ли_11_12_2022%2017_15.png" width='300' alt="namecard = False"/> 