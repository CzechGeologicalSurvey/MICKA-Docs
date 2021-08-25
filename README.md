# MICKA documentation for admin and users.

Source files are written in [reStructuredText](http://docutils.sourceforge.net/rst.html) and built into HTML pages using the [readthedocs](http://www.readthedocs.org) documentation generator automatically.

## Source files
Original documentation was a collection of rst and html files. THe rst files were copied and merged together to the current format in this repository. docx files were converted using pandoc as below:

```
pandoc --extract-media=appendixb -s -t rst http://www.onegeology.org/wmsCookbook/appendixB.html -o appendixb.rst
```

Documentation is published to https://czechgeologicalsurvey.github.io/MICKA-Docs/
