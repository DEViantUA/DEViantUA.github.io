## API address:

```
https://web-production-32d8.up.railway.app/api/
```

Supports request methods: ```POST```


### Method:

* card - Obtaining player showcase character cards.
```
https://web-production-32d8.up.railway.app/api/card
```


* profile -To get a profile preview.
```
https://web-production-32d8.up.railway.app/api/profile
```


## Card:

The card method supports the following options:

* uid - The in-game UID of the Genshin player. (Required parameter)
* lang - The language in which the information will be displayed. (English by default)
* nameCards - Takes the value: ```False/True``` Use a name card or a character card. Only for the second template.
* characterName - List of characters in str format separated by commas.
* hide - Takes the value: ```False/True``` Display UID or not.
* splashArt - Takes the value: ```False/True``` Use splash art of character costumes.
* teample - Takes the value: ```1,2,3,5 or 7``` Template type

## Profile:

The profile method supports the following options:

* uid - The in-game UID of the Genshin player. (Required parameter)
* teample - Select a profile template. 1 or 2 (1 by default)
* lang - The language in which the information will be displayed. (English by default)


## Excample:

* Python: 

```python
import requests

url = "https://web-production-32d8.up.railway.app/api/card"

data = {"uid": 724281429}


resp = requests.post(url, data=data)

print(resp.json())
```

* JavaScript/Ajax: 

```JavaScript
var url = "https://web-production-32d8.up.railway.app/api/card";

var xhr = new XMLHttpRequest();
xhr.open("POST", url);

xhr.setRequestHeader("Content-Type", "application/json");

xhr.onreadystatechange = function () {
   if (xhr.readyState === 4) {
      console.log(xhr.status);
      console.log(xhr.responseText);
   }};

var data = {"uid": 757562748};

xhr.send(data);
```