### Links

-   [YAML 1.2 Spec](http://www.yaml.org/spec/1.2/spec.html)
-   [Online YAML Linter (Ruby)](http://www.yamllint.com/)
-   [Online YAML Parser
    (Python)](http://yaml-online-parser.appspot.com/)
-   [kwalify - YAML schema validator
    (Ruby)](http://www.kuwata-lab.com/kwalify/)

### Syntax Snippets

# Scalars
## scalar = value

a: 1

a: 1.234

b: 'abc' 

b: "abc"

b: abc 

c: false    # boolean type

d: 2015-04-05   # date type

### Enforcing strings
b: !str 2015-04-05

# Sequences

### sequence
array:  
- 132
- 2.434
- 'abc'

### sequence of sequences

my_array:
- [1, 2, 3]
- [4, 5, 6] 

# Hashes

### Nested hash

my_hash:
subkey:
subsubkey1: 5
subsubkey2: 6
another:

### Hash of hashes
my_hash: {nr1: 5, nr2: 6}
