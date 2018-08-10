# 00-data-org-introduction-notes


[From Data Carpentry lesson](https://datacarpentry.org/spreadsheet-ecology-lesson/)

# Introduction 

* Good organization is the foundation of your research project. 

* Most people have data or conduct data entry in spreadsheets

* The GUI is useful for designing data tables and handling basic quality control functions.

___

### After this lesson, you'll be able to: 
* implement best practices in data table formatting 
* Identify and address common formatting mistakes 
* understand approaches for handling dates in spreadsheets 
* Effectively export data from spreadsheet programs 

and overall good data practices and how to think about data organization and some practices for more effective data wrangling.

---

### What were not going to learn in this lesson:
* how to do statistics
* how to do plotting
* or how to write code 

If you're looking to do this one recommended reference is the "Head First Excel" book pub. by O'Rielly

---

### Why were not teaching data anlysis in spreadsheets

* data analysis in spreadsheets usually requires a lot of manual work
* if there is something that needs to be changed or a new analysis needs to be run with new data, most things need to be redone by hand
* it is also difficult to track or reproduce statistical or plotting analyses done in spreadsheet program when you want to go back to your work
* especially if someone asks for details of your analysis 

### spreadsheet programs 
* many spreadsheet programs are available
* most people use Excel as the primary program 

      Poll: Ask who has Excel installed or other spreadsheet app.
      if there are people with no app. recommend LibreOffice
* For this lesson we will be using Excel examples
* commands may differ between programs, but general idea is the same

#### Quick poll and discussion:  Show slide or copy into hackmd

      Exercise 1:
      Write in ethrepad and briefly discuss:
      1. how many people have used spreadsheets in their research? 
      2. How many people have accidentially done something that 
      made them frustrated or sad?
      
      
      Exercise 2:
      Write in ethrepad and briefly discuss:
      1. what kinds of operations fo you do you do in spreadsheets?
      2. Which ones do you think spreadsheets are good for?


From our exmaples,  we can see spreadsheets encompass a lot of the things researchers need to do:
We can use them for a lot of difference operations:
* data entry
* organizing data
* subsetting and sorting data
* statistics
* plotting

### Problems with Spreadsheets:
* spreadsheets are good for data entry but we tend to use the programs for much more than data entry
* we use the to create a number of things:
    * tables for publications
    * generate summary for stats
    * make plots
    * etc.

* One problem that you may have encountered is generating plots for publications, and this is not optimal
* when formatting a data table for publication, you're reporting key summary statitics in a way that is not really meant to be read as data 
* generating the table often involves special formatting (merging cells, creating borders, making it pretty)
* a good practice and recommendatation for formatting tables is to format tables within the document editing software you're using

* Generating statistics and figures in spreadsheets should be used with caution. 
* The GUI and the ease of dragging and dropping is not reproducilbe.  can you or someone else replicate the steps especially if more complex calculations are involved.
* Calculations in spreadsheets introduce another problem.  it's easy to apply a different formula into another cell or cells. 
* Using R or Python it's practically impossible to apply a calculation to one observation in your dataset but not another unless you do it on purpose. 

### Using spreadsheets for data entry and cleaning 
* There are times when you want to use a spreadsheet to produce quick caluculations and figures.
* data cleaning will help use some of these features.
* data cleaning puts your data in a better format prior to importation into a stats program.
* we'll show you how to use some features of a spreadsheet program to check your data along the way and produce preliminary stats.

* to do this, well take a look at formating data. 

### Lesson outline:
1. formatting data tables in spreadsheets 
2. formatting problems
3. dates as data 
4. quality control 
5. exporting data 

