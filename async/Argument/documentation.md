# Information:

The EnkaGenshinGeneration class supports a number of arguments that customize the final version of the character card image.


## lang
Takes one value to define the language. Supported languages are listed below in the documentation. The default is Russian.

### Example:
```python

EnkaGenshinGeneration(lang = "en")

```

### Languages Supported:
| Languege    |  Code   | Languege    |  Code   |
|-------------|---------|-------------|---------|
|  English    |     en  |  русский    |     ru  |
|  Tiếng Việt |     vi  |  ไทย        |     th  |
|  português  |     pt  | 한국어      |     kr  |
|  日本語      |     jp  | 中文        |     zh  |
|  中文        |     zh  | Indonesian |     id  |
|  français   |     fr  | español    |     es  |
|  deutsch    |     de  | Taiwan     |    cht  |
|  Chinese    |    chs  |      |      |

## img
To transfer your image, which will be on the image card.

Supports the following types: 
- Image link or the path to the file.
- PIL.ImageFile: Image opened with Image.open()
- list: Image link, the path to the file or PIL.ImageFile  (list only works with the argument: ```randomImg```)


### Example:
```python
#Example str the path to the file:
ENC(img = "img.png") 
```

```python
#Example str image link:
ENC(img = "https//...image.png") 
```

```python
#Example PIL.ImageFile:
ENC(img = Image.open("img.png"))
```

```python
#Example list:
ENC(img = [Image.open("img.png"), "img.png", "https//...image.png"]) 
```

## characterImgs:
This argument can give each character card its own image.

Takes the value: ```dict``` (Can take all values from the img argument except list.)

### Example:
```python
ENC(characterImgs = {"Klee": Image.open("img.png"), "Albedo": "img.png", "Xiao": "https//...image.png"})
```

## randomImg:
Randomly select images from list of ```img``` argument.

### Example:
```python
ENC(img = [Image.open("img.png"), "img.png"], randomImg = True) #If img is not a list, then randomImg is ignored.
```

## adapt:
Adapt the background to the custom image passed in the ```img``` argument.

### Example:
```python
ENC(img = "img.png", adapt = True)
```

## splashArt:
If the character is wearing a costume, then their splashes will be available in costumes.

### Example:
```python
ENC(splashArt= True)
```


## nameCards:
Replaces the background of the player card image with character images. (Used only for the second template.)

### Example:
```python
ENC(nameCards = True)
```

## save:
If specified, it will save the finished results to the ```AioEnkaImg``` directory

### Example:
```python
ENC(save = True)
```

## characterName:
Generates only cards of the specified characters.

### Example:
```python
#Example str one character:
ENC(characterName = "Klee")
```
```python
#Example str two or more characters:
ENC.start(uids = "757562748", characterName = "Klee, Albedo, ...")
```

## hide:
Should the player's UID be displayed?

### Example:
```python
ENC(hide = False)
```

## miniInfo:
Generate 4 template with minimum information or complete?

### Example:

```python
ENC(miniInfo = False)
```

## agent:
Submit your user agent to EnkaNetwork

### Example:

```python
ENC(agent = "YOU_USER_AGENT")
```