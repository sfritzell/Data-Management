[<< Previous](DataFind.md) | [Next >>](ORIntro.md)

# Messy Data and Tidy Data

Alternatively called "dirty" and "clean", the ideas of messy data and tidy data generally refers to the degree to which data is consistently structured in order to be resuable and machine-readable. For our purposes, tidying up means thinking about data in terms of reusable, machine-readable files, where datasets are transparent and able to be audited whereever possible.

## What is tidy data?

If messy data intuitively refers to data in a raw, unrefined, and inconsistent form, tidy data must necessarily refer to it's opposite - data that has been refined and made consistent. 

[Outlined in 2014 by Hadley Wickham](https://www.jstatsoft.org/article/view/v059i10/), a programmer and statistician, tidy data refers to applying standard ways of optimally formatting data for use with the programming language R. With the recent tidal wave of students, journalists, humanists, artists, and/or scientists interested in engaging data in their research, "tidy data" has taken on a life of its own. Across disciplines and software and file formats awash with new sources of quantitative and qualitative data, who wouldn't want a Marie Kondo to guide us through?

Thinking tidily is helpful for anybody working with data, but particularly for those of us in the humanities and social sciences who may not interact with consistently structured sources in our research, or who have not previously needed to think in specifically structured ways about our resources. Unfortunately humanities data is often some of the messiest, most inconsistent, and otherwise challenging data to work with. Having a few rules of thumb to guide us can be invaluable.

## Why is (humanities) data so messy?

Humanities data is notoriously messy for a variety of reasons. Depending on their field, researches may be accustomed to differing ways of conducting scholarship, making arguments, and citing their sources. An art historian and an archaeologist may look at the same sculpture, but their ways of discussing that same work of art will differ greatly. 

**A quick exercise**: write out today's date and the current time on a slip of paper. Compare your slip with that of others. What do you notice?

Data entered by hand will always be inconsistent, but depending on our needs, that may not be a big deal. If we intend to perform computational analysis or create visualizations, however, we will need to address some of that inconsistency. While there is no ambiguity for a human reader if an extra space happens to appear between two words (for example, `N.  Lombard St`), to a machine, that same value is completely different from any other cell in which those same two words might appear (for example, `N Lombard Street` or `North Lombard`).

## How to keep things tidy

On a macro-level, we can save ourselves substaintial headache and confusion by being mindful of our data files, by keeping folders organized, naming files in a clear manner, and using consistent, logical column headers as we create our datasets. 

On a more micro-level, we should adhere to a few standards as we compile and clean our data:
1. each variable should form a column
2. each observation should form a row
3. each type of observational unit should form a table

Guidelines like these can be incredibly helpful for our sanity as we try to decode historical data or data created by hand. They can also be useful in guiding those of us who are not data scientists but want to create datasets from our research.

[<< Previous](DataFind.md) | [Next >>](ORIntro.md)
