blastConverters
===============

Blast2GO and many other applications use BLAST results as a starting point of the analysis process, and often these applications accept results only in specific format. BLAST itself is a time consuming procedure, especially in case of genome-wide analysis - and usually people run such a search only once. Another limitation appear from the hardware/software side - for example, blast machine can produce only two types of output: in tabular or in NCBI format.



bigBlast2XML.pl
----------------------

This is the script to convert the file from the standard blast output format (NCBI-like) to the xml. Script is able to convert blast files with >10.000 query records (it was tested on ~60.000 queries, but theoretically there is no limit).
<br>
The xml-output of this script was tested as an input for Blast2Go via local b2gPipev2.5 and online java application.
<hr>
<b>Usage</b>

perl bigBlast2XML.pl -blast input.file.name -out output.prefix
<br><br>
&nbsp;Usage:   bigBlast2XML.pl [options]
<br>
&nbsp;Options<br>
&nbsp;&nbsp;&nbsp;&nbsp;<b> blastFile|blast</b>  input BLAST file in NCBI format [Mandatory]<br>
&nbsp;&nbsp;&nbsp;&nbsp;<b>numberSeqs|n</b>  number of sequence in the output file. Sometimes input file is huge and for parallelization purpose user wants to divide it into chunks.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; By default it 1,000,000 seqs per file.<br>
&nbsp;&nbsp;&nbsp;&nbsp; <b>outputPrefix|out</b> prefix for output files. Output file names will be constructed like prefix+number+.xml<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;By default it is 'convertedBlast'<br>




