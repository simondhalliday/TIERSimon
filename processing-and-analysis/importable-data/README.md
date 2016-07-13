# Importable Data

For each of the original data files in your `original-data` folder, 
you should create a corresponding version that we will call an 
"importable data file." These importable data files should be stored in 
the `importable-data` folder.

In some cases, the importable data file will be a slightly modified 
version of the original. In other cases the importable version will be 
identical to the original. 

Whether or not an importable data file differs from the original 
version will depend on whether the original version is in a format that 
R can open or import.

There are two cases to consider:

(1) The original data file is in a format that R can open or import.

This case obviously applies if the original data file is in Stata’s 
`.dta` format. Files in `.dta` format can be opened with Stata’s `use` 
command. 

There are some file formats that Stata’s use command cannot open, but 
that can be imported to Stata with other commands. Common examples of 
this type are comma separated values (.csv) and other delimited text 
formats, as well as Excel workbooks. Stata’s `insheet` command can be 
used to import data from a file in .csv format, and the `import excel` 
command can be used to import data from an Excel workbook. 

When an original data file is in Stata’s `.dta` format, or another format 
that can be imported into Stata without any modification, the corresponding 
importable data file should be an exact copy of the original. In these 
cases, the copy of the file in the “Importable Data” folder should have 
the same name as the copy in the “Original Data” folder. 

Note, however, that in some cases, even when an original data file is 
in .csv or Excel format, it may be convenient or necessary to modify 
it slightly before using Stata to import the data it contains. Three 
examples of cases in which this is true are given below under item (ii).

(2) The original data file must be modified before it can be imported into Stata.

In some situations, it can be necessary or convenient to modify an 
original data file before importing it to Stata. The following examples 
illustrate a few of the common cases:

- If the original data file is a spreadsheet that contains explanatory 
notes as well as data, it may be necessary or convenient to remove those 
notes from the importable version of the spreadsheet.

- If a certain variable is measured in dollars, and a dollar sign ($) 
precedes each value of the variable in the original .csv or Excel data 
file, you may wish to remove the dollar signs so that Stata recognizes 
that the variable should be stored in a numeric format.

- If an original data file is formatted for use with a particular type 
of software other than Stata (e.g., SPSS, SAS, R or Matlab), it may be 
necessary to convert the file from its original format to Stata’s .dta 
format using a package like [Stat/Transfer](https://www.stattransfer.com/).

As these examples illustrate, the particular ways in which an original 
data file needs to be modified will vary depending on the nature of the 
original data file. But in every case, the modifications made to an original 
data file to create the importable version should follow this general principle:

**The importable data file should be as nearly identical as possible to the original;
no changes should be made to the file other than the minimal modifications
required to allow Stata to read the data it contains.**

The changes you make to your original data files to create the corresponding 
importable data files should be described in your ReadMe file.

When an importable data file is a modified version of the corresponding 
original data file, the original and importable versions should be given 
different names.