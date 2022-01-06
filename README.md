# Python Distilled

![](images/cover.jpg)

Welcome!  This repo contains errata related to the [Python
Distilled](https://www.dabeaz.com/python-distilled) book by [David Beazley](https://www.dabeaz.com).
If you'd like to contribute, please submit an issue or pull request.

## Errata

* Table 1.2. Description for `round(a, [n])` should state that it rounds to the nearest multiple of 10 to the -nth power.

* Section 6.4, pg. 145.   The code for `print_matching()` should be as follows:

```python
def print_matching(lines, substring):
    for line in lines:
        if substring in line:     # line instead of lines
	    print(substring)
```

* Section 7.28, pg. 212.   `del f.owner` should be `del a.owner` in example.

## Acknowledgements

The following individuals have contributed errata:

* Said Klundert
* David Dyck
* Scythal


