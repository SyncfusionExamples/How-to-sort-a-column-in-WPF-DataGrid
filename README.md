# How to sort a column in WPF DataGrid
## About the sample
This example illustrates how to sort a column in WPF DataGrid by enabling AllowSorting property for SfDataGrid or corresponding column

By default, sorting is enabled for columns in DataGrid. Sorting can be performed by clicking a column header. You can enable/disable the sorting for all the columns in datagrid by using [DataGrid.AllowSorting](https://help.syncfusion.com/cr/cref_files/wpf/Syncfusion.SfGrid.WPF~Syncfusion.UI.Xaml.Grid.SfGridBase~AllowSorting.html) property. Moreover, you can also enable/disable the sorting for a particular column by using Column.AllowSorting.

By default, DataGrid allows you to sort the data against one or more columns by clicking a column header by pressing <kbd>Ctrl</kbd> key. Sorting orders to denote the order of sorting performed for columns by using the DataGrid.ShowSortNumbers property.

You can sort a column in programmatic way by using the DataGrid.SortColumnDescriptions property.

### UI Sorting
```xml
        <syncfusion:SfDataGrid  x:Name="dataGrid" 
                        AllowSorting="False"
                        ShowSortNumbers="True"
                        ItemsSource="{Binding Orders}">
            <syncfusion:SfDataGrid.Columns>
                <syncfusion:GridTextColumn MappingName="OrderID" />
                <syncfusion:GridTextColumn MappingName="CustomerID" AllowSorting="True"/>
                <syncfusion:GridTextColumn MappingName="CustomerName" AllowSorting="True"/>
                <syncfusion:GridTextColumn MappingName="Country"/>
                <syncfusion:GridTextColumn MappingName="ShipCity" AllowSorting="True"/>
            </syncfusion:SfDataGrid.Columns>
        </syncfusion:SfDataGrid>
```
### Programmatic sorting

```xml
        <syncfusion:SfDataGrid.SortColumnDescriptions>
            <syncfusion:SortColumnDescription ColumnName="OrderID" SortDirection="Ascending" />
            <syncfusion:SortColumnDescription ColumnName="CustomerName" SortDirection="Descending" />
        </syncfusion:SfDataGrid.SortColumnDescriptions>
```


## Requirements to run the demo
Visual Studio 2015 and above versions
