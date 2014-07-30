blastConverters
===============

This script is for convert file in a standard blast output format (NCBI-like) to a xml formatted. Script is able to convert blast files with >10.000 query records from more then 20 subjects (we tried it on up to 60.000, but theoretically there is no limit). 

 Blast2GO and many other applications are using BLAST results as a starting point to their analysis, and in many cases this applications accept results only in specific format. BLAST search itself is a time consuming procedure, specially for the genome-wide analysis, usually people run such a search only once. Another limitation appear from the hardware/software side; for example blast machine can produce only two types of output either in tabular or in NCBI formats.

The output of this script was tested as an input to the Blast2Go via local b2gPipev2.5 and online java application.


-------------------
Usage
-------------------

perl bigBlast2XML.pl -blast <input.file.name> -out <output.prefix>
<br><br>
&nbsp;Usage:   bigBlast2XML.pl [options]
<br>
&nbsp;Options<br>
&nbsp;&nbsp;&nbsp;&nbsp;<b> blastFile|blast</b>  input BLAST file in NCBI format [Mandatory]<br>
&nbsp;&nbsp;&nbsp;&nbsp;<b>numberSeqs|n</b>  number of sequence in the output file. Sometimes input file is huge and for parallelization purpose user wants to divide it into chunks.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; By default it 1,000,000 seqs per file.<br>
&nbsp;&nbsp;&nbsp;&nbsp; <b>outputPrefix|out</b> prefix for output files. Output file names will be constructed like prefix+number+.xml<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;By default it is 'convertedBlast'<br>




