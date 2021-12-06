# UFO-sighting

## Overview of Analysis

### Purpose
I'm assisting a journalist named Dana write about UFOs. Dana has a javascript file of data on UFO sightings, including location and description.

### Development
The data was rendered onto a website using HTML and with a CSS bootstrap. The data was formatted into a table. The user was given five search boxes to filter the data based on: date, city, state, country and object shape. When the user types in the filter fields, it automatically updates the table to show only the identified information.

## Results

### Performing a Search
![datafilter](https://user-images.githubusercontent.com/24308495/144783202-0b3b3d0e-52f0-4366-b0bd-12a84fefbae5.PNG) <br>
This is the layout of the webpage for the data search. Users enter text into the search box, and it filters the data based on the search.
<br>

### Listening for Change
It does this by listening for changes to any of the d3 html elements. When a change occurs, it launches a function called updateFilters. <br>
![1listen](https://user-images.githubusercontent.com/24308495/144783215-debe9a05-c78e-4e2b-b9d9-bd031d05da45.PNG) <br>

### Updating Filters
The function updateFilters stores the value that was input into the search box as a key-value pair based on which search box received the input. If there was previously a value for the key, that value is updated to the new data. If there is no data in the search box, the key is removed from the filter. Then the code launches the function filterTable. <br>
![2collectfilters](https://user-images.githubusercontent.com/24308495/144783219-d2cdde6f-d76f-4363-99ea-9f800e04cc1c.PNG) <br>

### Filtering the Table
The filterTable function takes the key from the filters variable and identifies the column it is filtering. Then it iterages through each row to find cells that match the value. It does this for each key-value pair. The rows that remain are used in the buildTable(filteredData) function to build a new table with only the filtered rows. <br>
![3filtertable](https://user-images.githubusercontent.com/24308495/144783226-7900a96f-4580-48d3-b9d1-305380ea65be.PNG)
 <br>
 
### Build Table
The buildTable function pulls in the filteredData variable to construction a new table that shows only the filtered data.
![4buildfilteredtable](https://user-images.githubusercontent.com/24308495/144783234-4b9ae0d4-eb75-4ab1-aaad-f6b3051f0f0b.PNG)

## 
