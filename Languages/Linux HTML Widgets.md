When you start a new open source project and decide to provide parts or the whole UI by an HTML widget you face the problem of first finding HTML widget libraries, especially light weight ones, and then using the correct one to avoid throwing away the code at a later point when you find one important feature missing. With this blog post I try to give a summary of existing open source HTML renderer libraries in the Linux world. I have some background experiences with the libraries from working on Liferea(http://liferea.sf.net) where we started with GtkHTML2, later added GtkMozembed support, then added Webkit support and finally switched to WebKit-only rendering.
The following table tries to summarize the simple availability of the different HTML renderers:

| Name        | Toolkit       | Platform | Derived From | Driving Force     | Active              |
|-------------|---------------|----------|--------------|-------------------|---------------------|
| KHTML       | QT            | %        | KDE          | KDE               | YES                 |
| wxHtml      | wxWidgets GTK | Windonws | KHTML        | wxWidgets         | YES                 |
| GtkHtml     | GTK+ 1.0      | GNOME 1  | KHTML        | GNOME 1           | No, long gone       |
| GtkHtml2    | GTK+ 2.0      | GNOME 2  | GtkHtml      | GNOME 2           | No, v2.11: Aug 2007 |
| GtkHtml3    | GTK+ 2.0      | GNOME 2  | GtkHtml      | Ximian, Evolution | No, v3.14: May 2008 |
| GtkMozEmbed | GTK+ 2.0      | Gecko    | %            | Mozilla           | Somewhat            |
| WebKitGtk   | GTK+ 2.0      | Webkit   | KHTML        | safari            | Yes                 |

## Note: 

My summary somewhat complements this Wikipedia list. Still it focusses more on Linux renderers and does correctly distinguish between the rather mad history of GtkHtml*. Given the list above one could conclude the only acceptable renderers are KTHML, wxHtml and WebkitGtk simply based on project activity. Still other renderers like GtkHtml2 and GtkHtml3 have gone a long way and provide a limited but stable functionality. But the important question is: What features are supported by the different renderers?

| NAME        | Widget Embed | Full HTML | CSS        | JS | Java | Flash Editor |
|-------------|--------------|-----------|------------|----|------|--------------|
| KHTML       | y            | y         | 1,2,3      | y  | y    | n            |
| wxHtml      | y            | n         | none       | n  | n    | n            |
| GtkHtml     | y            | y         | none       | n  | n    | y            |
| GtkHtml2    | y            | y         | 1,2,inline | n  | n    | n            |
| GtkHtml3    | y            | y         | none       | n  | n    | y            |
| GtkMozEmbed | n            | y         | 1,2,3      | y  | y    | n            |
| WebKitGtk   | n            | y         | 1,2,3      | y  | y    | n            |

The feature matrix along with the platform listing explains why a lot of those old renderer libraries are still around. Given you want to render simple markup in an email client you might still choose wxHtml or GtkHtml3, with the latter one providing you with a HTML editor for rich mail editing. Of course when you want to allow your users to have fully fledged inline browsing you need to use either KTHML, GtkMozEmbed or Webkit. Currently I believe WebKitGtk to be the best choice as it's widget gets a lot of attention, which GtkMozEmbed never had while being unstable and rather limited at the same time. If you find mistakes or have something to add please post a comment!