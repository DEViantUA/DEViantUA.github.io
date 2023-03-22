# Information:

The main function to start generating character card images.

!!! tip "Requires ENC"
    This function requires an [enc()](enc.md#template-example) argument that must be obtained from the enc function

## Start:
It takes ```enc``` and ```template``` argument.

```enc``` - The result returned by the ```EnkaGenshinGeneration().enc()``` function
```template``` - Choosing a template to create a character card. There are 3 in total.
(Template examples can be found here: [template](/Other/additionally.md))


### Thread example:
``` python
from enkanetworkcard import encbanner
import asyncio

ENC = encbanner.EnkaGenshinGeneration()
encR = asyncio.run(ENC.enc(uids = "811455610"))
resultProfile = ENC.start(enc = encR, teample = 3)
print(resultProfile)
```

### Result:
### If you specified download = True:
```python
    >> {"uid": {"name_charter1": "PillImage.Image","name_charter2": "PillImage.Image", ...}, ...}
```
### If you specified download = False:
```python
    >> None
```
!!! example "Result download = False"
    In the directory of the executable file, a special folder EnkaImage / AioEnkaImage will be created where the finished images will be saved.



[def]: ../about/license.md