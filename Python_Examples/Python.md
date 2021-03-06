# HowTo

-   [Ad-hoc
    Webserver](https://docs.python.org/2/library/simplehttpserver.html)
```python
        import SimpleHTTPServer
        import SocketServer

        PORT = 8000

        Handler = SimpleHTTPServer.SimpleHTTPRequestHandler

        httpd = SocketServer.TCPServer(("", PORT), Handler)

        print "serving at port", PORT
        httpd.serve_forever()
```
-   Python - Value Dumping
```python
        # For scalars and dictionaries
        print(vars(somevar))

        # For hashes
        from pprint import pprint
        pprint(h)
```
-   Python - Installing Modules via PIP
```shell
        apt-get install python-pip  # Python 2.x
        apt-get install python-pip3 # Python 3.x

        pip install <module>
        pip install --upgrade <module>
        pip uninstall <module>
        pip freeze   # Prints all versions
        pip3 install <module>
```
-   Python - PEP Linting
```shell
        pip3 install pyflakes
        pip3 install pep8
```
-   [Python - PyGtk Example
    Snippets](http://www.eurion.net/python-snippets/snippet/)
-   [Python - Google Coding Style
    Guide](http://google-styleguide.googlecode.com/svn/trunk/pyguide.html)
-   [Python - Django Best
    Practices](http://lincolnloop.com/django-best-practices/)
-   [Python - Types and
    Objects](http://www.cafepy.com/article/python_types_and_objects/python_types_and_objects.html#basic-concepts)
-   [Python - Debugging Memory
    Leaks](http://chase-seibert.github.io/blog/2013/08/03/diagnosing-memory-leaks-python.html)

