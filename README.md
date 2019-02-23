# scielobr_xmltopdf
ScieloBR XML to PDF

This can be seen on https://test.patafisica.cc/scielo/article.class.php.

A PHP implementation of Scielo's brazilian XML standard (http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/) using simplexml and fpdf to output pdfs. The general purpose of this project is generate pdf files from XML, so that there's no need (or at least there's a minimal need) to check manually the output files for whole issues or individual articles. This is being thought as an independent server application, although it wouldn't be any difficult to implement it as an OJS plugin so that the pdf generation would happen as a new issue (with marked XML files through Scielo Brazil's tool, Markup) is published.

Unfortunately I'll have to use PHP's "OO" to implement this sice it'd be easier to implement fpdf to it and organize; i'm simply translating Scielo schema into PHP to be able to handle those files; an issue i found is that many indexed journals do not follow scielo's standards, so that's a deal breaker, but i'll do it following the documentation and see where it leads me; organizing the article in a class will give me the ability to change how the file is parsed (ie different tags) so i wouldn't be the only person capable of using it without reading the whole specs.

I'm thinking about using JSON for the internal use of data, but i'm still not sure.

# Technical details
You can see there are two different XML files: one is a XML i got from a random journal indexed by Scielo, and the other (artigo2.xml) is taken directly from Scielo publish schema's examples. It's not hard to see both files are different and still indexable either way :p standards such as these suck.
