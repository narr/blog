---
title: A task to handle URI
date: 2016-08-09 23:29:25
tags:
- task
- URI
- URL
---
### Write a function, checkURIs(uri1, uri2) that can check if 2 URIs are equivalent. The function should return true if match, and false otherwise
<br>
### Constraints and assumptions are as follow:
### A port that is empty, or not given, is equivalent to the default port of 80
### Comparisons of scheme names must be case-insensitive
### Comparisons of host names must case-insensitive
### Comparisons of path, hash, and querystring must be case-sensitive
### Paths may contain traversal tokens . (same dir) and .. (one dir up) which must be accounted for
### Characters are equivalent to their % HEX HEX encodings. (Other than typical reserved characters in urls like , / ? : @ & = + $ #)
### Query string parameters must be equivalent in arbitrary order, BUT query string arguments of the same name must be listed in the same order in both URIs to be equivalent. There may be multiple (not just 2) args of the same name that need to be accounted for.
### In-URI basic auth may be present: e.g. http://uname:passwd@host.com/foo/bar.html, auth must be case-sensitive

<br>
#### example:

```javascript
checkURIs('http://abc.com:80/~smith/home.html',
  'http://ABC.com/%7Esmith/home.html'); // true

checkURIs('http://abc.com/drill/down/foo.html',
  'http://abc.com/drill/further/../down/./foo.html'); // true

checkURIs('http://abc.com/foo.html?a=1&b=2',
  'http://abc.com/foo.html?b=2&a=1'); // true

checkURIs('http://abc.com/foo.html?a=1&b=2&a=3',
  'http://abc.com/foo.html?a=3&a=1&b=2'); // false
```

<!-- more -->

<br>{% codepen narr mEQoOG 0 js 4300 100% %}
