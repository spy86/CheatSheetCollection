### CLI Usage

-  DBUS - List Registered Services:
```shell
        # List system services
        dbus-send --system --dest=org.freedesktop.DBus --type=method_call --print-reply \
        /org/freedesktop/DBus org.freedesktop.DBus.ListNames | grep -v '":'

        # List session services
        dbus-send --session --dest=org.freedesktop.DBus --type=method_call --print-reply \
        /org/freedesktop/DBus org.freedesktop.DBus.ListNames | grep -v '":'
```
-   DBUS - Registry Locations:
```shell
        /usr/share/dbus-1/services/*.service
        /usr/share/dbus-1/system-services/*.service
        /usr/share/dbus-1/interfaces/*.xml
```
-   DBUS - Call RPC:
```shell
        dbus-send --session --dest=<class> <namespace> <method> [<parameters>]
```
    Example
```shell
        dbus-send --session --dest=org.gnome.feed.Reader \
          /org/gnome/feed/Reader \
          org.gnome.feed.Reader.Subscribe \
          string:http://osnews.com/files/recent.rdf
```
