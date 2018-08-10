# 03-data-org-dates-notes

## Dates as Data
Let's talk about dates and date formatting in spreadsheets:

Dates in spreadsheets are stored in a single column.

While this seems the most natural way to record dates, it actually is not best practice.

A spreadsheet application will display the dates in a seemingly correct way (to a human observer) but how it actually handles and stores the dates may be problematic.

In particular, please remember that functions that are valid for a given spreadsheet program (be it LibreOffice, Microsoft Excel, OpenOffice, Gnumeric, etc.) are usually guaranteed to be compatible only within the same family of products.

If you will later need to export the data and need to conserve the timestamps, you are better off handling them using one of the solutions discussed below.

Additionally, Excel can turn things that aren’t dates into dates.

For example names or identifiers like ``MAR1, DEC1, OCT4``. So if you’re avoiding the date format overall, it’s easier to identify these issues.

[Gene name error:  Bad date example](https://nsaunders.wordpress.com/2012/10/22/gene-name-errors-and-excel-lessons-not-learned/)

---

### Exercise 2:
[**Download spreadsheet data here if needed**](https://ndownloader.figshare.com/files/2252083)

> **Show Exercise 2 slide Image**
> Challenge: pulling month, day and year out of dates

**read exercise instructions**

> **show and explain plot 3 with new MDY columns**

---

### Exercise 3:
add columns to cleaned spreadsheet tab

> **Show Exercise 2 slide Image**
> Challenge: pulling hour, minute and second out of the current time

**read exercise instructions**

> **show and explain time eextractions**
>


### Preferred date format
It is much safer to store dates with ``YEAR, MONTH, DAY`` in separate columns or as ``YEAR and DAY-OF-YEAR`` in separate columns.

***Excel Note:***
***Excel is unable to parse dates from before ``1899-12-31``, and will thus leave these untouched.
If you’re mixing historic data from before and after this date, Excel will translate only the post-1900 dates into its internal format, thus resulting in mixed data.
If you’re working with historic data, be extremely careful with your dates!***

***Excel's second date system:
Excel also entertains a second date system, the 1904 date system, as the default in Excel for Macintosh. This system will assign a different serial number than the 1900 date system. Because of this, dates must be checked for accuracy when exporting data from Excel (look for dates that are ~4 years off).***

### Data formats in spreadsheets

Spreadsheet programs have numerous “useful features” which allow them to handle dates in a variety of ways.

> **Show date examples screencap**

* keep in mind, these spreadsheet “features” often allow ambiguity to creep into your data.
* Ideally, data should be as unambiguous as possible.

### Dates stored as integers

* The first thing you need to know is that Excel stores dates as numbers - see the last column in the above figure.

* Essentially, it counts the days from a default of ``December 31, 1899``, and thus stores ``July 2, 2014 as the serial number 41822``.

(But wait. That’s the default on my version of Excel. We’ll get into how this can introduce problems down the line later in this lesson. )

* This serial number thing can actually be useful in some circumstances.
* By using the above functions we can easily add days, months or years to a given date.
* Say you had a sampling plan where you needed to sample every thirty seven days.
* In another cell, you could type the formula:

**goto excel date tab and demonstrate:**
```
=B2+37
```
and it would return
```
8-Aug  #or 37 days added to orig date
```

* Excel understands the date as a number ``41822``, and ``41822 + 37 = 41859`` which it interprets as ``August 8, 2014``.
* It retains the format (for the most part) of the cell that is being operated upon, (unless you did some sort of formatting to the cell before, and then all bets are off).
* Month and year rollovers are internally tracked and applied.

***Note:***
*Adding ``years and months and days`` is slightly trickier because we need to make sure that we are adding the amount to the correct entity.*

To do that:
* First we extract the single entities (day, month or year)
* We can then add values to to that
* Finally the complete date string is reconstructed using the ``DATE()`` function.

As for dates, times are handled in a similar way
* ``seconds`` can be directly added
* but to add ``hour and minutes`` we need to make sure that we are adding the quantities to the correct entities.

Which brings us to the many different ways Excel provides in how it displays dates.

If you refer to the figure (date-formats)
* you’ll see that there are many ways that ambiguity creeps into your data depending on the format you chose when you enter your data
* if you’re not fully aware of which format you’re using, you can end up actually entering your data in a way that Excel will badly misinterpret.

---
### Exercise 4:
Saving dates tab as CSV format and reopening in texte ditor.

> **explain steps - ask to do**

**read exercise instructions**
**walk through steps**

> **show solution/outcome**

***Note:***
**You will notice that when exporting into a text-based format (such as CSV), Excel will export its internal date integer instead of a useful value (that is, the dates will be represented as integer numbers).
This can potentially lead to problems if you use other software to manipulate the file.**

### Advantages of Alternative Date Formatting

### Storing dates as YEAR, MONTH, DAY

Storing dates in YEAR, MONTH, DAY format helps remove this ambiguity. Let’s look at this issue a bit closer.

For instance this is a spreadsheet representing insect counts that were taken every few days over the summer, and things went something like this:

> **show screencap insect counts**
>

If Excel was to be believed, this person had been collecting bugs in the future.

Now, we have no doubt this person is highly capable, but I believe time travel was beyond even their grasp.

* Entering dates in one cell is helpful but due to the fact that the spreadsheet programs may interpret and save the data in different ways (doing that somewhat behind the scenes), there is a better practice.

* In dealing with dates in spreadsheets, separate date data into separate fields ``(day, month, year)``, which will eliminate any chance of ambiguity.


### Storing dates as YEAR, DAY-OF-YEAR

There is also another option.
* You can also store dates as year and day of year (DOY). Why? Because depending on your question, this might be what’s useful to you, and there is practically no possibility for ambiguity creeping in.

* Statistical models often incorporate year as a factor, or a categorical variable, rather than a numeric variable, to account for year-to-year variation, and DOY can be used to measure the passage of time within a year.

* Can you convert all your dates into DOY format?

In Excel, here’s a useful guide:

> **show screencap DOY**
>


### Storing dates as a single string

* Another alternative could be to convert the date string into a single string using the ``YYYYMMDDhhmmss`` format.

For example the date ``March 24, 2015 17:25:35`` would become ``20150324172535``, where:

YYYY: the full year, i.e. 2015
MM: the month, i.e. 03
DD: the day of month, i.e. 24
hh: hour of day, i.e. 17
mm: minutes, i.e. 25
ss: seconds, i.e. 35

Such strings will be correctly sorted in ascending or descending order, and by knowing the format they can then be correctly processed by the receiving software.

#### Key Lesson points:
* Treating dates as multiple pieces of data rather than one makes them easier to handle.
