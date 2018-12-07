When you start a new open source project and decide to provide parts or the whole UI by an HTML widget you face the problem of first finding HTML widget libraries, especially light weight ones, and then using the correct one to avoid throwing away the code at a later point when you find one important feature missing.

With this blog post I try to give a summary of existing open source HTML renderer libraries in the Linux world. I have some background experiences with the libraries from working on <a href="http://liferea.sf.net">Liferea</a> where we started with GtkHTML2, later added GtkMozembed support, then added Webkit support and finally switched to WebKit-only rendering.

The following table tries to summarize the simple availability of the different HTML renderers:

