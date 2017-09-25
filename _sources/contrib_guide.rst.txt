Contribution guide
==================

This module is intended to be more than just one persons work.

The source code is hosted in gitlab, click on the scary wolf to icon to get there.
Please raise issues in the issue tracker, including improvement wishes. If you
get a 404 email me your gitlab username and you'll be added to the team.

.. image:: .static/GitLab1600.png
	:scale: 10%
	:target: https://gitlab.com/rmenk/flexibility


The aim of this module is to analyse flexibility assets.
The initial focusses on the economic analysis of AMP, but more will follow.
If you find that you are doing a certain calculation more often or would like to
be able to do it on a few different assets, it should probably be added to this
module.

Guidelines
----------
Here are some guidelines. They are guidelines not rules.

Style
.....
* Favour descriptive variable names over line length limitations
* Note units as comments in source code
* Pay attention to MWh and MWh per half hour
* Classes do one specific thing. Split the module if it gets too big.
* Try to document the work, see below.


Documentation first!
....................
The aim is to follow a documentation fist principle, where functions and
classes are documented with rudimentary doc strings before implementation.
Once successfully implemented the documentation should be fleshed out,
best with *working* examples! Try and follow Google's python docstring guide.

Git
...
The `master` branch must always work. Only commit tested code to the master branch.
There is not particular versioning system in place yet. How you call the development
branch or branches is up to you, but please keep it sensible. 

Tests
.....
There should be tests. So far there aren't any. This needs fixing. If you'd like
to contribute tests, I'll provide cake.
