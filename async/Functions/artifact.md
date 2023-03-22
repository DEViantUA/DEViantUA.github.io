# Information:

A useful feature for bot developers. Get information about the characters from the showcase, for their further use.
!!! tip "Requires ENC"
    This function requires an [enc()](enc.md) argument that must be obtained from the enc function

## Profile:
It takes ```enc``` and ```image``` argument.


```enc``` - The result returned by the ```EnkaGenshinGeneration().enc()``` function
```teample``` - Select a profile template. Currently only template is available: 1
```artifactType``` - Select the artifact card you want to receive. (Available options: Flower,Feather,Sands,Goblet,Circlet, if you want to get all, leave the field empty)


### Example
``` python
from enkacard import encbanner
import asyncio

def encartifact():
    async with encbanner.ENC() as encard:
        ENCpy = await encard.enc(uids = 757562748)
        artifact = await encard.artifact(enc = ENCpy, 1, artifactType = "Flower,Feather,Sands,Goblet,Circlet")
    print(artifact)

asyncio.run(encprofile())        
```

### Result:
```python
{UID: {Name_Character: {Name_Artifact_Type: PILL.Image, Name_Artifact_Type: PILL.Image, ... }, Name_Character: {Name_Artifact_Type: PILL.Image, Name_Artifact_Type: PILL.Image, ... }, ....}}
```

- ```UID``` - User Game UID.
- ```Name_Character``` - Character name 
- ```Name_Artifact_Type``` - Artifact type name


