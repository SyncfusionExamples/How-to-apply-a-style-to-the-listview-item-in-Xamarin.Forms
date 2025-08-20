# How to apply a style to the listview item in Xamarin.Forms
This example demonstrates how to apply style to the listview item in Xamarin.Forms platform by using the style.

## Sample

```xaml
<Grid>
    <syncfusion:SfListView x:Name="listView" ItemSize="70" 
                        ItemsSource="{Binding contactsinfo}" ItemSpacing="0,0,5,0" >
        <syncfusion:SfListView.DataSource>
            <dataSource:DataSource>
                <dataSource:DataSource.GroupDescriptors>
                    <dataSource:GroupDescriptor PropertyName="DisplayString"/>
                </dataSource:DataSource.GroupDescriptors>
            </dataSource:DataSource>
        </syncfusion:SfListView.DataSource>
        <syncfusion:SfListView.GroupHeaderTemplate>
            <DataTemplate>
                <ViewCell>
                    <ViewCell.View>
                        <StackLayout Style="{StaticResource StackStyle}">
                            <Label Text="{Binding Key}" TextColor="White" />
                        </StackLayout>
                    </ViewCell.View>
                </ViewCell>
            </DataTemplate>
        </syncfusion:SfListView.GroupHeaderTemplate>
        <syncfusion:SfListView.ItemTemplate>
            <DataTemplate>
                <ViewCell>
                    <ViewCell.View>
                        <Grid x:Name="grid" RowSpacing="1">

                            <Grid.RowDefinitions>
                                <RowDefinition Height="*" />
                                <RowDefinition Height="1" />
                            </Grid.RowDefinitions>
                            <Grid RowSpacing="1">
                                <Grid.ColumnDefinitions>
                                    <ColumnDefinition Width="50" />
                                    <ColumnDefinition Width="*" />
                                    <ColumnDefinition Width="70" />
                                </Grid.ColumnDefinitions>

                                <Grid>
                                    <Image Source="{Binding ContactImage}"
                                            VerticalOptions="Center"
                                            HorizontalOptions="Center"
                                            HeightRequest="50"/>

                                </Grid>

                                <Grid Grid.Column="1"
                                        RowSpacing="1"
                                        Padding="10,0,0,0"
                                        VerticalOptions="Center">
                                    <Grid.RowDefinitions>
                                        <RowDefinition Height="*" />
                                        <RowDefinition Height="*" />
                                    </Grid.RowDefinitions>

                                    <Label LineBreakMode="NoWrap" Style="{StaticResource LabelStyle}"
                                            Text="{Binding ContactName}">
                                    </Label>
                                    <Label Grid.Row="1"
                                            Grid.Column="0"
                                            LineBreakMode="NoWrap"
                                            Style="{StaticResource LabelStyle}"
                                            Text="{Binding ContactNumber}">
                                    </Label>
                                </Grid>
                            </Grid>
                            <StackLayout Grid.Row="1" BackgroundColor="Gray" HeightRequest="1"/>
                        </Grid>
                    </ViewCell.View>
                </ViewCell>
            </DataTemplate>
        </syncfusion:SfListView.ItemTemplate>
    </syncfusion:SfListView>
</Grid>
```

See [How to apply a style to the listview item in Xamarin.Forms](https://www.syncfusion.com/kb/9641/how-to-apply-a-style-to-the-listview-item-in-xamarin-forms) for more details.
## <a name="requirements-to-run-the-demo"></a>Requirements to run the demo ##

* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/) or [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/).
* Xamarin add-ons for Visual Studio (available via the Visual Studio installer).

## <a name="troubleshooting"></a>Troubleshooting ##
### Path too long exception
If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.
