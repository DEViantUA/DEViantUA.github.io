# Information:
Example of running Threads:

``` python
from enkanetworkcard import encbanner
import asyncio

ENC = encbanner.EnkaGenshinGeneration() 
encR = asyncio.run(ENC.enc(uids = "811455610"))
result = ENC.start(enc = encR)
print(result)
```