[<< Previous](ORIntro.md) | [Home >>](../README.md)

# Data Cleaning with OpenRefine

Now that we have created a new project you should see the imported data displayed in a tabular format in OpenRefine - it should look a lot like other tabular tools that you are familiar with, such as Microsoft Excel. 

**A quick exercise**: without using any of OpenRefine's tools, take a quick look at the information in front of you.  How is the data organized? What are the column headers and what sort of information does each column appear to contain? If you expand your view ("Show 100 rows"), do you notice any inconsistenceies or points of strangeness in the data that may need to be addressed?

## Exploring data with OpenRefine

Let's use OpenRefine to explore our data a little further. 

### Sort

Sorting allows you to temporarily sort your rows by one column and is one of the most basic ways of exploring your data. You may already be familiar with this function from your experience with other tools, such as Excel! 

Click on the caret at the top of the **name** column and select `Sort`. You are able to sort by different data types and select where errors and blank cells should appear in the sorting. Drag `Blanks` and `Errors` above `Valid values` and click `Sort`. What do you notice about the data now?

Notice the new `Sort` option that appears in the top bar (next to the "show rows" option) now that you have temporarily sorted the data on the values in the **name** column. Selecting the caret beside the new Sort option gives you the option to permanently apply a new order to the underlying data.

### Filter

Another easy way of exploring your data is with a text filter. From the caret at the top of the **name** column select `Text filter`. This will open a search widget to the left of your data. Note the total number of rows in your dataset. Now try searching for a particular food name in the widget. What changes? How many dishes contain "tomato soup"?

### Facet

Faceting is an important feature of OpenRefine which allows you to look for patterns and trends in your data. It is also the inspriation for OpenRefine's diamond logo! Facets are basically aspects of data variance in a particular column, and faceted browsing lets you look at the "big-picture" of this data and to explore a specific subset of this data in greater detail.

**A quick exercise**: from the caret at the top of the **name** column slect `Facet` and choose `Text facet`. What message does OpenRefine give you about that facet? What do you think the issue is?

**Another quick exercise**: select `Numeric facet` from the facet options in the **times_appeared** column. What do you notice? Why might that be?

## Transforming data with OpenRefine

OpenRefine allows us to automatically fix typos, convert information into the correct format, and to reorder data, among a slew of other useful features. We will review some of the most fundamental methods for cleaning, correcting, and converting data, but you are encouraged to refer to the [OpenRefine documentation](https://docs.openrefine.org/) for additional (and more advanced!) data cleaning methods.

### Editing cells

#### Data types

When we tried to facet the **times_appeared** column OpenRefine reported that no numeric values were present.  This is because the data which appeared to us (as human readers) to be number, was in fact recorded as text values. To facet this information in a way that makes sense, we will need to change the data type for the cells in this column. OpenRefine refers to this process as a **transform**. 

From the caret in the **times_appeared** column, select `Edit cells` and `Common transforms`. This will present you with a number of common options for transforming the contents of the cells in this column. Let's try `To number`. What appears to have changed? Try applying a number facet to this column now. What do you notice?

**A quick exercise**: what common transforms do you think should be applied to the cells in other columns in our dataset? Try applying some of these transforms. What happens? Do these transforms apply uniformely accross each cell in the column? (What about some of the transforms that don't change data types?)

**Hint**: if you think you've screwed something up with your data, navigate to the `Undo/Redo` tab to the left of your tabular data. This will allow you to backtrack to an earlier stage in your exploration and cleaning!

#### Dealing with whitespace

Let's redirect our attention to some of our textual data in the **name** column. One common aspect of textual data entry that can cause issues further on down the road are invisible characters, such as spaces, tabs, and carriage returns. Let's trim these annoying invisible characters. 

From the caret in the **name** column navigate to `Common transforms` and select `Trim leading and trailing whitespace`. Now select `Collapse consecutive whitespace` from the `Common transforms` option for this same column. What do you think this step achieved?

#### Clustering

As you explored the dataset you may have noticed that certain dish names that likely referred to the same type of food, but were notated differently. Think of all the different ways that someone might make a record of "two poached eggs on toast"! A common transform called **clustering** will help us to standardize this information. 

Clustering uses different machine comparison methods to locate text entries that are similar but not exact, then shares those results with you so that you can merge the cells that should match. Clustering is quick and streamlined in comparison to editing one cell at a time. 

From the caret in the **name** column, navigate to `Edit cells` and select `Cluster and edit...`. OpenRefine it will suggest values it thinks are variations on the same thing, and you can choose which, of any, versions to keep and apply across all the matching cells by selecting any relevant suggestions. Note that `Select All` and `Unselect All` options are available at the bottom of the suggestion pane. 

Browse through some of the suggestions provided by OpenRefine. What do you notice? Once you are finished, make some selections and click on `Merge selected and re-cluster`. You can repeat this same process as many times as you want. When you are ready to move on, simply close the window.

#### Editing with GREL

GREL, or General Refine Expression Language, allows us to use shorthand code called **regular expressions** to match classes and strings of characters. We will use some simple GREL to clean up the contents of the **first_appeared** and **last_appeared** columns. Notice how when we changed the data-type to "date" in this column, more information appeared than we may have needed. Let's modify this information to display only the year (but without chaning the data-type!).

From the caret in the **first_appeared** column, select `Edit cells` and `Transform`. Make sure that GREL is selected from the drop-down menu in the new pane. In the expression window type `value.datePart("year")` and notice what happens to each value in the preview. Click `ok` to apply your changes.

GREL is a great tool for mass editing data in OpenRefine! You should refer to the [GREL Reference](https://docs.openrefine.org/manual/grelfunctions) in the OpenRefine documentation for further guidence. 

### Editing columns

OpenRefine also allows you to edit columns. Some common column operations are **splitting** - for example, if you need to create seperate columns for first and last name from one general "name" column - **joining** - if there are several columns for catetory-type values that you need combine into a single "category" column - and **adding a column based on another column**.  Let's apply this third opperation to our data set to create a new column for "date-range".

From the caret in the **last_appeared** column, click on `Edit column` and select `Add column based on this column...`. In the window that opens, name this new column "date-range" (or something similar). Make sure that GREL is selected from the drop down menu and type the following into the expression box: `cells["first_appeared"].value + "-" + cells["last_appeared"].value`. Why do you think `"-"` is included in the expression?

## Practice with OpenRefine

Using the tools introduced so far, spend some time further cleaning and refining your dataset. Some things you might consider (but only if they make sense!):
- remove non-alpha characters from the contents in the **name** column
- rename columns to be more precise
- remove or collapse irrelevant columns
- remove all entries that contain a null or empty entry for some variable

Make liberal use of the faceting tools to explore and identify patterns (and problems!) in your data. It is also possible to **star** or **flag** a subset of entries identified in a facet for mass editing!

If you're not sure about a particular operation, refer to the [OpenRefine documentation](https://docs.openrefine.org/). 

When you have finished cleaning our dataset(s) you should export a copy of it. Click on `Export` in the upper right-hand corner and select the file format of your choice.  If you don't want to export the full dataset, click on `Custom tabular explorer...`.  With the custom tabular explorer you have the option to select which data to export (and in what order) as well as a choice of file formats (among other things). 

Once you have exported your cleaned dataset, don't forget to open it in a text editor like VSCode or in Excel to ensure that everything has transferred properly.

[<< Previous](ORIntro.md) | [Home >>](../README.md)
