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
