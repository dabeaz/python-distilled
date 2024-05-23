# Python Distilled

![](images/cover.jpg)

Welcome!  This repo contains errata related to the [Python
Distilled](https://www.dabeaz.com/python-distilled) book by [David Beazley](https://www.dabeaz.com).
If you'd like to contribute, please submit an issue or pull request.

## Errata

* Table 1.2, pg. 5. Description for `round(a, [n])` should state that it rounds to the nearest multiple of 10 to the -nth power.

* Section 1.6, pg. 10.  Comment in code sample mid-page should read `# g = 'Hello Cruel World'`.

* Table 1.6, pg. 10. Description for `s.endswith(prefix [,start [,end]])` would be better if it used `suffix` instead
of `prefix`.

* Section 1.8, pg. 15.  `['SYM', '123', '456.78']` should include the newline and be `['SYM', '123', '456.78\n']`

* Section 1.15, pg. 26.  `print "Going away..."` should be `print("Going away...")`

* Section 2.1, pg. 38. Typo mid-page should read "Tuple, list, set, and dictionary literals are written as follows:"

* Section 2.7, pg. 43.  Truthiness should be expanded to include sets and any non-empty container.  "... any nonzero number,
a nonempty string, list, tuple, set, dictionary, or container is taken to be true."

* Section 2.7, pg. 44.  The function invocation of `foo(3, a)` should be `f(3, a)`.

* Section 2.14, pg. 52. The list comprehension example should use `squares` instead of `nums`.

```python
nums = [1, 2, 3, 4, 5]
squares = [ ]
for n in nums:
    squares.append(n*n)
```

* Section 4.8, pg. 88.  `compute_cost(prices, quantities)` should be `compute_cost(prices, units)`.

* Section 5.8, pg. 106.  The docstring in the `factorial()` function should use `factorial(5)`
instead of `factorial(6)` to get a result of 120.

* Section 6.4, pg. 145.   The code for `print_matching()` should be as follows:

```python
def print_matching(lines, substring):
    for line in lines:
        if substring in line:     # line instead of lines
	    print(substring)
```


* Section 7.3, pg. 156.  Missing right parenthesis on `b.withdraw(50.0)`.

* Section 7.7, pg. 160.   Perhaps the class should be called `MyAccount` instead
of `MyAcount`.   Although, it's inheritance--you can call the class whatever you
want!

* Section 7.12, pg. 172. Comment in code right before section 7.13 should read
`# Calls Date.today(Date)`.

* Section 7.21, pg. 194.  The code for `register_decoder()` should use `mt` instead
of `mt.mimetype`.  For example:

```python
_registry = { }
def register_decoder(cls):
    for mt in cls.mimetypes:
        _registry[mt] = cls
    return cls
```

* Section 7.23, pg. 200.   Typo in constructor example at the top.  Should be

```python
a = Account.__new__(Account, 'Guido', 1000.0)
if isinstance(a, Account):
    a.__init__('Guido', 1000.0)
```

The example that follows should also be corrected to:

```python
a = Account.__new__(Account)
a.__init__('Guido', 1000.0)
```

* Section 7.23, pg. 200.   Typos in the date `today()` constructor.  Should be

```python
@classmethod
def today(cls):
    t = time.localtime()
    self = cls.__new__(cls)    # Make instance
    self.year = t.tm_year
    self.month = t.tm_mon
    self.day = t.tm_mday
    return self
```

* Section 7.26, pg. 208.  Typo (missing "that").  "A proxy is an object that exposes..."

* Section 7.28, pg. 212.   `del f.owner` should be `del a.owner` in example.

* Section 9.3, pg. 250. `format(x, '<*10.2f')` should be `format(x, '*<10.2f')`.

* Section 9.3, pg. 250.  "The general format of the format specifier should be `[fill][align][sign][0][width][,][.precision][type]` where each part enclosed in `[]` is optional."

* Section 9.3, pg, 252. `'Value is {val:<*10.2f}'.format(val=x)` should be `'Value is {val:*<10.2f}'.format(val=x)`.

* Section 9.3, pg, 253. Comment in code sample at bottom third of the page should be changed from `# b'The value is 123.46'` to `# b'Value is 123.46'`.

* Section 9.9, pg. 264. `for filename in path.Path('dirname').glob('*.txt')` should be `for filename in pathlib.Path('dirname').glob('*.txt')`.

* Section 9.15.9, pg. 279.   Typo, missing "to" in the sentence "Go to a directory with a collection of files and type the following:"

* Section 9.15.15, pg. 283. There is an extra `return pathname.stat().st_size` statement that
can be removed (because there is a `return` statement right above it).

* Section 9.15.19, pg. 285.  `serv` should be `server` in the SMTP example:

```python
server = smtplib.SMTP('localhost')
server.sendmail(fromaddr, toaddrs, msg)
server.quit()
```

* Section 9.15.21, pg. 288.  The output of `struct.pack()` should be as follows:

```
>>> struct.pack(">HIff", 123, 456, 1.23, 4.56)
b'\x00{\x00\x00\x01\xc8?\x9dp\xa4@\x91\xeb\x85'
>>>
```

* Section 10.1, pg. 308.  The description of `round()` should start with "Returns the result of rounding the floating-point number..."

* Table 10.9, pg. 311.    The description for `format_map()` should use "taken" instead of "taking".   "Formats `s` with substitutions taken from the mapping m."

* Table 10.10, pg.  The description for `s + t` should read "Concatenation if `t` is a tuple."

* Table 10.10, pg, 313.  The `s.append(x)` method should be deleted.

## Acknowledgements

The following individuals have contributed errata:

* Jonathan Oberländer
* Lucas Plaetevoet
* Chris Gibson
* Lawrence Wu
* Andy Lester
* Siavash Tavakoli
* Said van de Klundert
* David Dyck
* Scythal
* Feng Guo
* Xavier Noria
* Evan Friedenberg
* Karthik-d-k
* Marc Hertzog
* Jack Rubin
* Paul Barry
* @physadair
* @phils4000
* @michrag
* Sam Kramer
* @wildekat


