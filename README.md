# KeyStore
A thread friendly database written in python


## Example

### Creating Keystore
```
x = KeyStore(hello="world")
print(x)
```
### Accessing an attribute
```
x = KeyStore(hello="world")
print(x.hello)
```
### Accesing dict
```
x['hello'] = 'bye'
print(x)
```
### Setting Attribute
```
x.hello = "Goodbye"
x.set('hello', x.hello)
print(x)
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
### Loading JSON as Dict
```
_dict = x.dict(_json)
print(_dict['hello'])
```
