[<< Previous](MessyTidy.md) | [Next >>](DataClean.md)

# Introduction to OpenRefine

Formerly Google Refine, OpenRefine is a relatively user-friendly tool for processing and cleaning large amounts of messy data. While it is by no means the only or best way to work with data, OpenRefine inhabits a middle ground between proprietary tools intended for a broad audienceand the programming systems used in data science. Some of the advantages of using OpenRefine over other methods for cleaning data, such as Microsoft Excel or programming languages like R or Python, include that it is free and open-source, it is fairly easy to learn, and it can batch fix problems in the data (i.e. change many fields at once) more quickly than manually cleaning the data in a program like Excel.

**A quick activity**: Look over the [OpenRefine website](https://openrefine.org/) to get a sense of what this software is and who is maintaining it. Watch some of the videos on the landing page to get a sense of what OpenRefine looks like and how it can be used. You should also notice pages on how to download OpenRefine, on the history of the tool (important for understanding its transition from proprietary software owned by Google to free, open-source software supported by the user community), a FAQ page, etc.

## Install OpenRefine

Once you have a better sense of what OpenRefine is as a tool and what resources are available to you, navigate to the [download page](https://openrefine.org/download.html) on the OpenRefine website and install the latest stable version of the software. You may find it helpful to refer to the [installation instructions](https://docs.openrefine.org/manual/installing) in the OpenRefine documentation. 

OpenRefine works on all platforms (Windows, Mac, and Linux). Even though OpenRefine is a software package, it was originally written for the web, so it will open in your browser. It works best on browsers based on Webkit (Google Chrome, Chromium, Opera, Microsoft Edge), so take care that you open the program such a browser if it isn't the default on your computer. 

## Creating a Project

For our project we will be using data from historical restaurant menus transcribed by the New York Public Library. Download the [latest CSV data export](http://menus.nypl.org/data) and save the file contents to a projects folder on your computer. 

Launch OpenRefine - if a command line window opens on launch, you can ignore it. A homescreen with a few basic menu options should open in your browser. Toggle into `Create Project`, get data from `This Computer` and select `Dish.csv` from the data files which you just saved.

Once you've selected your file, add a project name in the top bar and select `Create Project`. You may also choose from an array of options regarding how to parse that data - we will stick with the presets. Note that you can import both tabular data like CSV's or Excel files as well as nested formats, like JSON or XML.

[<< Previous](MessyTidy.md) | [Next >>](DataClean.md)
