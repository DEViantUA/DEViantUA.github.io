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
EnkaGenshinGeneration(img = "img.png") 
```

```python
#Example str image link:
EnkaGenshinGeneration(img = "https//...image.png") 
```

```python
#Example PIL.ImageFile:
EnkaGenshinGeneration(img = Image.open("img.png"))
```

```python
#Example list:
EnkaGenshinGeneration(img = [Image.open("img.png"), "img.png", "https//...image.png"]) 
```

## charterImg:
This argument can give each character card its own image.

Takes the value: ```dict``` (Can take all values from the img argument except list.)

### Example:
```python
EnkaGenshinGeneration(charterImg = {"Klee": Image.open("img.png"), "Albedo": "img.png", "Xiao": "https//...image.png"})
```

## randomImg:
Randomly select images from list of ```img``` argument.

### Example:
```python
EnkaGenshinGeneration(img = [Image.open("img.png"), "img.png"], randomImg = True) #If img is not a list, then randomImg is ignored.
```

## adapt:
Adapt the background to the custom image passed in the ```img``` argument.

### Example:
```python
EnkaGenshinGeneration(img = "img.png", adapt = True)
```

## splash:
If the character is wearing a costume, then their splashes will be available in costumes.

### Example:
```python
EnkaGenshinGeneration(splash= True)
```


## namecard:
Replaces the background of the player card image with character images. (Used only for the second template.)

### Example:
```python
EnkaGenshinGeneration(namecard = True)
```

## dowload:
Will return ready images for further work with them. (If not specified, then the finished results will be saved in the directory of the executable file in the folder ```EnkaImg``` and return None: )

### Example:
```python
EnkaGenshinGeneration(dowload = True)
```

## name:
Generates only cards of the specified characters.

### Example:
```python
#Example str one character:
EnkaGenshinGeneration(name = "Klee")
```
```python
#Example str two or more characters:
EnkaGenshinGeneration.start(uids = "757562748", name = "Klee, Albedo, ...")
```

## hide:
Should the player's UID be displayed?

### Example:
```python
EnkaGenshinGeneration(hide = False)
```

