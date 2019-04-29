### Data Types

Dumping complex structures

    import json
    print json.dumps(something)

#### Arrays (Lists)

Print array of strings:

    print "\n".join(arr)

Iterating by index

    for i in range(len(arr)):
      print arr[i]

### Standard Tasks

#### Read from Pipe

Line by line

    proc = subprocess.Popen(['/bin/ls', 'something'],stdout=subprocess.PIPE)
    while True:
      line = proc.stdout.readline()
      if line != '':
        do_something
      else:
        break

Entire output at once

    echo subprocess.check_output(['/bin/ls', 'something])

#### Parse JSON

    import json
    data = json.loads(json_string)
