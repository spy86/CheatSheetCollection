## Syntax
```python

    e = {}                                          # empty dict
    d = { 'key1': 'value1', 'key2': 'value2' }      # flat "hash"
    n = { 'toplevelkey': { 'subkey1': 'value3' } }  # nested "hash"
```
For debugging just print() to dump print out the dict content. Note that
for nicely formatted output you need to use something like pprint.
```python
    print(d)
    print(len(d))                  # return length
 ```   
Access dictionaries using []
```python
    d['key1']                      # gives 'value1'
    n['toplevelkey']['subkey1']    # gives 'value3'
```
Adding and removing stuff
```python
    d['key3'] = 'abc'                 # adds new key
    del n['toplevelkey']['subkey1']   # delete a sub key
```
Testing for keys
```python
    if 'key1' in d:
         print("Key exists.")
 ```   
## Iterating

To iterate on keys:
```python
    for k in d:
         print("key=", k)
```
To iterate on tuples:
```python
    for k,v in d.items():
        print("key=%s value=%s" % (k,v)) 
```
