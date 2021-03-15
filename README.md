# How to sort a column in WPF DataGrid (SfDataGrid)?
## About the sample

This example illustrates how to sort a column in [WPF DataGrid](https://www.syncfusion.com/wpf-ui-controls/datagrid) (SfDataGrid) by enabling AllowSorting property for SfDataGrid or corresponding column

[WPF DataGrid](https://www.syncfusion.com/wpf-ui-controls/datagrid) (SfDataGrid) allows you to sort the data against one or more columns either in ascending or descending order. The sorting can be performed by clicking a column header. You can enable/disable the sorting for all the columns in DataGrid by using [DataGrid.AllowSorting](https://help.syncfusion.com/cr/cref_files/wpf/Syncfusion.SfGrid.WPF~Syncfusion.UI.Xaml.Grid.SfGridBase~AllowSorting.html) property. Moreover, you can also enable/disable the sorting for a particular column by using [Column.AllowSorting](https://help.syncfusion.com/cr/cref_files/wpf/Syncfusion.SfGrid.WPF~Syncfusion.UI.Xaml.Grid.GridColumnBase~AllowSorting.html).

```xml
<syncfusion:SfDataGrid  x:Name="dataGrid" 
                        AllowSorting="True"
                        ItemsSource="{Binding Orders}">
</syncfusion:SfDataGrid>
```
### Programmatic sorting
You can sort a column in programmatic way by using the [DataGrid.SortColumnDescriptions](https://help.syncfusion.com/cr/cref_files/wpf/Syncfusion.SfGrid.WPF~Syncfusion.UI.Xaml.Grid.SfGridBase~SortColumnDescriptions.html) property.

```xml
<syncfusion:SfDataGrid.SortColumnDescriptions>
    <syncfusion:SortColumnDescription ColumnName="OrderID" SortDirection="Ascending" />
    <syncfusion:SortColumnDescription ColumnName="CustomerName" SortDirection="Descending" />
</syncfusion:SfDataGrid.SortColumnDescriptions>
```

### Showing sort order numbers
[WPF DataGrid]((https://www.syncfusion.com/wpf-ui-controls/datagrid) (SfDataGrid) allows you to sort the data against one or more columns by clicking a column header by pressing <kbd>Ctrl</kbd> key. Sorting orders to denote the order of sorting performed for columns can be enabled by using the [DataGrid.ShowSortNumbers](https://help.syncfusion.com/cr/cref_files/wpf/Syncfusion.SfGrid.WPF~Syncfusion.UI.Xaml.Grid.SfGridBase~ShowSortNumbers.html) property.

```xml
<syncfusion:SfDataGrid  x:Name="dataGrid" 
                        AllowSorting="True"
                        ShowSortNumbers="True"
                        ItemsSource="{Binding Orders}">
</syncfusion:SfDataGrid>
```

### Tristate sorting

By default, the data is sorted in ascending or descending order when clicking a column header. Data can be rearranged to its initial order from descending, when clicking column header by setting [SfDataGrid.AllowTriStateSorting](http://help.syncfusion.com/cr/cref_files/wpf/Syncfusion.SfGrid.WPF~Syncfusion.UI.Xaml.Grid.SfGridBase~AllowTriStateSorting.html?_ga=2.197145967.1354036390.1571571849-1942950702.1567054426) property

Following are the sequence of sorting orders when clicking column header,

1. Sorts the data in ascending order
2. Sorts the data in descending order
3. Clears the sorting and records displayed in its initial order
                
```xml
<syncfusion:SfDataGrid  x:Name="dataGrid" 
                        AllowSorting="True"
                        AllowTriStateSorting="True"
                        ItemsSource="{Binding Orders}">
</syncfusion:SfDataGrid>
```

### Custom Sorting
Columns can be sorted based on the custom logic. The custom sorting can be applied by adding the [SortComparer](https://help.syncfusion.com/cr/cref_files/wpf/Syncfusion.Data.WPF~Syncfusion.Data.SortComparer.html?_ga=2.223646427.1354036390.1571571849-1942950702.1567054426) instance to [SfDataGrid.SortComparers](https://help.syncfusion.com/cr/cref_files/wpf/Syncfusion.SfGrid.WPF~Syncfusion.UI.Xaml.Grid.SfDataGrid~SortComparers.html?_ga=2.226483546.1354036390.1571571849-1942950702.1567054426).

You can go through this [user guide](https://help.syncfusion.com/wpf/datagrid/sorting?_ga=2.226483546.1354036390.1571571849-1942950702.1567054426#custom-sorting) to know more about custom sorting.

### Events
You can change the sorting behavior using [SfDataGrid.SortColumnsChanging](https://help.syncfusion.com/cr/cref_files/wpf/Syncfusion.SfGrid.WPF~Syncfusion.UI.Xaml.Grid.SfDataGrid~SortColumnsChanging_EV.html?_ga=2.255784392.1354036390.1571571849-1942950702.1567054426) and [SfDataGrid.SortColumnsChanged](https://help.syncfusion.com/cr/cref_files/wpf/Syncfusion.SfGrid.WPF~Syncfusion.UI.Xaml.Grid.SfDataGrid~SortColumnsChanged_EV.html?_ga=2.255784392.1354036390.1571571849-1942950702.1567054426) event in DataGrid. SortColumnsChanging event occurs while sorting the columns by clicking a column header. SortColumnsChanged event occurs when the sorting is applied to the column.

```c#
dataGrid.SortColumnsChanging += DataGrid_SortColumnsChanging;
private void DataGrid_SortColumnsChanging(object sender, Syncfusion.UI.Xaml.Grid.GridSortColumnsChangingEventArgs e)
{
    // Do your customization here
}

dataGrid.SortColumnsChanged += DataGrid_SortColumnsChanged;
private void DataGrid_SortColumnsChanged(object sender, Syncfusion.UI.Xaml.Grid.GridSortColumnsChangedEventArgs e)
{
    // Do your customization here
}
```

## Requirements to run the demo
Visual Studio 2015 and above versions
