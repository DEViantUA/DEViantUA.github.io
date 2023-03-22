# Information:

Enc - An asynchronous function that returns the result of executing enkanetwork.py in the required format for further passing it as an argument to the functions of the EnkaNetworkCard class: ```start```, ```profile```


## Enc:
Takes an ```uids``` argument.

```uids``` - Can be a single number/string or a string containing multiple player uids separated by commas.

## Asynchronous/Threaded:
If you are using the asynchronous version, then it is enough to call it with await, if you are using the threaded version, then you need to call it via asyncio.run()

### Example:
```python
# Example one uids:
from enkacard import encbanner
import asyncio

async def aiocard():
    async with encbanner.ENC() as encard:
        ENCpy = await encard.enc(uids = 757562748)

    print(ENCpy)

asyncio.run(aiocard())

```
```python
#Example one or more uids:
from enkacard import encbanner
import asyncio

async def aiocard():
    async with encbanner.ENC() as encard:
        ENCpy = await encard.enc(uids = "757562748,757562749,...")
    print(ENCpy)

asyncio.run(aiocard())
```

### Result:
```python
{"757562748": {enkanetwork.py_object}, "757562749": enkanetwork.py_object, ...}
```

