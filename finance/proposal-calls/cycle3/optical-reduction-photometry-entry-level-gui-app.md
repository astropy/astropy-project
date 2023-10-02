### Title

Develop a Jupyter widget-based app for reducing and performing stellar photometry on optical images

### Project Team

Matt Craig would lead. There would potentially be additional outside hires or money for hiring students.

### Project Description

This would be an astropy-based project to provide an essential function in undergraduate-level astronomy: a tool for calibrating images, doing stellar photometry, and providing some basic tools for looking at the results of that photometry.

While astropy already provides a mechanism for scripting those activities, it is painful to have to write code every time. It can be done in a way that novices can use it (see the [photometry notebooks here](https://github.com/mwcraig/ast266-notes/tree/main/notebook-templates) for an example), but is cumbersome.

Doing something simple like generating a time series requires substantial boilerplate code. While tedious for someone experienced, that boilerplate is intimidating to new comers.

The community this potentially impacts are amateur astronomers, those teaching astronomy in high school or at the undergraduate level, and potentially those running REU programs.

### Project / Work

To be clean, none of the ideas here are really new. For example, [LEMON](https://github.com/vterron/lemon), presented at the first PyAstro conference, did some of these things without a GUI. It has not had a release in 5 years, though.

Some of the features listed below have rough implementations in [stellarphot](https://github.com/feder-observatory/stellarphot) (note that the state of that code/documentation indicates the need for some dedicated funding for work on this).

+ Finalize a fast implementation of an image widget, work begun in the [astrowidgets](https://github.com/astropy/astrowidgets) package.
+ Design/layout an ipywidgets-based app for
    - image display, generating PSF/seeing profiles
    - identifying stars to photomer
    - running the photometry to get (at least) instrumental aperture magnitudes.
    - Offer several ways to process those magnitudes
    - Offer straightforward time series plotting, leveraging wigdet-based plotting to provide, e.g. cutouts of a star when you hover over a data point in the time series.
+ Include output routines for reporting data to TESS and EXOTIC (exoplanets), and the AAVSO (variable stars).
+ Define a framework to make the tools extensible, i.e. able to plug in new analysis tools.
+ Work throughout to make sure the tools are interoperable with other tools (e.g. Users of AstroImageJ should be able to feed their photometry files into this to do variable star photometry).


### Approximate Budget

Currency: US $40,000

This is a really rough ballbark estimate, all salary/contractor.

### Approved budget

$32,000.

### Extended budget

The Finance Committee approved an extension, resulting in a total budget of $58,723.
