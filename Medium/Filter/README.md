There are three levels of filters in Power BI: report, page, and visual.

Report-level filters are those that affect all of the data in the report, regardless of what you're looking at. Think of them as universal filters.

Page-level filters only filter the data on a given page, which makes them useful for creating pages that focus on particular subsets of your data. 
For example, you can use page-level filters to make one page focus solely on revenue data, while the next page focuses on expense data. 
Page-level filters operate within the context of the report-level filters, which means that a page-level filter cannot override a report-level filter. 
They also cannot be programmed to filter the data on other pages.

Visual-level filters only filter the data on a given visual, whether that's a table, chart, card, slicer, etc. 
These are the most granular filters you can apply to your data, and they operate within the context of both the page-level and report-level filters, 
which means visual-level filters cannot override them, nor can they be programmed to filter data on other visuals.


Filtering Modes
Each filter has two modes you can use when running your report: Basic Filtering and Advanced Filtering.

In Basic Filtering, you are given a list of values which is scrollable and searchable. 
To search for a value, simply type a keyword or identifier into the search box, and the list of available values will automatically update based on the search criteria you entered. 
You can then select one or multiple entries from the list using the white checkboxes to the left of each entry. 

With Advanced Filtering, you won't see a list of values to choose from, but you can use rules to determine a range of values the report will return. 
