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

Philosophy: You don't need N different libraries/frameworks to accomplish
the same task. You need one really solid one that is your go-to, with
some knowledge of (and possibly experience with) a few others as backups for
specific requirements your primary tool may not nail.

Contributions to and recommendations for this list are welcome, but
are strictly advisory.

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
    - [HTML and XML Manipulation](#html-and-xml-manipulation)
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

* [Six](https://pypi.python.org/pypi/six) - Python 2 and 3 compatibility utilities.
  This is has been my essential bridge between 2 and 3.
  That said, nowadays you should *strongly* favor Python 3. All compatibility code
  should key off Python 3 being the natural default environment, and Python 2 the
  outlier. E.g. `if _PY2:` conditionals not `if _PY3:`.

## Configuration

* [options](https://pypi.python.org/pypi/options) - My own design. The most flexible manager of program, module, class, instance, method, and function options in any programming language, anywhere. By far.

## Data Analysis

* [NumPy](http://www.numpy.org/) - Essential library for optimized math in Python. API occasionally undisciplined in a way more often seen in PHP and C, but its results are exceptional.
* [Pandas](http://pandas.pydata.org/) - Pandas' Series and DataFrames data structures add sophisticated indices, file I/O, and query and manipulation methods atop NumPy arrays. Like a spreadsheet in Python code. Steep-ish learning curve, but *so* worth it.

## Data Visualization

* [Bokeh](https://github.com/bokeh/bokeh) - Marriage of d3.js and Python.
* [Matplotlib](http://matplotlib.org/) - The essential/foundation Python plotting
  library. API(s) derive from MATLAB, R, etc. and can be undisciplined, but with a
  little tweaking, strong results possible. Easily saves output to PNG and SVG.


## Date and Time

* [arrow](https://github.com/crsmithdev/arrow) - Better dates & times. Esp. helpful managing and adjusting for timezones, a task for which the standard `datetime` sucks like a Hoover.
* [dateutil](https://github.com/dateutil/dateutil) - Extensions to the standard Python [datetime](https://docs.python.org/2/library/datetime.html) module. Especially good for parsing date strings, a task that is otherwise hard to accomplish in Python.

* [Perl's Date::Manip](http://search.cpan.org/~sbeck/Date-Manip-6.57/lib/Date/Manip.pod) the most sophisticated date management library I've seen, esp. for parsing human-entered dates and logical time intervals. Sadly know of no analog in Python.

## Debugging Tools

* [show](https://pypi.python.org/pypi/show). My own design. Debug print statements
  done right.


## Documentation

* [Sphinx](http://www.sphinx-doc.org/en/latest/) - Foundation Python Documentation generator. Both love and hate it. RST (ReStructured Text) is semantically more sophisticated than Markdown, but gratuitously different in numerous annoying ways. Markdown needs to be upgraded, and RST needs to be phased out in its favor. Until then, there's Sphinx and RST.
    * [awesome-sphinxdoc](https://github.com/yoloseem/awesome-sphinxdoc)


## Editor Plugins and IDEs

Use an IDE, okay? `vi` and `emacs` are so 1985.

* [Project Jupyter](http://jupyter.org/) - Project Jupyter and its generalization of
  IPython notebooks to multiple languages and web UIs is
  amazing. Completely transforms your programming experience,
  I find more and more of my development time spent in Jupyter Notebooks,
  then moved to IDEs.
* [JupyterLab](https://github.com/jupyterlab) - JupyterLab is an extension to,
  and the next generation of, Jupyter Notebook.
  They say "very early pre-alpha developer preview" and "not ready for general usage yet."
  Bullshit. Even in preview status, it's become my go-to development
  place.
* [Komodo IDE](http://www.activestate.com/komodo-ide) - Commercial IDE for Python,
  JavaScript, HTML, XML, CSS, Ruby, Go, Perl.... Everything in one place. Has been my
  primary development tool for many years.
* [PyCharm](https://www.jetbrains.com/pycharm/) - Commercial Python IDE by JetBrains.
  Has free community edition available. I use it only occasionally, but my
  students use it often. Excellent value inspector in the debugger.

## Functional Programming

* `itertools` from the standard library - Hugely useful. Enables higher-level programming,
  especially with collections and sequences.
  Often makes complex problems simple.
  Grouping, permutations, and different patterns of
  processing are helped. Perhaps not strictly functional, but related.
  Wish that some of the generators given as cookbook recopies were actually implemented
  in the code.
* [more-itertools](https://more-itertools.readthedocs.io/en/latest/api.html) - A project
  that picks up where `itertools` leaves off. Implements the `itertools` recipes,
  and provides a whole range of other patterns. Need a random permutation?
  A list flattener? Iterleaved iteration? It's got it!
* [funcy](https://github.com/Suor/funcy) - A fancy and practical functional tools.
* [Toolz](https://github.com/pytoolz/toolz) - A collection of functional utilities for iterators, functions, and dictionaries.


## HTML and XML Manipulation

* [lxml](http://lxml.de/) - Fast, versatile, powerful library for parsing and manipulating HTML and XML. Uses ElementTree API. Excellent XPath implementation. Very extensible.

* Perl's XML::Twig - Sadly no direct Python equivalent. Yet.

## HTTP

* [requests](http://docs.python-requests.org/en/latest/) - HTTP Requests for Humans™. Much nicer than historical Python standard library approaches. Similar to the Arrow time/date library, markedly up-levels code.
* [requests-cache](https://pypi.python.org/pypi/requests-cache) - A cache to use when developing code with  requests`. Don't make 46 identical requests; service hosts don't like that. Also, it's slow. Use a cache.

## Imagery

* [pillow](https://github.com/python-pillow/Pillow) - Pillow is the friendly [PIL](http://www.pythonware.com/products/pil/) fork. The essential Python image manipulation library.

## Implementations

* Python 3, not Python 2. It's time to migrate whole-heartedly.

  Like many, I was laggardly in making the switch. Even after Python 3
  started getting good (3.3 timeframe, IMO), there just wasn't enough positive reason to
  make the jump, considering how good Python 2.7 was, how often it was the default version,
  and general inertia. But those days are over. Python 3.{3,4,5} are increasingly good,
  and 3.6 is truly excellent.

  I have long supported Python 3 in my modules and with my students, but still often r
  eached for the familiar  2.7 for my own work. No longer. Python 3.6 (released
  December 2016) is now the place to go if you have any choice in the matter. In
  addition to the superior handling of modern Unicode text (which is everywhere in a
  global economy) and other 'standard' features of Python 3, 3.6 adds template strings
  and orders `dict` keys, fixing ugly "Why?! Why does Python not do this yet?!" glitches.
  3.6 is both the Python 3 we need and the Python 3 we deserve.

  I have aliased `python` so it now runs 3.6, and `pip` == `pip3`.  Python 2.6 is the earliest
  release I will support in any way. Both it and even 2.7 are now seen more in the rear-view
  mirror than in daily use.

* CPython, aka the standard, C-based implementation of Python you'd get from
  [python.org](https://www.python.org/) and other source. The Gold Standard
  and generally best place to run Python code.
* [PyPy](https://bitbucket.org/pypy/pypy) - Accelerated JIT implementation of
  Python. Good currency with CPython. I test and certify all my code against PyPy,
  and occasionally use it when CPython isn't fast enough.
* [Jython](https://hg.python.org/jython) - Implementation of Python programming
  language written in Java for the Java virtual machine (JVM). I used to test
  all my libraries against Jython and to be hopeful for a JVM-resident
  Python, but my hopes for it have dimmed over time. Development is slow and the
  versions are back-level vs. standard CPython. It also doesn't easily support
  C-implemented libraries like `lxml` and `numpy` which are essential to much
  of my code. The standard execution environment now seems to be Linux-in-the-cloud,
  not JVM. Time marches on. Still, love it as an old fling.
* Other implementations. I'll believe it when I see it. PyPy and Jython show how
  entirely difficult it is to build and maintain a reall full-Python equivalent.
  Small teams may make magic, but rarely on the scale and with the consistency and
  speed required for core platforms.

## Interactive Interpreter

* [IPython](https://ipython.org/) - A better interactive Python interpreter. Friends don't let friend REPL. Use IPython instead.
* `idle` and `idle3`. If you can't use IPython for interactive work, at least use the interactive IDLE interpreter.
* [Jupyter Notebook (IPython)](https://jupyter.org) - Jupyter Notebook (fka IPython Notebook) is a web-based interactive tool. Write and run code, plus document it in Markdown and Latex math expressions. Also supports other languages, such as JavaScript, Perl.... I spend at least half my development time in Jupyter Notebook.  Enthusiastically recommended.


## Package Management

* `pip` - best way to install modules for Python. You can also use more platform- or
  distribution-specific tools such as `conda` (Anaconda distribution) or a local
  OS installer (e.g. `brew` on macOS, `apt-get` or `yum` on Linux). Avoid
  `easy_install`.

* [wheel](http://pythonwheels.com/) - The new standard of Python distribution
  and are intended to replace eggs. All my packages are built for wheel distribution.


## Specific Formats Processing

* General
    * [openpyxl](https://openpyxl.readthedocs.io/) - A library for reading and writing Excel 2010 xlsx/xlsm/xltx/xltm files.
    * [XlsxWriter](https://xlsxwriter.readthedocs.io) - A Python module for creating Excel .xlsx files.

* Markdown
    * [Python-Markdown](https://github.com/waylan/Python-Markdown) - A Python implementation of John Gruber’s Markdown.
* YAML
    * [PyYAML](http://pyyaml.org/) - YAML implementations for Python.


## Testing

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

* General
    * [chardet](https://github.com/chardet/chardet) - Python 2/3 compatible character encoding detector.
    * [difflib](https://docs.python.org/2/library/difflib.html) - (Python standard library) Helpers for computing deltas.
    * [ftfy](https://github.com/LuminosoInsight/python-ftfy) - Makes Unicode text less broken and more consistent automagically.
    * [fuzzywuzzy](https://github.com/seatgeek/fuzzywuzzy) - Fuzzy String Matching.
    * [Levenshtein](https://github.com/ztane/python-Levenshtein/) - Fast computation of Levenshtein distance and string similarity.

* Slugify
     * [python-slugify](https://github.com/un33k/python-slugify) - A Python slugify library that translates unicode to ASCII.

* Parser

    * [Pygments](http://pygments.org/) - Polyglot syntax highlighter. Seems to support all the languaes.
    * [pyparsing](http://pyparsing.wikispaces.com/) - General purpose framework for generating parsers.

## Third-party APIs

See also: [List of Python API Wrappers and Libraries](https://github.com/realpython/list-of-python-api-wrappers).

* [boto3](https://github.com/boto/boto3) - Python interface to Amazon Web Services.
* [gspread](https://github.com/burnash/gspread) - Google Spreadsheets Python API.

## Web Frameworks

* [Flask](http://flask.pocoo.org/) - A "microframework," which I presume means "simple enough for mere motals." Extraordinarily good combintation of simplicity, logical APIs, performance, extensibility, and community support. Admin dashboards, social logins, and pretty much anything you could want to do in a Python web app, you can do with a Flask server and its add-on modules.
    * [awesome-flask](https://github.com/humiaozuzu/awesome-flask)
* [Django](https://www.djangoproject.com/) - The Big Bog web framework in Python. Opinionated and highly structured. You *will* use very specific MVC components and follow its recommended path. Doubly so if you also operate a REST API or other systematic modules. Deployments can grow intricate to the point of Byzantine. Too many "guts exposed" places to recommend it as a first framework. "Steep" doesn't begin to describe its full-stack learning curve. OTOH, it has a vast number of strong supporting modules, a large development community, and strong outcomes. A backup option should Flask not suit, e.g. for large-scale, highly-internationalized, highly-structured sites. But having run it in production web, I must warn: its complexity comes at a substantive development, testing, optimization, and operational complexity cost. If it were a ski course, its simplest parts would be the intermediate paths; many activities are black diamond and double black diamond rated.
    * [awesome-django](https://github.com/rosarior/awesome-django)

* [Tornado](http://www.tornadoweb.org/en/latest/) - A Web framework and asynchronous networking library. Includes some of the core scheduling features usually implemented by nginx or other web servers. Strong foundation for highly async operations, e.g. WebSockets. Prefer to Twisted.
* Avoid [Bottle](http://bottlepy.org/docs/dev/index.html),
  [CherryPy](http://www.cherrypy.org/),
  [Pyramid](http://www.pylonsproject.org/),
  [TurboGears](http://www.turbogears.org/),
  [Web2py](http://www.web2py.com/), Twisted.
  IMO, time has passed these by. I do not see the energy, community, or speed of
  development in these that I do in Flask, Django, and Tornado.

# Services

Online tools and APIs to simplify development.

* [PyPI](https://pypi.python.org/pypi) - The Python Package Index. Where
  you go to get add-on modules for Python. `pip` installs directly from there.
* [Github](https://github.com) - Leading provider of Git-based source code
  control and related services. The hub of many developers' online development
  identity and experience.
* [Bitbucket](https://bitbucket.org) - Alternative provider of Git and Mercurial (Hg)
  online repositories. I have really loved using Mercurial, and have preferred it to
  Git. But truth be told, Github is outpacing Bitbucket by a very large distance.
  Even Python itself has made the switch to Git and Github.

## Continuous Integration

*See also: [awesome-CIandCD](https://github.com/ciandcd/awesome-ciandcd#online-build-system).*

* [Travis CI](https://travis-ci.org) - Popular CI service. Works well with open source
  projects. (GitHub only). Most of my Python open source projects are Travis CI
  tested. They are a little slow updating the latest versions (esp of PyPy!), but
  generally very solid and rapid.
* [CircleCI](https://circleci.com/) - A CI service that can run very fast parallel
  testing.
