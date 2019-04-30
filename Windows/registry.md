## reg Usage
```cmd
    reg query  [domain]\[key] /v [value]       # Query a single key value
    reg query  [domain]\[key] /v [value] /s    # Query a single key value recursively
  
    reg add    [domain]\[key]              # Add a key
    reg export [domain]\[key] output.reg   # Export subtree to file
    reg import output.reg                  # Import keys from file
```
## Remote Access

To dump a remote registry write something like
```cmd
    reg export \\[ip]\ [domain]\[key] output.reg
```    
