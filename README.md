# Jonathan's Python

A curated list of awesome Python frameworks, libraries, software, and resources.
And a few warnings away from others that are, IMHO, not so awesome.

Inspired by, and often cribbed from,
[Awesome Python](https://github.com/vinta/awesome-python).
That list is far more comprehensive, terse, and invariably positive.
This one, in contrast, only recommends tools I've personally used
and love. It explains a bit more why I use these, as opposed to other
available tools. It is intentionally opinionated, giving negative reviews
as well. It will also unabashedly include my own modules,
developed to fill gaps I've found.

- [Jonathan's Python](#jonathans-python)

    - [Compatibility](#compatibility)
    - [Configuration](#configuration)
    - [Data Analysis](#data-analysis)
    - [Data Visualization](#data-visualization)
    - [Date and Time](#date-and-time)
    - [Debugging Tools](#debugging-tools)
    - [Documentation](#documentation)
    - [Editor Plugins and IDEs](#editor-plugins-and-ides)
    - [Functional Programming](#functional-programming)
    - [HTML Manipulation](#html-manipulation)
    - [HTTP](#http)
    - [Imagery](#imagery)
    - [Implementations](#implementations)
    - [Interactive Interpreter](#interactiveinterpreter)
    - [Package Management](package-management)
    - [Specific Formats Processing](#specific-formats-processing)
    - [Text Processing](#text-processing)
    - [Third-party APIs](#third-party-apis)
    - [Web Frameworks](#web-frameworks)
    - [Code Quality](#code-quality)
    - [Continuous Integration](#continuous-integration)


- - -

## Compatibility

*Libraries for migrating from Python 2 to 3.*

* [Six](https://pypi.python.org/pypi/six) - Python 2 and 3 compatibility utilities. This is my essential bridge between 2 and 3.


## Configuration

*Libraries for storing and parsing configuration options.*

* [options](https://pypi.python.org/pypi/options) - My own design. The most flexible manager of program, module, class, instance, method, and function options in any programming language, anywhere. By far.

## Data Analysis

*Libraries for data analyzing.*

* [NumPy](http://www.numpy.org/) - Essential library for optimized math in Python. API occasionally undisciplined in a way more often seen in PHP and C, but its results are exceptional.
* [Pandas](http://pandas.pydata.org/) - Pandas' Series and DataFrames data structures add sophisticated indices, file I/O, and query and manipulation methods atop NumPy arrays. Like a spreadsheet in Python code. Steepish learning curve, but *so* worth it.
* [Pandas](http://pandas.pydata.org/) - Pandas' Series and DataFrames data structures add sophisticated indices, file I/O, and query and manipulation methods atop NumPy arrays. Like a spreadsheet in Python code. Steepish learning curve, but *so* worth it.


## Data Visualization

*Libraries for visualizing, plotting, or displaying data. See also: [awesome-javascript](https://github.com/sorrycc/awesome-javascript#data-visualization).*

* [Bokeh](https://github.com/bokeh/bokeh) - Marriage of d3.js and Python.
* [Matplotlib](http://matplotlib.org/) - The essential/foundation Python plotting library. API(s) derive from MATLAB, R, etc. and can be undisciplined, but with a little tweaking, strong results possible. Easily saves output to PNG and SVG.


## Date and Time

*Libraries for working with dates and times.*

* [arrow](https://github.com/crsmithdev/arrow) - Better dates & times. Esp. helpful managing and adjusting for timezones, a task for which the standard `datetime` sucks like a Hoover.
* [dateutil](https://github.com/dateutil/dateutil) - Extensions to the standard Python [datetime](https://docs.python.org/2/library/datetime.html) module. Especially good for parsing date strings, a task that is otherwise hard to accomplish in Python.

* [Perl's Date::Manip](http://search.cpan.org/~sbeck/Date-Manip-6.57/lib/Date/Manip.pod) the most sophisticated date management library I've seen, esp. for parsing human-entered dates and logical time intervals. Sadly know of no analog in Python.

## Debugging Tools

*Libraries for debugging code.*

* [show](https://pypi.python.org/pypi/show). My own design. Debug print statements done right.


## Documentation

*Libraries for generating project documentation.*

* [Sphinx](http://www.sphinx-doc.org/en/latest/) - Foundation Python Documentation generator. Both love and hate it. RST (ReStructured Text) is semantically more sophisticated than Markdown, but gratuitously different in numerous annoying ways. Markdown needs to be upgraded, and RST needs to be phased out in its favor. Until then, there's Sphinx and RST.
    * [awesome-sphinxdoc](https://github.com/yoloseem/awesome-sphinxdoc)


## Editor Plugins and IDEs

Use an IDE, okay?

* IDE
    * [Komodo IDE](http://www.activestate.com/komodo-ide) - Commercial IDE for Python, JavaScript, HTML, XML, CSS, Ruby, Go, Perl.... Everything in one place.
    * [PyCharm](https://www.jetbrains.com/pycharm/) - Commercial Python IDE by JetBrains. Has free community edition available.

## Functional Programming

*Functional Programming with Python.*

* [funcy](https://github.com/Suor/funcy) - A fancy and practical functional tools.
* [Toolz](https://github.com/pytoolz/toolz) - A collection of functional utilities for iterators, functions, and dictionaries.


## HTML Manipulation

*Libraries for working with HTML and XML.*

* [lxml](http://lxml.de/) - Fast, versatile, powerful library for parsing and manipulating HTML and XML. Uses ElementTree API. Excellent XPath implementation. Very extensible.

* Perl's XML::Twig - Sadly no direct Python equivalent.

## HTTP

*Libraries for working with HTTP.*

* [requests](http://docs.python-requests.org/en/latest/) - HTTP Requests for Humans™. Much nicer than historical Python standard library approaches. Similar to the Arrow time/date library, markedly up-levels code.
* [requests-cache](https://pypi.python.org/pypi/requests-cache) - A cache to use when developing code with  requests`. Don't make 46 identical requests; service hosts don't like that. Also, it's slow. Use a cache.

## Imagery

*Libraries for manipulating images.*

* [pillow](https://github.com/python-pillow/Pillow) - Pillow is the friendly [PIL](http://www.pythonware.com/products/pil/) fork. The essential Python image manipulation library.

## Implementations

*Implementations of Python.*

* [Jython](https://hg.python.org/jython) - Implementation of Python programming language written in Java for the Java virtual machine (JVM). I used to test all my libraries against Jython and to be hopeful for a JVM-resident Python, but my hopes for it have dimmed over time. Development is slow and the versions are back-level vs. standard CPython. It also doesn't easily support C-implemented libraries like `lxml` and `numpy` which are essential to much of my code. The standard execution environment now seems to be Linux-in-the-cloud, not JVM. Time marches on. Still, love it as an old fling.
* [PyPy](https://bitbucket.org/pypy/pypy) - Accelerated JIT implementation of Python. Good currency with CPython. I test and certify all my code against PyPy, and occasionally use it when CPython isn't fast enough.


## Interactive Interpreter

*Interactive Python interpreters (REPL).*

* [bpython](https://github.com/bpython/bpython) - A better Python interpreter. Highly recommended. Friends don't let friend REPL.
* [Jupyter Notebook (IPython)](https://jupyter.org) - A rich toolkit to help you make the most out of using Python interactively, including interactive documentation in Markdown and Latex math expressions. I spend at least half my Python development time in Jupyter Notebook / IPython. Also supports other langauges, such as JavaScript, Perl, .... Enthusiastically recommended.


## Package Management

*Libraries for package and dependency management.*

* [wheel](http://pythonwheels.com/) - The new standard of Python distribution and are intended to replace eggs. All my packages are built for wheel distribution.

## Package Repositories

*Local PyPI repository server and proxies.*

* [warehouse](https://github.com/pypa/warehouse) - Next generation Python Package Repository (PyPI).
    * [Warehouse](https://pypi.org/)
* [bandersnatch](https://bitbucket.org/pypa/bandersnatch) - PyPI mirroring tool provided by Python Packaging Authority (PyPA).
* [devpi](http://doc.devpi.net/latest/) - PyPI server and packaging/testing/release tool.
* [localshop](https://github.com/mvantellingen/localshop) - Local PyPI server (custom packages and auto-mirroring of pypi).

## Permissions

*Libraries that allow or deny users access to data or functionality.*

* [Carteblanche](https://github.com/neuman/python-carteblanche/) - Module to align code with thoughts of users and designers. Also magically handles navigation and permissions.
* [django-guardian](https://github.com/django-guardian/django-guardian) - Implementation of per object permissions for Django 1.2+
* [django-rules](https://github.com/dfunckt/django-rules) - A tiny but powerful app providing object-level permissions to Django, without requiring a database.

## Specific Formats Processing

*Libraries for parsing and manipulating specific text formats.*

* General
    * [openpyxl](https://openpyxl.readthedocs.io/) - A library for reading and writing Excel 2010 xlsx/xlsm/xltx/xltm files.
    * [XlsxWriter](https://xlsxwriter.readthedocs.io) - A Python module for creating Excel .xlsx files.

* Markdown
    * [Python-Markdown](https://github.com/waylan/Python-Markdown) - A Python implementation of John Gruber’s Markdown.
* YAML
    * [PyYAML](http://pyyaml.org/) - YAML implementations for Python.


## Testing

*Libraries for testing codebases and generating test data.*

Testing is annoying and has a highish learning curve. But nothing will
imporve your code quality more than solid testing. Nothing.

* Testing Frameworks
    * [pytest](http://pytest.org/latest/) - Testing done right. Simple assertions, no extra boilerplate.
    * Avoid [unittest](https://docs.python.org/2/library/unittest.html) and similar high-boilerplate, unit-test-centric, Java-derived tools.

* Test Runners
    * [tox](https://tox.readthedocs.io/) - Auto builds and tests distributions in multiple Python versions. All my code is tested across N different Python versions. Highly recommended.

* Code Coverage
    * [coverage](https://pypi.python.org/pypi/coverage) - Code coverage measurement. Line or branch coverage. Helps game-ify the testing process, which is surprisingly motivational. Gives strong insights as to "what needs to be tested next?"

* Wish that Python test runners enjoyed some of the visual fluidity enjoyed by JavaScript's Mocha and Istanbul tools.

## Text Processing

*Libraries for parsing and manipulating plain texts.*

* General
    * [chardet](https://github.com/chardet/chardet) - Python 2/3 compatible character encoding detector.
    * [difflib](https://docs.python.org/2/library/difflib.html) - (Python standard library) Helpers for computing deltas.
    * [ftfy](https://github.com/LuminosoInsight/python-ftfy) - Makes Unicode text less broken and more consistent automagically.
    * [fuzzywuzzy](https://github.com/seatgeek/fuzzywuzzy) - Fuzzy String Matching.
    * [Levenshtein](https://github.com/ztane/python-Levenshtein/) - Fast computation of Levenshtein distance and string similarity.
    * [pangu.py](https://github.com/vinta/pangu.py) - Spacing texts for CJK and alphanumerics.
    * [pyfiglet](https://github.com/pwaller/pyfiglet) - An implementation of figlet written in Python.
    * [shortuuid](https://github.com/stochastic-technologies/shortuuid) - A generator library for concise, unambiguous and URL-safe UUIDs.
    * [unidecode](https://pypi.python.org/pypi/Unidecode) - ASCII transliterations of Unicode text.
    * [uniout](https://github.com/moskytw/uniout) - Print readable chars instead of the escaped string.
    * [xpinyin](https://github.com/lxneng/xpinyin) - A library to translate Chinese hanzi (漢字) to pinyin (拼音).
* Slugify
    * [awesome-slugify](https://github.com/dimka665/awesome-slugify) - A Python slugify library that can preserve unicode.
    * [python-slugify](https://github.com/un33k/python-slugify) - A Python slugify library that translates unicode to ASCII.
    * [unicode-slugify](https://github.com/mozilla/unicode-slugify) - A slugifier that generates unicode slugs with Django as a dependency.
* Parser
    * [phonenumbers](https://github.com/daviddrysdale/python-phonenumbers) - Parsing, formatting, storing and validating international phone numbers.
    * [PLY](http://www.dabeaz.com/ply/) - Implementation of lex and yacc parsing tools for Python
    * [Pygments](http://pygments.org/) - A generic syntax highlighter.
    * [pyparsing](http://pyparsing.wikispaces.com/) - A general purpose framework for generating parsers.
    * [python-nameparser](https://github.com/derek73/python-nameparser) - Parsing human names into their individual components.
    * [python-user-agents](https://github.com/selwin/python-user-agents) - Browser user agent parser.
    * [sqlparse](https://github.com/andialbrecht/sqlparse) - A non-validating SQL parser.

## Third-party APIs

*Libraries for accessing third party services APIs. See: [List of Python API Wrappers and Libraries](https://github.com/realpython/list-of-python-api-wrappers).*

* [boto3](https://github.com/boto/boto3) - Python interface to Amazon Web Services.
* [gspread](https://github.com/burnash/gspread) - Google Spreadsheets Python API.

## Web Frameworks

*Full stack web frameworks.*

* [Django](https://www.djangoproject.com/) - The most popular web framework in Python.
    * [awesome-django](https://github.com/rosarior/awesome-django)
* [Flask](http://flask.pocoo.org/) - A microframework for Python.
    * [awesome-flask](https://github.com/humiaozuzu/awesome-flask)
* [Tornado](http://www.tornadoweb.org/en/latest/) - A Web framework and asynchronous networking library.
* Avoid [Bottle](http://bottlepy.org/docs/dev/index.html), [CherryPy](http://www.cherrypy.org/), [Pyramid](http://www.pylonsproject.org/), [TurboGears](http://www.turbogears.org/), [Web2py](http://www.web2py.com/), Twisted. IMO, time has passed these by. I do not see the energy, community, or speed of development in these that I do in Flask, Django, and Tornado.

# Services

Online tools and APIs to simplify development.

## Continuous Integration

*See: [awesome-CIandCD](https://github.com/ciandcd/awesome-ciandcd#online-build-system).*

* [CircleCI](https://circleci.com/) - A CI service that can run very fast parallel testing.
* [Travis CI](https://travis-ci.org) - Popular CI service. Works well with open source  projects. (GitHub only)
