# Troubleshooting

This section provides solutions for common issues you might encounter when using Google Sheets for data analysis.

| **Symptoms** | **Probable Cause** | **Action** |
|--------------|-------------------|------------|
| **Sorting not working as expected** | Hidden rows or merged cells in the data range. | Unmerge any merged cells before sorting. Make sure to select the entire data range including headers. Check for hidden rows that might be excluded from the sort. |
| **Conditional formatting not applying** | Conflicting rules or incorrect formula. | Check for multiple conditional formatting rules that might conflict. Review your custom formulas for errors. Try simplifying complex rules into multiple simpler rules. |
| **Data validation dropdown not showing** | Incorrect range reference or formatting issues. | Verify the range used for validation exists and contains the expected values. Try recreating the data validation rule with a simpler range or explicit list of items. |
| **Formatting disappears after sorting** | Formatting applied to cells rather than data. | Apply formatting to the data itself using conditional formatting rules based on cell values rather than manually formatting specific cells. |
| **Formula returns #DIV/0!** | Division by zero or an empty cell. | Check your formula for division operations and ensure the denominator is never zero. Use the IFERROR function to handle this case: `=IFERROR(A1/B1, "Cannot divide by zero")`. |
| **Formula returns #VALUE!** | Using incorrect data types in a formula. | Verify that the cells referenced in your formula contain the appropriate data types. For example, ensure you do not perform mathematical operations on text values. |
| **Formula returns #REF!** | Reference to a cell that no longer exists. | Check if you have deleted rows or columns that were referenced in your formula. Restore the deleted data or update your formula to reference existing cells. |
| **Formula returns #NAME?** | Function name is misspelled. | Double-check the spelling of function names. |
| **Functions returning unexpected results** | Mixed data types or hidden values affecting calculations. | Check for inconsistent data types in your range. Look for hidden rows or filtered data that might be included in calculations. Verify that text values aren't being interpreted as zeros. |
| **Chart not updating with new data** | Chart data range is fixed. | Edit the chart data range: click on the chart, select the three dots menu, choose **Edit chart**, and update the data range in the Chart editor. |
| **Linear regression trendline missing** | Insufficient data points or non-numeric data. | Ensure your data contains at least two valid numeric data points. Check for any text or error values in your data series that might prevent the trendline from appearing. |
| **Cannot access sheet (Trying to connect...)** | Internet connection issues or Google service disruption. | Check your internet connection. Verify Google Sheets service status at [Google Workspace Status Dashboard](https://www.google.com/appsstatus). Try accessing the sheet in incognito mode to rule out browser extension issues. |

!!! warning "Warning"
    Always make a backup copy of important spreadsheets before attempting significant changes or troubleshooting steps that might alter your data.

!!! info "Info"
    For persistent issues not covered in this troubleshooting guide, visit the [Google Sheets Help Center](https://support.google.com/docs/topic/9054603) or use the **Help** menu in Google Sheets to search for specific error messages. 