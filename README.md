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

* Section 2.7, pg. 44.  The function invocation of `foo(3, a)` should be `f(3, a)`.

* Section 2.14, pg. 52. The list comprehension example should use `squares` instead of `nums`.

```python
nums = [1, 2, 3, 4, 5]
squares = [ ]
for n in nums:
    squares.append(n*n)
```

* Section 4.8, pg. 88.  `compute_cost(prices, quantities)` should be `compute_cost(prices, units)`.

* Section 6.4, pg. 145.   The code for `print_matching()` should be as follows:

```python
def print_matching(lines, substring):
    for line in lines:
        if substring in line:     # line instead of lines
	    print(substring)
```

* Section 7.3, pg. 156.  Missing right parenthesis on `b.withdraw(50.0)`.

* Section 7.12, pg. 172. Comment in code right before section 7.13 should read
`# Calls Date.today(Date)`.

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

* Section 9.15.19, pg. 285.  `serv` should be `server` in the SMTP example:

```python
server = smtplib.SMTP('localhost')
server.sendmail(fromaddr, toaddrs, msg)
server.quit()
```

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



