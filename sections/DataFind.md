[<< Previous](DataThink.md) | [Next >>](MessyTidy.md)

# Finding Data

At this point you probably realize that data, or potential data is all around us. While some of us may only ever open and read spreadsheets, we interact with graph data constantly, whether using the library catalog or searching Facebook or using web-based maps. In our own research we are often faced with the task of creating our own datasets from an overwhelming amount of material and this can take significant time and effort. Luckily there are plenty of resources for finding pre-compiled datasets, or "raw" data. We'll look at this soon, but first, let's discuss in more detail what you can expect to find in a data file. 

## What's in a data file?

When we talk about data files we are generally talking about common formats for sharing datasets in which the data is encoded in text characters and written to the file. We are *not* talking about databases, which may very well store data files, but should not be considered their equivilant. As mentioned previously, most datasets that you encounter will come in two forms:

1. **Tabular data** is represented in terms of columns, rows, and cells. Rows represent observations or instances, which have values corresponding to column variables. Tabular data is typically seen in proprietary formats (Excel or GoogleSheets files) or in character delimited text files (CSV - comma separated values - or TSV - tab separated values)

2. **Graph data** is data that can be represented by nodes and edges, roughly speaking. Think of this in terms of [networks that spider out](https://en.wikipedia.org/wiki/Opte_Project#/media/File:Internet_map_1024.jpg). A **directed graph** is data that can be represented by a tree or a hierarchy. This is most commonly seen in XML or JSON formats, although you should note that these formats can also represent tabular data.

## Looking at data files and formats

Navigate to the “External Links” section at the bottom of the [Wikipedia entry for dataset](https://en.wikipedia.org/wiki/Data_set). These links should direct you to several good sources of data, although they are not always "clean" enough to use for a project in their current form. 

**A quick exercise**: choose one of the topics under the "Topics" tab at [Data.gov](https://data.gov/) and spend a few minutes exploring some of the available pages and datasets. Think about some of the following questions and make note of your observations:
- What file formats do the datasets appear in?
- Do you notice differences [geospatial](https://researchguides.library.yorku.ca/c.php?g=679467&p=4793119) and non-geospatial datasets?
- Is there much variety in terms of the sources of governmental data? The decades or years data comes from? Federal data versus state data?

Let's explore an example of a fairly clean dataset from Data.gov: the [Feed Grains Database](https://catalog.data.gov/dataset/feed-grains-database). Note the type of information that this dataset includes, what file formats are avaiable to download, when the dataset was created, and who created it. Before downloading and looking at any of the datasets in detail, take a moment to think about what differences you expect to see between how the data is represented in, for example, a CSV file versus an Excel notebook (based on what you already know about those file formats). 

Let's explore this a little futher: 
- Click on the download link for the .xlsx file and open the file in Excel. 
  - How is the dataset organized? 
  - What values or categories do the rows and columns of the table correspond to?
- Click on the download link for the .csv file. 
  - First open it using a text editor (such as VSCode) and then also open it using Excel. 
  - Is the data organized or stored differently in the .csv (comma separated values) file? 
  - What do you think the benefits might be of the .xlsx dataset versus the .csv dataset?
  - (Is there a default program for reading .csv files on your computer? Open the file with this program and ask yourself the same questions as before.)
- Finally, navigate to the query tool that accompanies this dataset. How does it represent the dataset that you've been exploring in tabular format? How is the information conveyed?

[<< Previous](DataThink.md) | [Next >>](MessyTidy.md)
