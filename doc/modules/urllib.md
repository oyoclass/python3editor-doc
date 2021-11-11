## urllib — URL handling

This module has several sub-modules that working with URLs, you can check the sub-modules in [Python's standard documentation](https://docs.python.org/3.6/library/urllib.html).

We will show some examples for the mostly common used submodules `urllib.request` and `urllib.parse`.

### urllib.request

One of the common usage of this module is fetching data from the internet.

#### Example 1) Get a webpage's source code:

```python
from urllib.request import urlopen

source_code = urlopen("http://sabrinaw.oyosite.com").read().decode("utf-8")
print(source_code)
```

This will print the source code string from website "sabrinaw.oyosite.com"

> Notice: If you are using the code above to get the source code from other website, it is not uncommon that you get some "forbidden" error instead of the actual source code. The reason is that some websites have restrictions for fetching their code, for example, they check if you are an actual browser or spider robot, and will return empty string or some fobidden error if they think you are a robot.

#### Example 2) Get CSV data and parse it with the CSV lib

A comma-separated values (CSV) file is a delimited text file that uses a comma to separate values. Each line of the file is a data record. Each record consists of one or more fields, separated by commas. [Read more on wiki >>](https://en.wikipedia.org/wiki/Comma-separated_values).


Suppose we have a CSV file for Code Conquest Hackthon:

```csv
Name, Nickname, Age, Kingdom, Soldier Type, Rank
Reuben,The Hammer,59,Prubadour,Lancer,Sergeant
Everitt,The Whisper,27,Prubadour,Pikeman,Major
Reinhardt,The Mammoth,56,Prubadour,Healer,Private
Mel,The Hawk,53,Truisian,Pikeman,Sergeant
```

We can upload this file to our OYO website then read from the url. For example:

```
import urllib.request, csv

page = urllib.request.urlopen("http://sabrinaw.oyosite.com/testing/data3.html")
reader = csv.reader(
    page.read().decode('utf-8').splitlines(),
    skipinitialspace=True
)

for row in reader:
    # row now is a python list
    print(row)
```

#### Example 3) Calling API

Most APIs provide [JSON](https://en.wikipedia.org/wiki/JSON) format data. Here we will a IP-to-Location API to get the location info from a IP.

```python
from urllib.request import urlopen
import json

ip = input("Input the IP you want to query: ")
url = f"http://ip-api.com/json/{ip}"
location = json.loads(urlopen(url).read())
print("Approx. Location:", location["city"], location["region"])
```

Run it (suppose we want to query the IP 67.84.146.84):
```
Input the IP you want to query: 67.84.146.84
Approx. Location: Ronkonkoma NY
```

#### Use OYOclass Proxy

Some schools may have firewalls that block domains in their allowlist. For example, if your school blocked access to the "ip-api.com" domain, you won't get the returned data like above. In such case, you can use our proxy: just simply prepend `https://proxy.oyoclass.com/` to any URL that you want to fetch data from.

```
from urllib.request import urlopen
import json

ip = input("Input the IP you want to query: ")
url = f"https://proxy.oyoclass.com/http://ip-api.com/json/{ip}"
location = json.loads(urlopen(url).read())
print("Approx. Location:", location["city"], location["region"])
```

Another example, here is an API you can call to get the bitcoin price in USD: https://api.coingecko.com/api/v3/simple/price?ids=bitcoin&vs_currencies=usd, suppose your school blocked the "coingecho.com" domain, you can just prepend `https://proxy.oyoclass.com/` to it:

```
from urllib.request import urlopen
import json
url = "https://proxy.oyoclass.com/https://api.coingecko.com/api/v3/simple/price?ids=bitcoin&vs_currencies=usd"
data = json.loads(urlopen(url).read())
print(data)
```

Run it:
```
{'bitcoin': {'usd': 65274}}
```

### urllib.parse

This submodule can help parse a URL string and split it into different components. [Read more >>](https://docs.python.org/3.6/library/urllib.parse.html#module-urllib.parse).

#### Example

```python
from urllib.parse import urlparse

url = "https://oyoclass.com/settings/account?name=python#anchor"
parsed = urlparse(url)
print(parsed)
print(parsed.scheme)
print(parsed.netloc)
print(parsed.path)
print(parsed.query)
print(parsed.fragment)
```

Run it:
```
ParseResult(scheme='https', netloc='oyoclass.com', path='/settings/account', params='', query='name=python', fragment='anchor')
https
oyoclass.com
/settings/account
name=python
anchor
```