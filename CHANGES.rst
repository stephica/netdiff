Changelog
=========

Version 0.4.8 [unreleased]
--------------------------

WIP

Version 0.4.7 [04-01-2016]
--------------------------

- `c79b745 <https://github.com/ninuxorg/netdiff/commit/c79b745>`_: fixed return value of ``_get_primary_address()`` in ``BatmanParser``

Version 0.4.6 [27-12-2015]
--------------------------

- `#36 <https://github.com/ninuxorg/netdiff/issues/36>`_: fixed wrong diff when same nodes but different links

Version 0.4.5 [28-09-2015]
--------------------------

- `#34 <https://github.com/ninuxorg/netdiff/issues/34>`_: show ``local_addresses`` in NetJSON output (``OlsrParser``, ``BatmanParser`` and ``NetJsonParser``)
- `#29 <https://github.com/ninuxorg/netdiff/issues/29>`_: support additional properties in NetJSON output
- `#32 <https://github.com/ninuxorg/netdiff/issues/32>`_: mock telnet requests in tests
- `63a5e8a <https://github.com/ninuxorg/netdiff/commit/63a5e8a>`_: added ``"Unrecognized format"`` message in ``ParserError`` exceptions
- `9ed48a4 <https://github.com/ninuxorg/netdiff/commit/9ed48a4>`_: added arbitrary metric value (average of tx and rx) in ``Bmx6Parser``

Version 0.4.4 [06-09-2015]
--------------------------

- `#31 <https://github.com/ninuxorg/netdiff/issues/31>`_: mocked HTTP requests in tests
- `#29 <https://github.com/ninuxorg/netdiff/issues/28>`_: replaced weight with cost in all NetJSON occurrences

Version 0.4.3 [02-07-2015]
--------------------------

- `#27 <https://github.com/ninuxorg/netdiff/issues/27>`_: added support for txtinfo format to ``BatmanParser``
- `ab9c40 <https://github.com/ninuxorg/netdiff/commit/ab9c40>`_, `9ac89a <https://github.com/ninuxorg/netdiff/commit/9ac89a>`_: minor optimizations and simplifications in ``BatmanParser``
- `990a30 <https://github.com/ninuxorg/netdiff/commit/990a30>`_: minor optimization in ``Bmx6Parser``
- `64f8f44 <https://github.com/ninuxorg/netdiff/commit/64f8f44>`_: the parse() method of each parser now must return a networkx.Graph instance instead of storing it

Version 0.4.2 [27-06-2015]
--------------------------

- `deea34 <https://github.com/ninuxorg/netdiff/commit/deea34>`_: skip links with infinite cost in ``OlsrParser``

Version 0.4.1 [26-06-2015]
--------------------------

- `#13 <https://github.com/ninuxorg/netdiff/issues/13>`_: added support for OLSR 0.6.x txtinfo plugin
- `e94e91 <https://github.com/ninuxorg/netdiff/commit/e94e91>`_: updated default "version" attribute of ``OlsrParser``

Version 0.4 [14-06-2015]
------------------------

- `#21 <https://github.com/ninuxorg/netdiff/issues/21>`_: **breaking change** made ``diff`` output consistent with NetJSON ``NetworkGraph``
- `#24 <https://github.com/ninuxorg/netdiff/issues/24>`_: add "changed" section to ``diff`` to show changes in weight
- `a6a161a <https://github.com/ninuxorg/netdiff/commit/a6a161a>`_: ``diff`` now returns an OrderedDict

Version 0.3.2 [03-06-2015]
--------------------------

- `#26 <https://github.com/ninuxorg/netdiff/issues/26>`_: renamed exceptions with "NetParser" prefix
- `#25 <https://github.com/ninuxorg/netdiff/issues/25>`_: raise Exception if topology file/URL not reachable
- `53e02cc <https://github.com/ninuxorg/netdiff/commit/53e02cc>`_: flagged ``to_python`` of ``BaseParser`` as public
- `48d2927 <https://github.com/ninuxorg/netdiff/commit/48d2927>`_: refactored exceptions, added explaination in README

Version 0.3.1 [22-05-2015]
--------------------------

- `c91e4e <https://github.com/ninuxorg/netdiff/commit/c91e4e48917c6503fc490e725da1574cb5c549fe>`_: corrected weight in ``OlsrParser``
- `#22 <https://github.com/ninuxorg/netdiff/pull/22>`_: added subtraction operator as a shortcut to diff function
- `be9f476 <https://github.com/ninuxorg/netdiff/commit/be9f476>`_: corrected ``MANIFEST.in`` to fix egg builds

Version 0.3 [15-05-2015]
------------------------

- `#18 <https://github.com/ninuxorg/netdiff/pull/18>`_: added CNML parser
- `#17 <https://github.com/ninuxorg/netdiff/pull/17>`_: added BMX6 (b6m tool) parser
- `#16 <https://github.com/ninuxorg/netdiff/pull/16>`_: added ``NetParserJsonException`` which is raised if no JSON object can be decoded in ``_to_python``
- `#14 <https://github.com/ninuxorg/netdiff/pull/14>`_: replaced ``startswith`` string method with ``urlparse`` module for URL scheme recognition

Version 0.2 [08-05-2015]
------------------------

- `#12 <https://github.com/ninuxorg/netdiff/pull/12>`_: Added support for telnet urls in ``BaseParser``

Version 0.1 [02-05-2015]
------------------------

- Added ``OlsrParser``
- Added ``BatmanParser``
- Added ``NetJsonParser``
- Added ``json`` method to ``BaseParser`` which returns valid NetJSON
- Added ``diff`` function
