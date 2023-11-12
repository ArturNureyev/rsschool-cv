# CV

### **Artur Nureyev**

![my photo](my_photo.png)

#### About me
I'm 38 and decided to study something new for me. Already spent 15 years in hospitality working as a bartender. When you work in a bar you need to work in a team, stay focused and study new everyday. I think that wil be handfull in programming.

#### My projects:
https://ArturNureyev.github.io/rsschool-cv/cv

#### Job experience:
Was making some parsing for my friends on *Python*:
```python
from bs4 import BeautifulSoup
import requests
import datetime


def earnings_next_two_weeks():
    earnings = {}
    url = "https://www.earningswhispers.com/calendar?sb=s&d=0&t=all"

    headers = {
        "accept": "image/avif,image/webp,image/apng,image/svg+xml,image/*,*/*;q=0.8",
        "user-agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/98.0.4758.82 Safari/537.36"
    }

    earnings_date = datetime.date.today()
    for i in range(14):
        if earnings_date.weekday() == 5 or earnings_date.weekday() == 6:
            url = url.replace(str(i), str(i + 1))
            earnings_date = earnings_date + datetime.timedelta(days=1)
            continue
        dict_date = earnings_date.strftime("%m/%d/%Y")
        earnings[dict_date] = ""
        src = requests.get(url, headers=headers).text
        soup = BeautifulSoup(src, "lxml")
        tickers = soup.find_all(class_="ticker")
        for item in tickers:
            earnings[dict_date] = f"{earnings[dict_date]}{item.text} "
        url = url.replace(str(i), str(i + 1))
        earnings_date = earnings_date + datetime.timedelta(days=1)
    return earnings


earnings_next_two_weeks()
```

#### My code from [Codewars](https://www.codewars.com/users/ArturNureyev) on *Javascript*:
```javascript
function alphabetPosition(text) {
  let textWithNum = [];
  for(i = 0; i < text.length; i += 1){
    if(text.toUpperCase().charCodeAt(i) < 91 && text.toUpperCase().charCodeAt(i) > 64){
      textWithNum.push(text.toUpperCase().charCodeAt(i) - 64);
      }
  }
  return textWithNum.join(' ');
}
```

* Languages:
    * Russian
    * English
    * Turkish

* Contacts:
    * +79172999718
    * arturnurey@gmail.com
    * N4#7359 (@ArturNureyev) (Discord)