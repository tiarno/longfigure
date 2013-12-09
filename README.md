longfigure
==========

LaTeX package using longtable internal code to support long figures that can break across pages.

The `longfigure` package differs slightly from the well-known `longtable` package
written by David Carlisle. The `longtable` package defines a `longtable` environment,
which produces tables that can be broken by TeX's standard page-breaking algorithm.
Similarly the `longfigure` package defines a `longfigure` environment which produces
figures that can be broken by TeX's standard page-breaking algorithm.

The `longfigure` package differs from the `longtable` package in the following ways:

* The counters and macros that start with `\LT`  are renamed to start with `\LF` to avoid
  namespace conflicts when the two packages are used together.
  Note: The generic macros defined in the `longtable` package
  (`\endfirsthead`, `\endhead`, `\endfoot`, `\endlastfoot`) are
  also renamed with `\LF` as a prefix.

* The `longfigure` package supports two additional key-value options:

    * `figname=` specifies the counter for numbering `longfigure` environments.
      The default is `figure`, but you can specify any string. 
      If the counter is not already defined, it is created.
     
    * `resetby=` specifies a counter (for example, `resetby=chapter`) such
      that output numbering is reset with each change in the counter value.
      Refer to the `tocloft` package documentation for information about how the
      lists are typeset.
      
  If a counter is specified that does not exist, the `tocloft` package is
  loaded to create the new counter.

  You can produce a *List of Figures* using the package defaults
  by inserting the following tag in your document at the point where you would like
  the list to appear:
  
    \listoffigures

    
