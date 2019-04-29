### Syntax

Here is the syntax of important subprocess functions

    <status> = subprocess.call         (<command array>[, <options>])
    <status> = subprocess.check_call   (<command array>[, <options>])
    <string> = subprocess.check_output (<command array>[, <options>])
    <Popen>  = subprocess.Popen        (<command array>[, <options>])

### Basic Example

    import subprocess

    subprocess.call(['find', '/etc', '-name', '*.conf'])

In the example a program named \'find\' is executed without a shell. To
launch the command in a shell pass \'shell=True\' in the list of options

    subprocess.call(['find', '/'], shell=True)

### Catching STDOUT

To collect all output of a command executed use check\_output()

    output = subprocess.check_output(["ls"])

### Redirecting STDERR

When you only want to redirect STDERR to STDIN and catch this output
too, simply add \'stderr=subprocess.STDOUT\' as an option when calling
check\_output()

    output = subprocess.check_output(["unknown_command"], stderr=subprocess.STDOUT)

### Complex Pipe Use Cases

To also handle STDIN, STDOUT and STDERR you need use Popen() and
Popen.communicate() to write and read from/to those pipes.

    # Launch command with all pipes connected
    p = subprocess.Popen(['rm', '-i', '*'], stdin=subprocess.PIPE, stdout=subprocess.PIPE, stderr=subprocess.PIPE)

    # Pass exactly one 'y' and read output
    (out, err) = p.communicate('y')

    # Check return code
    if p.returncode != 0:
        print("Error!")

Don\'t forget to pass a \'stdxx=subprocess.PIPE\' option for each pipe
you want to use

### Passing Environment Variables

    Popen(["ls"], env={"PATH": "/usr/local/bin"})
