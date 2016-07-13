# Command Files

This folder should contain one or more do-files (with the `.do` 
extension) that contain commands that execute every step of data 
processing and analysis required to reproduce the results you report in 
your paper.

In all of the do-files you write, it is important to include comments 
that are detailed and clear enough to make it possible for someone not 
familiar with your project to understand the steps of data processing 
and analysis that are executed by the commands in the do-file.

For the purpose of constructing and organizing your do-files, you should 
think of the work on your project in terms of three phases, which we 
will call (1) importing, (2) processing, and (3) analysis. Your do-files 
will include one or more files that execute each of these phases of 
research.

1.  For the importing phase, the do-file(s) should contain commands for 
Stata to read the data in each of your importable data files, and then 
save them in .dta format. For example, if you have an importable data file 
in `.csv` format, your command file(s) will include a command like `insheet` 
or `infix` that imports the data, and a save command that saves the data 
in a `.dta`-formatted file. (If an importable data file is already
in `.dta` format, nothing needs to be done to it during the importing phase.) <br><br> 
At the end of the importing phase, you will have a set of data files, all 
in Stata’s `.dta` format, containing all the data for your project. These 
data files will serve as inputs to the processing phase described below. <br><br>
When you have completed your paper, these files should not be included 
in the final documentation. Anyone interested in these files can create 
them simply by executing the do-files you wrote for the importing phase 
of your project.

1. The do-file(s) for the processing phase should include commands that 
execute all the processing required to transform the .dta-formatted versions 
of your data into the final data file(s) that you will use in your analysis. 
Exactly what these steps will be is highly variable, but they typically 
include operations such as joining two or more data files, dropping variables 
or cases, generating new variables, recoding and cleaning. At the end of 
the do-files for the processing phase, there should be save commands that 
save (in .dta format) the final data file(s) upon which your analysis will 
be conducted. We will refer to the final data files(s) that you use in your 
analysis as your “analysis data file(s).” <br><br>
If you have a single analysis data file - i.e, if all of your analysis 
will be performed using a single data file created during the 
processing phase - it should be saved with the name `analysis.dta`. 
If you have more than one analysis data file, give them informative 
names, such as `analysis_euro.dta`, `analysis_afri.dta`, and 
`analysis_asia.dta`; or `analysis_individual.dta` and 
`analysis_household.dta`. <br><br>
Your analysis data file(s) should be stored in your `analysis-data` 
folder. <br><br>
Strictly speaking, including your analysis data file(s) in the 
documentation is redundant:  anyone interested in your analysis data 
file(s) files can create them simply by executing the do-files you 
wrote for the importing and processing phases of your project. 
Nonetheless, the TIER Protocol calls for your analysis data file(s) to 
be included simply because it is sometimes convenient to have a readily 
accessible copy of the analysis data.

1. The do-file(s) for the analysis phase should contain commands that 
open the analysis data file(s) you created in the processing phase, and 
then generate the results reported in your paper. <br><br>
Every command in your analysis do-file(s) that generates a piece of 
output or a result reported in your paper should be preceded by a 
comment that indicates what piece of output or result the command will 
generate.The following examples illustrate some typical kinds of 
comments:

    `* The following command produces Table 6.`

    `* The following command produces Figure 12.`
    
    `* The following command calculates the correlation of -0.54` <br>
    `* between variables X and Y reported on page 16 of the paper.`

All of the do-files for importing, processing and analyzing your data 
should be included in the `command-files` folder. 

One additional do-file, called `data_appendix.do`, should also be 
included in your `command-files` folder. This do-file is described in 
the instructions for your Data Appendix.