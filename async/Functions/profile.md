# Information:

A useful feature for bot developers. Get information about the characters from the showcase, for their further use.
!!! tip "Requires ENC"
    This function requires an [enc()](enc.md) argument that must be obtained from the enc function

## Profile:
It takes ```enc``` and ```image``` argument.


```enc``` - The result returned by the ```EnkaGenshinGeneration().enc()``` function
```teample``` - Select a profile template. 1 or 2
```image``` - Generate a profile picture or not.

### Example
``` python
from enkacard import encbanner
import asyncio

def encprofile():
    async with encbanner.ENC() as encard:
        ENCpy = await encard.enc(uids = 757562748)
        profile = await encard.profile(enc = ENCpy)
    print(profile)

asyncio.run(encprofile())        
```

### Result:
```python
{"characters": {"name_charter": {...}, "charactersArg": {"name1", "name2", ..}}, "img": "..."}
```

- ```characters``` - Information about each character.
- ```charactersArg``` - List of character names to quickly pass to ```start()```
- ```img``` - Showcase generated image.


