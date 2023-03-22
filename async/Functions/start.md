# Information:

The main function to start generating character card images.

!!! tip "Requires ENC"
    This function requires an [enc()](enc.md#template-example) argument that must be obtained from the enc function

## Start:
It takes ```enc``` and ```template``` argument.

```enc``` - The result returned by the ```EnkaGenshinGeneration().enc()``` function
```template``` - Choosing a template to create a character card. There are 3 in total.
(Template examples can be found here: [template](/Other/additionally.md))
```background``` - Replaces the background on template 4, can be a link, local file or PILL.Image
```cards``` - The result that creat(template = 4 and 6) returns | Speeds up regeneration.

### Async example:
``` python
from enkacard import encbanner
import asyncio
def card():
    async with encbanner.ENC() as encard:
        ENCpy = await encard.enc(uids = "811455610")
        return await encard.creat(ENCpy,3)
print(asyncio.run(card()))
```

### Result teamplate 1,2,3,5,7:
```python
    >> {"uid": {:"name_charter1": {"img":"PillImage.Image", "id": charter_id},"name_charter2": {"img":"PillImage.Image", "id": charter_id},, ...}
```

### Result teamplate 4,6:
```python
    >> {'uid': 'uid', 'card': 
        {'1-4': {'img': "PillImage.Image", 'cards': {'name_charter1': {'img': "PillImage.Image", 'id': 10000049}, 'name_charter2': {'img': "PillImage.Image",, 'id': 10000063}...}}},
        {'5-8': {'img': "PillImage.Image", 'cards': {'name_charter3': {'img': "PillImage.Image", 'id': charter_id}, 'name_charter4': {'img': "PillImage.Image",, 'id': charter_id}...}}}
    }
```

!!! example "Result save = True"
    In the directory of the executable file, a special folder AioEnkaImage will be created where the finished images will be saved.



[def]: ../about/license.md