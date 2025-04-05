# Functions
## Overview
Google Sheets has become a powerful tool for data analysis, largely due to its extensive library of embedded [functions](./Glossary.md). Specifically, [COUNTIF](./Glossary.md), [SUMIF](./Glossary.md), and [AVERAGEIF](./Glossary.md) are three essential functions that data analysts and spreadsheet users rely on for quick and efficient data analysis.

In this section, we will provide a step-by-step guide for you to use these three powerful functions. To help you follow each step better, we will use the data below for this guide. To use this sample data to follow the guide, simply copy the table below and paste it to your Google Sheets. To create a new Google Sheets, click [here](https://docs.google.com/spreadsheets/create).

| Department | Employee | Age | Salary | Performance Rating |
|:----------:|:--------:|:---:|:------:|:------------------:|
|    Sales   |   John   |  28 |  45000 |         4.2        |
|  Marketing |   Sarah  |  35 |  52000 |         4.5        |
|     IT     |   Mike   |  32 |  65000 |         4.7        |
|     HR     |   Emily  |  29 |  48000 |         3.9        |
|    Sales   |   David  |  41 |  58000 |         4.3        |
|  Marketing |   Lisa   |  37 |  55000 |         4.1        |
|     IT     |   Alex   |  26 |  60000 |         4.6        |
|     HR     |  Rachel  |  33 |  50000 |          4         |
|    Sales   |    Tom   |  39 |  62000 |         4.4        |
|  Marketing |   Karen  |  36 |  53000 |         3.8        |
|     IT     |   Chris  |  31 |  67000 |         4.8        |
|     HR     |  Jessica |  30 |  47000 |         3.7        |
|    Sales   |   Mark   |  42 |  56000 |         4.1        |
|  Marketing |   Anna   |  34 |  51000 |         3.9        |
|     IT     |  Daniel  |  27 |  63000 |         4.5        |
|     HR     | Michelle |  38 |  49000 |         4.2        |
|    Sales   |   Ryan   |  40 |  59000 |         4.3        |
|  Marketing |   Emma   |  33 |  54000 |          4         |

## COUNTIF
[COUNTIF](./Glossary.md) function can be used when you need to count the number of cells that meet a criterion.
 > Scenario: You need to count the number of employees in Sales department.

![COUNTIF demo](./images_and_gifs/COUNTIF.gif)

1. Click a cell where you want to display the result (e.g., H3).
2. Type `=COUNTIF()` in the cell.
3. Type the [range](./Glossary.md) of cells containing your criteria (e.g., `=COUNTIF(A2:A19)`).
4. Type a comma, followed by the criterion you're looking for (e.g., `=COUNTIF(A2:A19,"Sales")`).
5. Press **Enter**.

    !!! success "Success"
        This formula will count the number of employees in Sales department.

### Using Comparison Operators with COUNTIF
You can use comparison operators (<, >, =, <=, >=, <>) with COUNTIF to create more complex criteria.

1. To count employees who are 35 or older, use: `=COUNTIF(C2:C19,">=35")`
2. To count employees with performance ratings below 4.0, use: `=COUNTIF(E2:E19,"<4")`

    !!! warning "Warning"
        When using comparison operators, make sure to enclose the entire criterion in quotation marks, including the operator.

### Using Wildcards with COUNTIF
COUNTIF also supports [wildcards](./Glossary.md) for partial matching.

* `*` - matches any sequence of characters
* `?` - matches any single character

For example, to count departments that start with "M", use: `=COUNTIF(A2:A19,"M*")`

### Using Multiple Criteria with COUNTIFS
If you need to count the number of cells based on multiple criteria, you can use the COUNTIFS function.
 > Scenario: You need to count the number of employees in Marketing department with a performance rating of 4.0 or higher.

1. Type `=COUNTIFS()` in a cell.
2. First, enter the first criteria range and its criterion (e.g., `=COUNTIFS(A2:A19,"Marketing")`).
3. Add additional criteria ranges and criteria as needed (e.g., `=COUNTIFS(A2:A19,"Marketing",E2:E19,">=4")`).

    !!! success "Success"
        This formula will count the number of Marketing employees with a performance rating of 4.0 or higher.


## SUMIF
[SUMIF](./Glossary.md) function can be used when you need to add all values in cells that meet a criterion.

 > Scenario: You need to calculate the total salary of Sales department.

![SUMIF demo](./images_and_gifs/SUMIF.gif)

1. Click a cell where you want to display the result (e.g., H4).
2. Type `=SUMIF()` in the cell.
3. Type the range of cells containing your criteria (e.g., `=SUMIF(A2:A19)`).
4. Type a comma, followed by the criterion you're looking for (e.g., `=SUMIF(A2:A19,"Sales")`).
5. Type another comma, followed by the range of cells containing the values you want to sum (e.g., `=SUMIF(A2:A19,"Sales",D2:D19)`).

    !!! warning "Warning"
        The sum range must be the same size as the criteria range. If they are in different columns, make sure they have the same number of rows.

6. Press **Enter**.

    !!! success "Success"
        This formula will sum the salaries of all employees in Sales department.

### Using Multiple Criteria with SUMIFS
If you need to sum values based on multiple criteria, you can use the SUMIFS function.

 > Scenario: You need to calculate the total salary of Sales employees who are over 30 years old.

1. Type `=SUMIFS()` in a cell.
2. First, enter the sum range, the range of cells containing the values you want to sum (e.g., `=SUMIFS(D2:D19)`).
3. Then enter the first criteria range and its criterion (e.g., `=SUMIFS(D2:D19,A2:A19,"Sales")`).
4. Add additional criteria ranges and criteria as needed (e.g., `=SUMIFS(D2:D19,A2:A19,"Sales",C2:C19,">30")`).

    !!! success "Success"
        This formula will sum the salaries of all Sales employees who are over 30 years old.

## AVERAGEIF
[AVERAGEIF](./Glossary.md) function can be used when you need to calculate the average of values in cells that meet a criterion.

 > Scenario: You need to find the average performance rating of IT department.

![AVERAGEIF demo](./images_and_gifs/AVERAGEIF.gif)

1. Click a cell where you want to display the result (e.g., H5).
2. Type `=AVERAGEIF()` in the cell.
3. Type the range of cells containing your criteria (e.g., `=AVERAGEIF(A2:A19)`).
4. Type a comma, followed by the criterion you're looking for (e.g., `=AVERAGEIF(A2:A19,"IT")`).
5. Type another comma, followed by the range of cells containing the values you want to average (e.g., `=AVERAGEIF(A2:A19,"IT",E2:E19)`).

    !!! warning "Warning"
        The average range must be the same size as the criteria range. If they are in different columns, make sure they have the same number of rows.

6. Press **Enter**.

    !!! success "Success"
        This formula will calculate the average performance rating of IT employees.

### Using Multiple Criteria with AVERAGEIFS
If you need to calculate averages based on multiple criteria, you can use the AVERAGEIFS function.

 > Scenario: You need to find the average salary of Marketing employees with a performance rating of 4.0 or higher.

1. Type `=AVERAGEIFS()` in a cell.
2. First, enter the average range, the range of cells containing the values you want to average (e.g., `=AVERAGEIFS(D2:D19)`).
3. Then enter the first criteria range and its criterion (e.g., `=AVERAGEIFS(D2:D19,A2:A19,"Marketing")`).
4. Add additional criteria ranges and criteria as needed (e.g., `=AVERAGEIFS(D2:D19,A2:A19,"Marketing",E2:E19,">=4")`).

    !!! success "Success"
        This formula will calculate the average salary of Marketing employees with a performance rating of 4.0 or higher.

## Creating a Summary Dashboard
You can combine these functions to create a powerful summary dashboard for your data:

1. Create a summary table with department names in column G.
2. In column H, use COUNTIF to count employees per department.
3. In column I, use SUMIF to calculate total salary per department.
4. In column J, use AVERAGEIF to find average performance rating per department.
5. In column K, calculate average salary by dividing total salary by employee count.

Example:

| Department | Employee Count | Total Salary | Avg Performance | Avg Salary |
|:----------:|:--------------:|:------------:|:---------------:|:----------:|
|    Sales   |        5       |    280000    |       4.26      |    56000   |
|  Marketing |        5       |    265000    |       4.06      |    53000   |
|     IT     |        4       |    255000    |       4.65      |    63750   |
|     HR     |        4       |    194000    |       3.95      |    48500   |


## Advanced Usage Tips

### Using Cell References for Criteria
Instead of typing criteria directly into your formulas, you can [reference cells](./Glossary.md) containing your criteria:

1. Type your criterion in a cell (e.g., type "Sales" in cell G3).
2. In your formula, reference that cell instead of typing the criterion (e.g., `=COUNTIF(A2:A19,G3)` instead of `=COUNTIF(A2:A19,"Sales")`).

This approach makes it easy to change criteria without editing formulas.

### Handling Errors
When using these functions, you might encounter the following errors.

* `#DIV/0!` - Occurs when dividing by zero (e.g., when no records match your criteria)
* `#VALUE!` - Occurs when using incorrect data types
* `#N/A` - Occurs when a reference is not available

To handle these errors, you can use the IFERROR function like the example below.

`=IFERROR(AVERAGEIF(A2:A19,"Finance",E2:E19),"No Finance Department")`

!!! warning "Warning"
    Always check your data for consistency before using these functions. Typos or inconsistent formatting can lead to incorrect results.

## Conclusion
By the end of this section, you will have successfully learned the following:  

- [x] How to use [COUNTIF](./Glossary.md) to count cells that meet specific criteria
- [x] How to use [SUMIF](./Glossary.md) to sum values based on criteria
- [x] How to use [AVERAGEIF](./Glossary.md) to calculate averages based on criteria
- [x] How to create summary dashboards using these [functions](./Glossary.md)
- [x] How to handle errors

These conditional functions are essential tools for data analysis in Google Sheets. They allow you to quickly extract meaningful insights from your data without the need for complex formulas or programming. By mastering these functions, you'll be able to analyze data more efficiently and make better-informed decisions.