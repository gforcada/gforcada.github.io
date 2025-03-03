Title: ajuda del python
Date: 2008-07-24 13:48
Author: admin
Category: General
Tags: python
Slug: ajuda-del-python
Status: published
Attachments: wp-content/uploads/2008/07/python_logo.png

<img src="{static}wp-content/uploads/2008/07/python_logo.png" data-align="right" alt="Logotip del Python" />Recordatori per a mi mateix i per a qui pensi que li és útil :)

**dir(***tipus variable o objecte ja declarat***)**

Amb això ens mostra totes les funcions que podem utilitzar sobre un tipus de dada, per exemple:

**dir(str)**

    ['__add__', '__class__', '__contains__', '__delattr__', '__doc__', '__eq__', '__ge__',
    '__getattribute__', '__getitem__', '__getnewargs__', __getslice__', '__gt__',
    '__hash__', '__init__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__',
    '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmod__', '__rmul__',
    '__setattr__', '__str__', 'capitalize', 'center', 'count', 'decode', 'encode',
    'endswith', 'expandtabs', 'find', 'index', 'isalnum', 'isalpha', 'isdigit', 'islower',
    'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'partition', 'replace',
    'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith',
    'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']

I per saber què fa, per exemple, zfill, només cal que teclajem:

**help(str.zfill)**

    zfill(...)
    S.zfill(width) -> string

    Pad a numeric string S with zeros on the left, to fill a field
    of the specified width.  The string S is never truncated.
