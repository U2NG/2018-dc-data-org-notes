# 01-formatting-data-tables-notes


[From Data Carpentry lesson](https://datacarpentry.org/spreadsheet-ecology-lesson/)

# Introduction 

One of the most common mistakes using spreadsheets is treating them like lab notebooks doing things like:
* replying on context
* notes in margin
* spatial layout of data and fields to convey information 


**This is ok for humans, but computers don't interpret the information in the same way, computers will not be able to interpert how the data fits together.**

we can manage and analyze data in faster more efficient ways but to do that we need to setup the data for the computer to be able to understand it.

* it is important to set up well-formatted tables from the outset before you even start entering data from the first experiement. 
* Data organization is the foundation of your research project 
* DM can make it easier or harder to work with your data throughout your analysis. 
* it's worth thinking DM when you're doing your data entry or setting up your research 


You can setup things in different ways in spreadsheets but some of these chouces can limit working with data in other programs or working the data yourself. 

### Keeping track of your analyses
> **show "notestab" screenshot**

When you’re working with spreadsheets: during data clean up or analyses, it’s very easy to end up with a spreadsheet that looks very different from the one you started with.    

In order to be able to reproduce your analyses or figure out what you did when Reviewer #3 asks for a different analysis, you should:

* create a new file or tab with your cleaned or analyzed data. 
* Don’t modify the original dataset, or you will never know where you started!

* keep track of the steps you took in your clean up or analysis. 
* track these steps as you would any step in an experiment. 
* Save info in another text file, or a good option is to create a new tab in your spreadsheet with your notes. 

Doing this keeps your notes and data together.

Think about these practices as wego through this lesson.

### Structuring data in spreadsheets 

There are some cardinal rules of using spreadsheet programs for data:

1. Put all your variables in columns - the thing you’re measuring, like ‘weight’ or ‘temperature’.
2. Put each observation in its own row.
3. Don’t combine multiple pieces of information in one cell. Sometimes it just seems like one thing, but think if that’s the only way you’ll want to be able to use or sort that data.
4. Leave the raw data raw - don’t change it!
5. Export the cleaned data to a text-based format like CSV (comma-separated values) format. This ensures that anyone can use the data, and is required by most data repositories.

**Example:** 
> **show combined column varialbe image**

For instance, in the image, we have data from a survey of small mammals in a desert ecosystem. 

Different people have gone to the field and entered data into a spreadsheet. 

They keep track of things like species, plot, weight, sex and date collected.

They kept their data like the example:

**Discussion Question:**

```
What is one problem you see with the recorded data in the image?
```

**The problem is the 'species' and 'sex' are in the same field.** 

* If the researchers wanted to look at all of one species or look at different weight distributions by sex, it would be hard to do this using this data setup. 

* If instead sex and species need to be in different columns. 

By doing this, you can see that it would be much easier.  What should be done is:

### Columns for variables and rows for observations

> **show seperated varialbe column image**

A good rule of thumb when setting up a datasheet: 
```
columns = variables, rows = observations, cells = data (values)
```

This is makes data import easier in R and Python. 

### Introduce Portal Project Teaching Dataset used for exercises

The data used in the ecology lessons are observations of a small mammal community in southern Arizona. 

This is part of a project studying the effects of rodents and ants on the plant community that has been running for almost 40 years. 

The rodents are sampled on a series of 24 plots, with different experimental manipulations controlling which rodents are allowed to access which plots.

This is a real dataset that has been used in over 100 publications. 

Data has been simplified for the workshop, but you can download the full dataset and work with it using exactly the same tools we’ll learn about today.

[Full dataset Available on FigShare](http://figshare.com/articles/Portal_Project_Teaching_Database/1314459)


### Exercise 1:
[**Download spreadsheet data**](https://ndownloader.figshare.com/files/2252083)

> **Show Exercise 1 slide Image**

**read exercise instructions**
* half way through show:
> **show list of common mistakes slide**

* Open discussion about messy things that were found.   

### Reminder points:

* Never modify your raw data. Always make a copy before making any changes.

* Keep track of all of the steps you take to clean your data.

* Organize your data according to tidy data principles.
