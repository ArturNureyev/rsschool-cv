# CV
![My photo](https://i.ibb.co/hy5MxGx/my-photo.png)
## **Artur Nureyev**


#### **About me:**
Most of my life i working as bartender/bar manager. For this moment trying to study something new for me.


#### **Knowledges:**
Just started studing course of [JavaScript/Front-end Preschool by RS School](https://rs.school/js-stage0/)

Was trying to work with parsing by using Python


#### **Examples of my code:**
JavaScript:
```js
function isPrime(num) {
if(num <= 1) return false;
if(num === 2 || num === 3) return true;
else {
  for(i = 2; i <= Math.sqrt(num); i++) {
    if(num % i === 0) return false;
  }
}
  return true;
}
```
Python:
```python
import requests
from selectolax.parser import HTMLParser


def get_ticker_pivot(ticker_symbol):
    url = f'https://www.earningswhispers.com/stocks/{ticker_symbol}'
    headers = {
        "accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9",
        "user-agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/99.0.4844.51 Safari/537.36"
    }
    src = requests.get(url, headers=headers)
    if HTMLParser(src.text).css_first('div#pivots') is None:
        error_message = {'error': 'NO TICKER FOUND'}
        return error_message
    else:
        resistance = []
        for item in ['r1', 'r2', 'r3']:
            resistance.append(HTMLParser(src.text).css_first(f'div#{item}').text())
        support = []
        for item in ['s1', 's2', 's3']:
            support.append(HTMLParser(src.text).css_first(f'div#{item}').text())
        pivots = {'resistance': resistance, 'support': support}
    return pivots
```

#### **Education:**
Diploma of Kazan State University of Culture and Arts - Theater Directing


Contacts:
- tel: +79172999718
- email: arturnurey@gmail.com
- telegram: [ArturNurey](https://t.me/arturnurey)