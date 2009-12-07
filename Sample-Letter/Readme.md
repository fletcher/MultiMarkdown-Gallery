Title: Sample Letterhead and Envelope Style for MultiMarkdown

# Requirements #

* MultiMarkdown 2.0.b5 or later, specifically:
	* custom-letterhead.xslt
	* letterhead.xslt
	* custom-envelope.xslt
	* envelope.xslt

* install the following in `~/Library/texmf/tex/latex`:
	* `mmd-letterhead` folder
	* `fletcherpenney` folder

* You may need to run `mktexlsr` within your texmf folder to update the
  database.

The idea is that you would then modify the `custom-letterhead.xslt` file to
use your own LaTeX style file and signature, rather than mine.

`signature.pdf` is simply a pdf containing a scanned signature, converted to vector format.  See [Digitize][] for more information on this.

# Using this Setup #

Insert the appropriate metadata for `Author`, etc, and select the
`custom-letterhead` XSLT file. Convert to LaTeX (or in my case, XeLaTeX due to
the customized fonts), and process using `pdflatex` or `xelatex`. Examine the
`sample.txt` file for more information.

You can then change to the `custom-envelope` XSLT and repeat in order to
generate the envelope. I suppose if you did this a lot, you might even create
a macro to process both stylesheets for you automatically.


[Digitize]: http://fletcherpenney.net/2009/10/digitize_your_signature
