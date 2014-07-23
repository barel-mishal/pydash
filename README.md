# pydash

[![Package Version](http://img.shields.io/pypi/v/pydash.svg?style=flat)](https://pypi.python.org/pypi/pydash/)
[![Build Status](http://img.shields.io/travis/dgilland/pydash/master.svg?style=flat)](https://travis-ci.org/dgilland/pydash)
[![Coverage Status](http://img.shields.io/coveralls/dgilland/pydash/master.svg?style=flat)](https://coveralls.io/r/dgilland/pydash)
[![License](http://img.shields.io/pypi/l/pydash.svg?style=flat)](https://pypi.python.org/pypi/pydash/)


Python port of the [Lodash](http://lodash.com/) Javascript library.

Currently, alpha stage.

Current status of initial port: https://github.com/dgilland/pydash/issues/2


## Requirements

### Compatibility

- (maybe) Python 2.6
- Python 2.7
- (planned) Python 3

### Dependencies

None.


## Installation

```
pip install pydash
```

## Overview

### Differences between Lodash

- Function names use `snake_case` instead of `camelCase`.
- Any Lodash function which shares its name with a reserved Python keyword will have an `_` appended after it (e.g. `filter` in Lodash would be `filter_` in Pydash.
- Extra callback args must be explictly handled. In Javascript, it's perfectly fine to pass in extra arguments to a function that aren't explictly accepted by that function (e.g. `function foo(a1){}; foo(1, 2, 3);`). In Python, those extra arguments must be explictly handled (e.g. `def foo(a1, *args): ...; foo(1, 2, 3)`). Therefore, callbacks passed to `pydash` functions must use named args or a catch-all like `*args` since each callback is passed `item`, `index`, and `array`.


## License

This software is licensed under the MIT License.
