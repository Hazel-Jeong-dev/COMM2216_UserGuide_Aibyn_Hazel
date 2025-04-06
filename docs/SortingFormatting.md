# Sorting and Formatting Data
## Overview
Organizing and presenting data effectively is essential for data analysis. Google Sheets provides powerful tools for sorting and formatting data that can transform raw information into clear, actionable insights. This section will guide you through the process of sorting data and applying formatting to enhance readability and analysis.

In this section, we will provide a step-by-step guide for sorting and formatting data in Google Sheets. To help you follow each step better, we will use the sample data below for this guide. To use this sample data to follow the guide, simply copy the table below and paste it intto your Google Sheets. To create a new Google Sheets, click [here](https://docs.google.com/spreadsheets/create).

| Product | Category | Sales | Date | In Stock |
|:-------:|:--------:|:-----:|:----:|:--------:|
| Laptop  | Electronics | 2500 | 2023-01-15 | Yes |
| Desk Chair | Furniture | 850 | 2023-01-22 | Yes |
| Headphones | Electronics | 320 | 2023-01-18 | Yes |
| Desk | Furniture | 1200 | 2023-01-10 | No |
| Monitor | Electronics | 950 | 2023-01-25 | Yes |
| Bookshelf | Furniture | 750 | 2023-01-30 | No |
| Keyboard | Electronics | 180 | 2023-01-05 | Yes |
| Coffee Table | Furniture | 650 | 2023-01-12 | Yes |
| Mouse | Electronics | 75 | 2023-01-08 | Yes |
| Filing Cabinet | Furniture | 420 | 2023-01-20 | No |

!!! info "Info"
    If you encounter any error message or if you do not get the same output while following this guide, check our [troubleshooting](./Troubleshooting.md) page.

## Sorting Data
Sorting data allows you to organize information in a meaningful way, making patterns and trends easier to identify.

### Basic Sorting
> Scenario: You need to sort products by their sales figures from highest to lowest.

![Basic Sorting](./images_and_gifs/BasicSort.gif)

1. Select the entire data [range](./Glossary.md) that you want to sort including headers if there are headers (e.g., A1:E11).
2. Click on **Data** in the top menu.
3. Select **[Sort range](./Glossary.md)** from the dropdown menu.

    !!! info "Info"
        You can also right-click on the selected range and choose **Sort range** from the context menu.

4. In the dialog box that appears, check **Data has header row** if your data includes column headers.
5. Select the column you want to sort by (e.g., "Sales").
6. Choose the sort order (A→Z for ascending, Z→A for descending).
7. Click **Sort**.

    !!! success "Success"
        Your data is now organized by sales figures from highest to lowest.

### [Multi-Level Sorting](./Glossary.md)
> Scenario: You need to sort products first by category and then by sales within each category.

![Multi-Level Sorting](./images_and_gifs/MultiLevelSort.gif)

1. Select the entire data range that you want to sort including headers if there are headers (e.g., A1:E11).
2. Click on **Data** > **Sort range**.
3. Check **Data has header row** if your data includes column headers.
4. Select the column you want to sort by first and its sort order (e.g., "Category" and A→Z).
5. Click **Add another sort column**.
6. For "Then by," select the column you want to sort by next and its sort order (e.g., "Sales" and Z→A)
7. Click **Sort**.

    !!! success "Success"
        Your data is now organized by category alphabetically, with products in each category sorted from highest to lowest sales.

## Formatting Data
Proper formatting enhances readability and helps highlight important information in your data.

### Number Formatting
Google Sheets offers various number formatting options to display your data appropriately.
> Scenario: You want to format the sales figures as currency.

![Number Formatting](./images_and_gifs/NumberFormatting.gif)

1. Select the number cells you want to format (e.g., C2:C11).
2. Click on **Format** in the top menu.
3. Select **Number**.
4. Choose from options (e.g., **Currency**):  
    - **Number**: Displays values as general number format with specified decimal places
    - **Percent**: Displays values as percentages
    - **Currency**: Displays values with currency symbols
    - **Date**: Displays values with various date formats
    - **Time**: Displays values with various time formats
    - **Custom number format**: Displays values with your own format
    
    !!! success "Success"
        The sales figures are now in the currency format.

### [Conditional formatting](./Glossary.md)
> Scenario: You want to highlight the "In Stock" status.

![Conditional Formatting](./images_and_gifs/ConditionalFormatting.gif)

1. Select the cells or the column you want to highlight (e.g., E2:E11).
2. Click on **Format** in the top menu.
3. Click on **Conditional formatting**.
4. In the sidebar that appears, set the following settings:  
    - Format cells if...: Choose a format rule (e.g., "Text is exactly" > "Yes" in the value field)
    - Formatting style: Choose a cell style for the cells that meet the format rule (e.g., a green fill colour)
5. Click **Add another rule** to add more rules, if needed (e.g., "Text is exactly" > "No" in the value field with a red fill colour)
6. Click **Done**.

    !!! success "Success"
        The "In Stock" status are now highlighted with a green fill colour for "Yes" and a red fill colour for "No".

### Creating [Alternating Row Colours](./Glossary.md)
Alternating row colours can make large datasets easier to read.

![Alternating Row Colours](./images_and_gifs/AlternatingColours.gif)

1. Select the entire data range (including headers).
2. Click on **Format** > **Alternating colours**.
3. In the sidebar, select a colour scheme from the preset options or create a custom one.
4. Click **Done**.

    !!! info "Info"
        You can customize the header colour, odd row colour, and even row colour separately by clicking on each element in the sidebar.

## Advanced Formatting Techniques

### Custom Number Formats
You can create custom number formats for specific needs.

![Custom Number Formats](./images_and_gifs/CustomFormats.gif)

1. Select the cells to format.
2. Click on **Format** > **Number** > **Custom number format**.
3. Enter a format pattern, such as:
    - `$#,##0.00 "in sales"` to display "$1,200.00 in sales"
    - `0.0%` to show percentages with one decimal place
    - `[>1000]"High";"Low"` to display "High" for values over 1000 and "Low" for others

### Using Data Validation
[Data validation](./Glossary.md) helps maintain data integrity.

![Data Validation](./images_and_gifs/DataValidation.gif)

1. Select a column where you want to restrict input (e.g., the Category column).
2. Click on **Data** > **Data validation**.
3. Set "Criteria" to "Drop-Down".
4. Enter valid categories in each line.
5. See what happens when invalid data is entered.
6. Click **Save**.

    !!! warning "Warning"
        Apply data validation before entering data to ensure consistency throughout your spreadsheet.

## Conclusion
By the end of this section, you will have successfully learned the following:  

- [x] How to sort data using single and multiple criteria
- [x] How to apply number formatting to different types of data
- [x] How to use [conditional formatting](./Glossary.md) to highlight important information
- [x] How to create [alternating row colours](./Glossary.md) for better readability
- [x] How to implement advanced formatting techniques

Effective sorting and formatting are fundamental skills that transform raw data into meaningful information. By mastering these techniques in Google Sheets, you'll be able to create professional spreadsheets that communicate insights clearly and efficiently. 