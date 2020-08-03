# Tableau

## Section 1: It's Super Easy to Get Started

### Lecture 3 - Installation

- Install Tableau from the [Tableau](https://www.tableau.com/) site
  - Click the "Try Now" button and follow the steps to start the free 14-day trial of Tableau Desktop
  - Can use [Tableau Public](https://public.tableau.com/s/), which is free
    - Some restrictions, including not being able to do extractions and having to save to the Tableau Public server

### Lecture 5 - Exercise - Get Excited!

- Download the first data set from the course [website](https://www.superdatascience.com/pages/tableau)
  - The data set is under Section 1: Getting Started and is called SuperStoreUS-2015.xlsx
- Data set is a store (company's) list of transactions for the first half of 2015
  - Each row represents one transaction
- Goal:
  - Which state(s) are the most profitable?
  - Create a map showing each state's profitability
- In Tableau
  - Under "To a file"
    - Click "Microsoft Excel" &rarr; find and open the data set
  - On the left, click and drag the "Orders" tab into the area w/ "Drag sheets here" &rarr; provides a preview of the spreadsheet
  - Click "Sheet 1" in bottom left, which gives access to the Tableau workspace
    - On the upper left, find, click, and drag "Country" into the area w/ "Drop field here" &rarr; displays a map (of the United States)
    - On the upper left, find, click, and drag "State or Province" onto the map
    - On the lower left, find, click, and drag "Profit" onto "Color", which is under "Marks"
    - On the lower left, find, click, and drag "Profit" onto "Label", which is also under "Marks"
    - Click on "Label" &rarr; "Font" &rarr; change the font size to 12
- The map now shows the profitability of each state in an easy to read manner
  - Least profitable state is North Carolina and most profitable state is California
  - Other insights

### Lecture 7 - Get the materials

- The materials for this course can be found on the course [website](https://www.superdatascience.com/pages/tableau)

## Section 2: Tableau Basics: Your First Bar Chart

### Lecture 1 (10) - The Business Challenge - Who Gets the Annual Bonus?

- Section 2 - Challenge
  - It is (It's) EOFY and that means time for annual bonuses!
  - The store operates in three regions and only the top-performing employee in each region qualifies for a bonus. Find out which three employees are eligible to get bonuses for this year.
  - Employees are measured on total sales (\$\$).
  - The data set is available on the course [website](https://www.superdatascience.com/pages/tableau)
    - Download the applicable file (OfficeSupplies.csv for Windows, OfficeSupplies-MAC for Mac, etc.)
    - The data set contains a list of transactions separated by region as well as the representative's name (i.e. who conducted the transaction). Also included in the data set is the item sold, the number of units, and the price per unit.

### Lecture 2 (11) - Connecting Tableau to a Data File - CSV File

- Under the "Connect" column &rarr; "To a file" &rarr; ability to connect to a number of different file types
  - A CSV (comma-separated values) file is a text file delimited by commas
- Select "Text file" &rarr; find and open the data set (OfficeSupplies.csv) &rarr; redirected to the Connections Manager for the data source
  - On the left is a directory that shows what files of the same type are available (it seems like the files)
  - Dragging files into the "Need more data?" area &rarr; Tableau will try and connect the files and basically join them
    - Data you are working w/ can come from many files, many tabs in a file, etc.
  - Bottom is a preview of the file (rows and columns)
    - Tableau can automatically identify the type of data contained in a column, e.g. date, text, number, etc.
- Proceed to the dashboard by selecting "Sheet 1"
  - On the left is a "Data" column which shows our data source
    - Right-click on the data source &rarr; "View Data..." will provide a preview of the data
  - Find the "Show Start Page" and "Hide Start Page" buttons in the upper left
    - Add additional data source(s)

### Lecture 3 (12) - Navigating Tableau

- Clicking on "Sheet 1" will bring up the Tableau workspace
- Tableau workspace comprised of two main areas
  1. "Data" connection/tab on the left
     - In previous versions of Tableau, this area is further broken down into "Dimensions" and "Measures"
     - Dimensions and Measures are two different roles that any data element can take
       - Dimensions &rarr; categorical/quantitative values or independent variables (e.g. "Region")
       - Measures &rarr; numerical values or dependent variables (e.g. "Units")
       - Default setting in Tableau, but can always move item(s) from one to the other
  2. The work(ing) area on the right
     - Main elements are "Columns" and "Rows"
     - Most Worksheets created by deciding what goes into Columns and what goes into Rows, but also what goes into other elements (e.g. color, size, etc.)
- Navigation bar
  - A "Dashboard" contains multiple "Worksheet"s
  - "Story" is a combination of "Worksheet"s and "Dashboard"s
- Learn by doing
  - Drag Region into the work area
  - Drag Units onto Region in the work area
  - Tableau has
    - Put Region into Rows
    - Summed (aggregated) the Units by Region and put them into a label
      - Alternatively, drag the "SUM(Units)" from under "Marks" to Columns &rarr; bar chart/graph
      - Can also click on the highlighted recommendation under "Show Me"
        - Some choices under Show Me are grayed out because there needs to be certain elements of data to create these
      - Note the tooltip that appears when hovering over a bar
      - Can do any number of data visualizations (pie, bubble, box, etc.)

### Lecture 4 (13) - Creating Calculated Fields

- Use the "Clear Sheet" icon in the ribbon to clear the Worksheet
- Create a bar chart for the representatives and see the number of units they have sold
  - Drag "Rep" into Columns
  - Drag Units into Rows
  - Now break down by region
    - Three bonuses total, one for the best representative in each region
    - Drag Region into Columns (before Rep)
    - Chart is now broken down by region (first) and then by representative (second)
  - Order the bars by their size using the "Sort" icon above Units
  - Does not give the answer to which representative in each region should get a bonus as the chart does not show the representative's sales numbers
    - Need to create a "Calculated Field"
- Creating a Calculated Field
  - Important to know how to do this as your data is probably not detailed enough, aggregated correctly, etc. for what you need
  - Right-click in the Measures area and select Calculated Field
  - In the work area type in the name of the Calculated Field, i.e "Total Sales"
  - Beneath Total Sales add the calculation, which in this case is [Unit Price] \* [Units]
  - Remove anything in Rows and drag Total Sales onto Rows
  - The resulting chart/graph shows who should receive bonuses (Matthew for Central, Susan for East, and James for West)

### Lecture 5 (14) - Adding Colors

- Color is important for telling the data's story
  - Imagine a chart going into a presentation for the executives of the company who will be distributing the bonuses or as a picture that may be hung on a wall so that everybody can see
  - Want the chart to be bright and colorful &rarr; use the Color button
- Color the chart from the previous lecture
  - Basic color change by clicking the Color button and selecting a color
  - The Color button also lets you change the transparency, add a border, etc.
  - Have the colors differ from bar to bar (i.e. have a different color for each representative)
    - Drag Rep onto the Color button
      - Each representative will now be represented by a different color
      - Color legend also given
    - Alternative
      - Drag Rep from Columns and, while holding the CTRL button, drop onto the Color button
      - Useful when you have lots of dimensions
    - Not happy with the colors?
      - Click the Color button &rarr; Click the "Edit Colors..." button &rarr; select the desired color palette &rarr; Click the "Assign Palette" button
  - Replace Rep with SUM(Total Sales)
    - Now a continuous color instead of a discrete color
    - The darker the blue, the more in Total Sales the representative has
  - Replace SUM(Total Sales) with Region
    - Now bars are colored by region
    - See that there are three distinct regions (or elements)
      - Backs the idea of why there are three bonuses

### Lecture 6 (15) - Adding Labels and Formatting

- Make the chart look awesome AND also make the chart easy to understand
- How much in Total Sales did Bill have? What about James?
  - The further away you get from the y-axis, the harder it is to tell
  - Want to make the visualizations easy to understand
- Add the SUM(Total Sales) as a label
  - While pressing the CTRL button, click and drag SUM(Total Sales) from Rows to the Label button
    - The SUM(Total Sales) for the associated represenative now appears at the top of the representative's bar
- Can add additional labels by dragging dimension(s) onto the Label button
  - Do not overdo it
- Can modify the label
  - Click on the Label button &rarr; click on the ... after the "Text" field &rarr; modify the label as desired
  - If the label does not appear &rarr; right-click on the bar &rarr; select "Mark Label" &rarr; select "Always Show"
- Formatting the chart
  - Change the font
    - Click the Label button &rarr; click on the "Font" dropdown &rarr; change the font size to 12 and make the font bold
    - Can also be done by selecting the ... after the Text field under Label
  - Change the type of the label
    - Right-click on the label (i.e. SUM(Total Sales) in the Marks area) and select "Format"
    - Make sure you are in "Pane"
    - Select "Currency (Custom)" from the "Numbers" dropdown under "Default"
      - Change "Decimal places" to 1 and "Display Units" to Thousands (K)
  - Format the axes
    - For all axes
      - Right-click on the axis and select Format
      - Select "Axis"
        - Click on the dropdown for Font under Default and change the font size to 12
    - Right-click on "Region / Rep" &rarr; select "Hide Field Labels for Columns"
- Be consistent throughout

### Lecture 7 (16) - Exporting Your Worksheet

- Learn how to export Worksheets as images for other files
- In the navigation bar
  - Select "Worksheet" &rarr; "Export" &rarr; "Image..."
- Alternatively
  - Right-click &rarr; "Copy" &rarr; "Image..."
- Don't need "Caption" as we do not have one
- Can just CTRL + v into a Word document, PowerPoint, etc.
- Why does it still say "Sheet 1" and how do we get rid of it?
  - The "Title" is the name of the tab, so either unclick or rename the tab
  - Double-click on the Title to change the font size, color, etc.
- When copying the image, know the way in which to make the chart bigger (e.g. putting the legend beneath the chart)
- Save your work as Tableau does not autosave

### Lecture 8 (17) - Get the Viz

- Download all the visuals and workbooks for the course at the following [site](https://public.tableau.com/profile/kirill.eremenko#!/)

### Quiz 1: Tableau Basics

- Question 1: To connect Tableau to a CSV data source what type of connection should you use?

  - Excel
  - **Text File**
  - Access
  - Statistical File

- Question 2: What are the two main groups that all fields are broken up into in Tableau?

  - Items and Regions
  - Labels and Values
  - Details and Quantities
  - **Dimensions and Measures**

- Question 3: What are calculated fields in Tableau?

  - There is only one calculated field in Tableau: 'Number of Records'
  - Any numeric field is a calculated field because it can be used in a calculation
  - **These are custom variables that you create from fields provided in the Data**
  - Calculated fields have to be created in Excel and then imported into Tableau

- Question 4: How many fields can you add to be shown in the label?

  - Maximum 1
  - Maximum 2
  - Maximum 3
  - **No limit**

- Question 5: What is the main thing you should take into account when setting the colours for your chart in Tableau?
  - Trick question! Colours are automatically set by Tableau and cannot be changed
  - The number of objects on your chart. You should use as many colours as possible. Ideally, every object should have a unique color.
  - **The main thing to take into account is the end user / viewer. Colours should assist them in seeing the insights your chart is portraying.**
  - Colours don't matter in Data Science visualizations. Random or default colours should be fine.

## Section 3 - Time series, Aggregation, and Filters

### Lecture 1 (18) - Section Intro

- Looking at a data set containing information about long-term unemployment rates in the U.S. for the past couple of years
- Visualize how things change, trends, and breaking them down by different categories
  - Working with and visualizing time series data
- Granularity and aggregation
  - Foundation of Tableau
  - Understand what is going on behind the visuals being created
- Filters and quick filters
- Final product will be an (formatted) area chart

### Lecture 2 (19) - Working with Data Extracts in Tableau

- Download the data set from the course [site](https://www.superdatascience.com/pages/tableau)
  - Section 3: Timeseries, Aggregation and Filters > Long-Term-Unemployment-Statistics.xlsx
- Explore the data
  - A lot of "duplicate" records in many of the columns
    - Effectively the data is broken down by age, gender, and period &rarr; so many different age groups that gender and period get repeated
  - Data is structured in a very non-human like way
    - Not a good way to quickly and efficiently present the data
    - Easy to import into Tableau
  - A better way of presenting the data would be something that does not duplicate the ages or genders
  - ![Present Data Better](Images/BetterPresentData.jpg)
    - Harder to import into Tableau
- Open Tableau and connect to the data source
  - To a File > Microsoft Excel
- Working with Extract(s)
  - In the Worksheet, underneath the Data tab, there is Sheet1 (P1-Long-Term-U...), which is the data
    - Right-click and select "Extract Data..."
      - Creates an extract for Tableau to work from
    - Click the "Extract" button
    - Select the save location and click the "Save" button
    - Note how the icon has changed
  - Instead of working or connecting to live data, the data is extracted into a separate file and kept there
    - Changing the extract will not change the data in the original data source and vice versa
      - Can right-click on the data source, choose Extract, and then select "Refresh" to get around
  - Not really necessary when working with small data sets, but using the Live connection may be slow and-or unreliable when working with large data sets
    - Can always go back to live by right-clicking on the data source and unchecking "Use Extract"
  - More about extracts can be found (here)[https://help.tableau.com/current/pro/desktop/en-us/extracting_data.htm#:~:text=Extracts%20are%20saved%20subsets%20of,filters%20and%20configuring%20other%20limits.]

### Lecture 3 (20) - Working with Time Series

- Save the workbook
- Look at the data
  - Right-click on the data source and select "View Data"
  - Age, Gender, Period, and Unemployed values
  - Want to see how unemployment changes over time (i.e. as the period changes)
- Double-click on "Unemployed" and then double-click on "Period"
  - Observe the results
    - Put Unemployed into Rows and summed it up
    - Put Period into Columns and taken the year of the Period
    - Aggregation
      - Tableau is taking all of the data it can see for a year and summing up all of the values in all of the rows for that year (irrespective of gender, month, etc.)
- Initial result is missing granularity or the finer details
  - How to get?
  - Under Columns > Hover over YEAR(Period) and select the dropdown
    - Note that there are two sections responsible for time
      - What is the difference between the two sections?
        - The first section treats the selected timeframe as a dimension
        - The second section treats the selected timeframe as a measure
          - Year > Quarter > Month ... Least granularity (resolution) > Most granularity (resolution)
      - Click on "Month" in the first section
        - No longer have years at the bottom but have months
        - Only one of each month instead of many of each month
        - Tableau is taking the data for each individual month, aggregating (summing) it, and then summing all of that month across all the years (i.e. January on the Chart = January 2005 + January 2006 + ... + January 2015)
          - No real meaning to this value or visualization
          - Occuring because Tableau is recognizing MONTH as a dimension
          - Tableau is creating a calculation (which is, effectively, a new variable that Tableau recognizes as a dimension) &rarr; double-click on "MONTH(Period)" to see the calculation
          - Treating the new variable as a dimension or categorical variable
            - Only has 12 categories and is putting data into those categories
      - Want a timeline, not different categories of months &rarr; Click on "Month" in the second section
        - Chart has changed
        - Notice that MONTH(Period) is now green and therefore is being recognized as a measure
- Tableau always highlights Dimensions in blue and Measures in green
- Need to understand what you want from your time data
  - Do you want it to be a dimension or measure?
  - How much granularity (resolution) do you want?
- Verify data
  - Google search for "unemployment 27 weeks fred"
  - [Unemployment Data](https://fred.stlouisfed.org/series/UEMP27OV)
  - Similar looking charts
    - Some differences, which will occur due to different data sources, but well within reason

### Lecture 4 (21) - Understanding Aggregation, Granularity, and Level of Detail

- Aggregations and granularity are foundational to Tableau (i.e. they govern how Tableau operates)
- Chart shows unemployment in the U.S. from month-to-month from 2005 to 2015
  - How does Tableau know that we want to see the visualization of the data at the monthly level?
  - How does Tableau know that the aggregation it is doing, i.e. summing up the Unemployed variable, how does it know that we want to see the data visualized at the monthly level (i.e. to sum up the variable at the monthly level)?
  - Answer: Tableau will always aggregate measures at the level of granularity of your worksheet
    - Variable MONTH(Period) &rarr; Tableau knows that the plotting is to be done at the level, or granularity, of one month
    - What happens if we remove MONTH(Period) from Columns?
      - Tableau has no idea what granularity we want to see the worksheet and therefore just assumes the broadest level possible (i.e. at the level of the whole data set) &rarr; will sum up all values for the Unemployed variable into a single value and visualizes that
- The concept behind Tableau is that Measures get aggregated and Dimensions specify the level of granularity
  - In our case, even though MONTH(Period) is a measure, it is the variable that is specifying the level of granularity
    - Result of introducing the axis, or timeline, at the bottom which specifies that the granularity should be at the monthly level
- Alter aggregation
  - Go to the navigation bar and select "Analysis" &rarr; De-select "Aggregate Measures"
  - Select the dropdown under Marks and choose "Shape"
  - Instead of aggregating the data, Tableau is plotting Unemployed, i.e. Tableau is separately plotting every single row of the data set
    - Lots of points due to having different age groups, genders, etc.
    - The total numer of marks can be found in the lower left corner and is now equal to the number of rows in our data set
  - Turn aggregation back on
- Instead of switching aggregation off, introduce a dimension which will change the level of granularity and therefore affect the aggregation
  - Drag "Gender" onto Color
    - Blue represents male unemployment for that month
    - Orange represents female unemployment for that month
  - Tableau knows that we want to see all the measures aggregated at the level of month plus gender
    - The chart has become more granular
  - Add more Dimensions to increase granularity
    - Drag Age onto Shape
    - Tableau knows that the sum now needs to be calculated using month, gender, and age
- Different types of aggregations that are available
  - Change from SUM(Unemployed)
    - Rows > SUM(Unemployed) > Click on dropdown and select "Measure (Sum)" > "Measure (Average)"
      - Chart does not change much, but the axis does
- Detail
  - Increase level of granularity &rarr; make dashboard more detailed, but do not want to drag any Dimensions onto Color, Shape, etc. (i.e. you do not want to affect the visual)
  - Use "Detail" which is under Marks
  - Drag Age onto Detail
    - Shapes have not changed, but granularity of the chart has changed
  - Add Dimensions and Measures to the dashboard to increase granularity without affecting the visual representation
  - Control at which level the aggregation is going to happen

### Lecture 5 (22) - Creating an Area Chart & Learning About Highlighting

- How to create an area chart
- Chart at present is way too cluttered to present any insightful information
  - May come across a chart like this when doing data discovery process &rarr; may need to look for anomalies, trends, and patterns in a chart that is not perfect
  - For every month there are 14 (seven age groups and two genders &rarr; 14) observations present
  - What happens if you want to investigate one gender?
    - Can restructure the chart and just leave the one gender of interest OR
    - Can use highlighting &rarr; achieve the same result, but much faster
      - Go to legend and click on the gender you are interested in
  - What about highlighting age?
    - Age as a level of granularity obtained by dragging Age into Detail, so not a Color, Shape, etc.
    - Highlighting age requires giving it some sort of visual representation or chart
      - Drag Age into Shape
      - Click on button in the Age legend that says "Highlight Selected Items"
      - Focus on different unemployments for different age groups
- Create an area chart
  - Take Gender out
  - Take Age out
  - Change to Automatic/Line
  - Change to SUM(Unemployed)
  - Take Age and drag into Color &rarr; many lines with the chart ranging from 0 to 1.6 million w/ every single line being independent
    - Visual is not very useful, not easy to understand &rarr; change the visualization to a different type
      - Can use Show Me and click around to find a chart type that works
        - Select area charts (continuous)
      - Area chart from scratch
        - Select the dropdown under Marks and go to Area
        - Unemployment rates now stacked on top of one another
        - Notice the difference in the axis between the Line and the Area charts
          - When stacked, the unemployment is summed
          - The unemployment for each age group is given by the pop-up
        - Add some labels and format to make everything clearer
          - CTRL and drag Age onto Label
          - Change the size of the label to 12 and make bold

### Lecture 6 (23) - Adding a Filter and Quick Filter

- Adding a filter
  - What information is missing on the chart? &rarr; Gender
    - One way to add gender to the chart is by putting gender into a filter
      - Take Gender or the variable that you want to add as a filter and put it into the "Filters" shelf
        - Filter pop-up displays and can add settings to the filter
          - "Select from list" is for Dimensions
          - Click on the "All" button
          - Exclude allows you to filter out what you do not want to see
          - Chart did not change, but now Gender is a filter
          - Can use the dropdown and select "Edit Filter..." to edit the filter and show only men, only women, or both men and women
- Quick filter
  - Use the dropdown and select "Show Filter" to see the filter and turn off and on the filter as desired
  - Dropdown on newly created quick filter allows you to select different types of filter (e.g. Single Values, Multiple Values, etc.)
- Create a filter and quick filter for age
  - See what you obtain when selecting a different type of filter (e.g. Single Value (list))
  - Remove the filter and quick filter for age
- Format the axes and the title

### Quiz 2: Timeseries, Aggregation, and Filters

- Question 1: Which of these is a valid reason to use a Data Extract over a Live Connection to the Dataset in Tableau?

  - Extracts always take up less space than the data
  - Extracting data automatically fixes any data errors
  - Your Data is in Excel therefore you have to create an extract to work in Tableau
  - **Your Data is constantly being updated and you want to work with a static file when building your visual (you will later return to the live connection when the visual is ready)**

- Question 2: What is the difference between the Blue Month() and the Green Month() in Tableau?

  - **Blue is a dimension and Green is a measure; Blue ignores higher periods such as year and treats month as a category - just like Gender; Green creates a proper timeline**
  - Blue is a measure and Green is a dimension; Blue ignores higher periods such as year and treats month as a category - just like Gender; Green creates a proper timeline
  - Blue is a dimension and Green is a measure; Green ignores higher periods such as year and treats month as a category - just like Gender; Blue creates a proper timeline
  - Blue is a measure and Green is a dimension; Green ignores higher periods such as year and treats month as a category - just like Gender; Blue creates a proper timeline

- Question 3: How does Tableau know at which level to aggregate values?

  - Values are always aggregated at the Month level
  - Values are always aggregated at one level above the level of granularity of the worksheet
  - **Values are always aggregated at the level of granularity of the worksheet**
  - Values are always aggregated at the maximum level of granularity of all of the worksheets in the workbook

- Question 4: Which of these explains the conceptual difference between a line chart and an area chart?

  - In a line chart lines cannot cross, but they can cross in an area chart
  - **An area chart stacks up values of different categories on top of each other, whereas a lilne chart visualizes them separately**
  - An area chart always has more colours than a line chart
  - You can use colour highlighting on an area chart, but not on a line chart

- Question 5: Which of these is NOT a type of Quick Filter available in Tableau?

  - Single Value (List)
  - Multiple Values (List)
  - Wildcard Match
  - **JSON Lookup (Category)**
