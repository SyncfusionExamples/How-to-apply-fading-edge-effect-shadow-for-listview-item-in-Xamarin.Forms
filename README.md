# How to apply fading edge effect (shadow) for listview item in Xamarin.Forms?
This example demonstrates how to apply fading edge effect for the listview item in Xamarin.Forms.

## Sample

```xaml
<Grid>
    <syncfusion:SfListView x:Name="listView" ItemSize="80" ItemSpacing="3"
                    ItemsSource="{Binding ContactsInfo}">
        <syncfusion:SfListView.DataSource>
            <dataSource:DataSource>
                <dataSource:DataSource.SortDescriptors>
                    <dataSource:SortDescriptor PropertyName="ContactName" Direction="Ascending"/>
                </dataSource:DataSource.SortDescriptors>
            </dataSource:DataSource>
        </syncfusion:SfListView.DataSource>

        <syncfusion:SfListView.ItemTemplate>
            <DataTemplate>
                <Grid Padding="2" Margin="2" >
                    <Frame x:Name="frame" HasShadow="True" OutlineColor="Black" CornerRadius="0"
                    Padding="2" Margin="2">
                        <Grid Grid.Column="0"
                                    RowSpacing="1"
                                    Padding="10,0,0,0"
                                    VerticalOptions="Start">
                            <Grid.RowDefinitions>
                                <RowDefinition Height="*" />
                                <RowDefinition Height="*" />
                            </Grid.RowDefinitions>

                            <Label LineBreakMode="NoWrap"
                                Text="{Binding ContactName}"
                                FontAttributes="Bold"
                                HorizontalTextAlignment="Start"
                                VerticalTextAlignment="Center"
                    TextColor="Teal">
                                
                            </Label>
                            . . .
                            . . .
                        </Grid>
                    </Frame>
                </Grid>
            </DataTemplate>
        </syncfusion:SfListView.ItemTemplate>
    </syncfusion:SfListView>
</Grid>
```

See [How to apply fading edge effect (shadow) for listview item in Xamarin.Forms](https://www.syncfusion.com/kb/9489/how-to-apply-fading-edge-effect-shadow-for-listview-item-in-xamarin-forms) for more details.
## <a name="requirements-to-run-the-demo"></a>Requirements to run the demo ##

* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/) or [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/).
* Xamarin add-ons for Visual Studio (available via the Visual Studio installer).

## <a name="troubleshooting"></a>Troubleshooting ##
### Path too long exception
If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.
