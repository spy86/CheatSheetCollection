### Data Types

Dumping complex structures
```python
    import json
    print json.dumps(something)
```
#### Arrays (Lists)

Print array of strings:
```python
    print "\n".join(arr)
```
Iterating by index
```python
    for i in range(len(arr)):
      print arr[i]
```
### Standard Tasks

#### Read from Pipe

Line by line
```python
    proc = subprocess.Popen(['/bin/ls', 'something'],stdout=subprocess.PIPE)
    while True:
      line = proc.stdout.readline()
      if line != '':
        do_something
      else:
        break
```
Entire output at once
```python
    echo subprocess.check_output(['/bin/ls', 'something])
```
#### Parse JSON
```python
    import json
    data = json.loads(json_string)
```
