untangle 
========

* Converts XML to a Python object. 
* Siblings with similar names are grouped into a list. 
* Children can be accessed with ``parent.child``, attributes with ``element['attribute']``.
* You can call the ``parse()`` method with a filename, an URL or an XML string.
* Substitutes ``-`` with ``_`` so ``<foobar><foo-bar/></foobar>`` can be accessed with ``foobar.foo_bar``

Usage
-----
(See and run <a href="https://github.com/stchris/untangle/blob/master/examples.py">examples.py</a> for more info)

```python
import untangled
obj = untangled.parse(resource)
```

``resource`` can be:

* an URL
* a filename
* an XML string

This XML:

```xml
<?xml version="1.0"?>
<root>
	<child name="child1">
</root>
```
can be navigated from the untangled object like this:

```python
obj.root.child['name'] # u'child1'
```

