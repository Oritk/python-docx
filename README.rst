.. image:: https://travis-ci.org/python-openxml/python-docx.svg?branch=master
   :target: https://travis-ci.org/python-openxml/python-docx

*python-docx* is a Python library for creating and updating Microsoft Word
(.docx) files.

More information is available in the `python-docx documentation`_.

.. _`python-docx documentation`:
   https://python-docx.readthedocs.org/en/latest/

This fork adds support for font size using complex script.
This is required for runs that need to have both direction instruciton (rtl) and size.
In those cases, adding <w:sz w:val="??"/> to the documentis not enough and we need to add: <w:szCs w:val="??"/>

Usage:
   run = p.add_run(line)
   
   #ru.font.size = Pt(8) This line is redundant - but you can leave it
   
   run.font.cs_size = Pt(8)
   
   run.font.rtl = True
   
