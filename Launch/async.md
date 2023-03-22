
# Information:
Example of running profile and card:


## Launch:
``` python
from enkacard import encbanner
import asyncio

async def card():
    async with encbanner.ENC() as encard:
        ENCpy = await encard.enc(uids = "811455610")
        return await encard.creat(ENCpy,1)

result = asyncio.run(card()) 

print(result)
```

<details>
<summary>Launch Profile</summary>

``` python
from enkacard import encbanner
import asyncio

async def card():
    async with encbanner.ENC() as encard:
        ENCpy = await encard.enc(uids = "811455610")
        return await encard.profile(ENCpy,1)

result = asyncio.run(card()) 

print(result)
```
</details>