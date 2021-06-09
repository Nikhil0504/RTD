.. RTD_Demo documentation master file, created by
   sphinx-quickstart on Wed Jun  9 11:38:18 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

==================
Documentation Demo
==================

This is a read-the-docs file which uses .rst and python to create documentation.

You can checkout the the configuration in ``docs/source/conf.py`` in the GitHub repo.

There is no particular theme and pages yet as this is just a Proof-Of-Concept.


Things you can do with RTD
==========================

Paragraphs
^^^^^^^^^^
Restructured text. A paragraph is the most basic building block with a reST document. Paragraphs are separated by a blank line.

This is paragraph 1

This is paragraph 2

This is paragraph 3.
   This is not a paragraph as no is no blank line between these two lines.

.. note ::
   You can also have indentations just by tabbing.


Inline markup
-------------

The standard reST inline markup is quite simple: use
::

   one asterisk: *text* for emphasis (italics),
   two asterisks: **text** for strong emphasis (boldface), and
   backquotes: ``text`` for code samples.

for the blocks :ref:`"see"<#_literalBlock>`.

This is **bold**.

This is *italics*.

This is ``code samples``.

If you need to code \*this is not bold\* in your text you will to escape the asterisks with a \\ to avoid the conversion to italics.


Lists and Quote-like blocks
---------------------------
* This is a bulleted list.
* It has two items, the second
  item uses two lines.

1. This is a numbered list.
2. It has two items too.

you can also have nested lists like this:

* this is
* a list
   * with a nested list
   * and some subitems
* and here the parent list continues


.. _#_literalBlock:

Literal block (::)
------------------

Literal code blocks are introduced by ending a paragraph with the special 
marker ::. The literal block must be indented (and, like all paragraphs, 
separated from the surrounding ones by blank lines):

The handling of the ``::`` marker is smart:

* If it occurs as a paragraph of its own, that paragraph is completely left out of the document.
* If it is preceded by whitespace, the marker is removed.
* If it is preceded by non-whitespace, the marker is replaced by a single colon.

there is more stuff here https://sphinx-rtd-theme.readthedocs.io/en/stable/demo/demo.html#code-blocks


Our Usage
=========

We can create pseudo code and code blocks and have some custom stuff in the backend to make it better.

We can create code-blocks like this and also hightlight and do a lot more.


.. code-block:: python
   :linenos:
   :emphasize-lines: 3,5

   def some_function():
       interesting = False
       print 'This line is highlighted.'
       print 'This one is not...'
       print '...but this one is.'



=======
Example
=======
Now we will create a program for generating Fibonacci numbers

This is the equation for the Fibonacci Sequence:


.. math::
   
   F_n = F_{n-1} + F_{n-2}

In mathematical terms, the sequence Fn of Fibonacci numbers is defined by the recurrence relation with
a few defined values given below:


.. math::
   
   F_0 = 0 \\
   F_1 = 1

Here's the pseudo code for implementing this algorithm

.. code-block:: rst

   Step 1: Start 
   Step 2: Declare variable a, b, c, n, i
   Step 3: Initialize variable a=0, b=1 and  i=2 
   Step 4: Read n from user 
   Step 5: Print a and b 
   Step 6: Repeat until i<=n : 
      Step 6.1: c=a+b 
      Step 6.2: print c 
      Step 6.3: a=b, b=c 
      Step 6.4: i=i+1 
   Step 7: Stop