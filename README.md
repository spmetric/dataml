DataML
======

Having some generic way to describe scientific data files is a common problem.
Many domain-specific meta-data standards exist, but I don't know of any models
that are broadly applicable and also interface well to generic data management
APIs and web services.

This work is the start of such a generic description, with the initial goal of
providing a simple abstract model of standard name/value pairs that can be used
to describe a range of file formats: flat text files, XML, binary, etc.

Example
-------

The following is an example for a tab-delimited text file with the meta-data
provided in HTTP-Header format, and the "schema" described using pseudo-numpy
syntax.

    :::css
    data-delimiter: \t
    data-format:    (S4)mtz, (S6)scop, (S12)result, (i4)start, (i2)runtime, (u1)exitcode, (f4)rfz, (f4)tfz, (u1)pak, (i2)llginitial, (i2)llg
    data-entries:   14243
    data-creation:  2010-06-01
    data-owner:     "Ian Stokes-Rees" <ijstokes@hkl.hms.harvard.edu>
    data-home:      glidein.nebiogrid.org:/home/ijstokes/public_html/phaser/clean/3cdx/results

Alternative Standard Data Formats
-------
    JSON
    XML
    NetCDF
    YAML
    http://code.google.com/p/ssdf/
