ThinkStats2
===========

Text and supporting code for [Think Stats, 2nd Edition](http://greenteapress.com/thinkstats2/index.html)

Here's my configuration for using Python 3.6  for the ThinkStats2 codebase: (Environment: Mac OS X 10.11.6 with homebrew)

```
brew install openssl
brew install pyenv
brew install sqlite3
export CFLAGS="-I$(brew --prefix openssl)/include"
export LDFLAGS="-L$(brew --prefix openssl)/lib -L$(brew --prefix sqlite3)/lib"
export CPPFLAGS="-I$(brew --prefix sqlite3)/include"
PYTHON_CONFIGURE_OPTS="--enable-framework --enable-loadable-sqlite-extensions" pyenv install -v 3.6.0
```

I then added through `pip3 install` the following packages (current versions in parentheses) to get IPython working with all the packages listed in the section "Using the Code":

- ipython (5.1.0)
- jupyter (1.0.0)
- pandas (0.19.2)
- numpy (1.12.0)
- scipy (0.18.1)
- statsmodels (0.6.1)
- matplotlib (2.0.0)

Once I started IPython from the command prompt, I was able to run the `nsfg.py` code this way:

```
%run code/nsfg.py
```

and it reported "All tests passed."
