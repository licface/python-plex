====
Plex
====

Plex is a library building lexical analysers.


Plex is a Python module for constructing lexical analysers, or scanners. Plex
scanners have almost all the capabilities of the scanners generated by GNU Flex,
and are specified in a very similar way. Tokens are defined by regular
expressions, and each token has an associated action, which may be to return a
literal value, or to call an arbitrary function.

Plex is designed to fill a need that is left wanting by the existing Python
regular expression modules. If you've ever tried to use one of them for
implementing a scanner, you will have found that they're not really suited to
the task. You can define a bunch of regular expressions which match your tokens
all right, but you can only match one of them at a time against your input. To
match all of them at once, you have to join them all together into one big r.e.,
but then you've got no easy way to tell which one matched. This is the problem
that Plex is designed to solve.

Another advantage of Plex is that it compiles all of the regular expressions
into a single DFA. Once that's done, the input can be processed in a time
proportional to the number of characters to be scanned, and independent of the
number or complexity of the regular expressions. Python's existing regular
expression matchers do not have this property.


Contact
=======

Original author :

| Greg Ewing <greg@cosc.canterbury.ac.nz>,
| Computer Science Department,
| University of Canterbury,
| Christchurch,
| New Zealand

Maintainer : Stephane Klein <stephane@harobed.org>
