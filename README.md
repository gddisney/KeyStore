# KeyStore
A thread friendly database written in python


## Example

### Creating Keystore
```
from Keystore import *
x = KeyStore(hello="world")
print(x)
```
#### Output
```
{'hello': 'world'}
```
### Accessing an attribute
```
from Keystore import *
x = KeyStore(hello="world")
print(x.hello)
```
#### Output
```
world
```
### Accesing dict
```
x['hello'] = 'bye'
print(x)
```
#### Output
```
{'hello': 'bye'}
```
### Setting Attribute
```
x.hello = "Goodbye"
x.set('hello', x.hello)
print(x)
```
#### Output
```
{'hello': 'Goodbye'}
```
### Writing to DB
```
x.write("id-test","id.db")
```
### Gettomg Database len
```
_len = x.len('id.db')
x.write(f"id-test-{_len}","id.db")
y = x.get(f"id-test-{_len}","id.db")
```
### Exporting JSON
```
_json = x.json()
print(_json)
```
#### Output
```
{"hello": "Goodbye"}
```
### Loading JSON as Dict
```
_dict = x.dict(_json)
print(_dict['hello'])
```
#### Output
Goodbye
