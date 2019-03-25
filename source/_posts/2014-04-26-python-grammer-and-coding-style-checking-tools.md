---
title: Python grammer and coding style checking tools
date: 2014-04-26 17:06:00
comments: true
categories: Tutorials
tags:
	- Python
	- Programming
---

In this post, several python/C coding style documentaion and static chekcing tools are introduced.

<!-- more -->

## Style recommendations

The main proposals in python ecosystem is indexed by [PEPs (Python Enhancement Proposals)](http://legacy.python.org/dev/peps/) whose index number is allocated by the PEP editors. In PEPs, the [7th](http://legacy.python.org/dev/peps/pep-0007/) and [8th](http://legacy.python.org/dev/peps/pep-0008/) proposals defines the C and Python coding styles recommended.

Another important feature in Python is a clear and readable in-code documentation, also called "docstring" in python. [PEP257](http://legacy.python.org/dev/peps/pep-0257/) shows a simple recommendation about that.

<!-- more -->

## Static checking tools

Brilliant pythoners have contributed several wonderful grammer/style analyzing tools in accordance with PPE8 recommendation, such as [flake8](https://pypi.python.org/pypi/flake8), [pep8](https://pypi.python.org/pypi/pep8), [PyChecker](http://pychecker.sourceforge.net/), [PyFlakes](https://pypi.python.org/pypi/pyflakes), [PyLint](http://www.pylint.org/) etc. For my faviorate, flake8 meets most of my requirements in daily programming. But you can choose a suitable one for yourself. For others' opinions, you can follow the [thread on SO](http://stackoverflow.com/q/35470/1320284).


## Editor plugins

For Sublime Text, flake8 has its plugin [Flake8Lint](https://github.com/dreadatour/Flake8Lint). You can also ask google about your package option. In Eclipse, pep8 is integrated in PyDev (2.3.0+) by default. You can enable it manully if its not activated in your settings:

`Open Window` > `Preferences` > `PyDev` > `Editor` > `Code Analysis` > `pep8.py`
