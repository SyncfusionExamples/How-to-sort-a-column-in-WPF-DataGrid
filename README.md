# How-to-sort-a-column-in-WPF-DataGrid
This example illustrates how to sort a column in WPF DataGrid using AllowSorting property.

```xml
        <syncfusion:SfDataGrid  x:Name="dataGrid" AllowSorting="False" ItemsSource="{Binding Orders}">
            <syncfusion:SfDataGrid.Columns>
                <syncfusion:GridTextColumn MappingName="OrderID" />
                <syncfusion:GridTextColumn MappingName="CustomerID" AllowSorting="True"/>
                <syncfusion:GridTextColumn MappingName="CustomerName" AllowSorting="True"/>
                <syncfusion:GridTextColumn MappingName="Country"/>
                <syncfusion:GridTextColumn MappingName="ShipCity" AllowSorting="True"/>
            </syncfusion:SfDataGrid.Columns>
        </syncfusion:SfDataGrid>
```
## Requirements to run the demo
Visual Studio 2015 and above versions
