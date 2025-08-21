# How to apply a style to the listview item in Xamarin.Forms
This example demonstrates how to apply style to the listview item in Xamarin.Forms platform by using the style.

## Sample

```xaml
    <ContentPage.Resources>
        <ResourceDictionary>
            <Style x:Key="StackStyle" TargetType="StackLayout">
                <Setter Property="BackgroundColor" Value="#4b69a0"/>
            </Style>
            <Style x:Key="LabelStyle" TargetType="Label">
                <Setter Property="TextColor" Value="YellowGreen"/>
                <Setter Property="FontAttributes" Value="Italic" />
            </Style>
        </ResourceDictionary>
    </ContentPage.Resources>
   <Grid>
    <syncfusion:SfListView x:Name="listView" ItemSize="70" 
                        ItemsSource="{Binding contactsinfo}">
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
                <Grid x:Name="grid" RowSpacing="1">
                      <Grid.RowDefinitions>
                          <RowDefinition Height="*" />
                          <RowDefinition Height="1" />
                      </Grid.RowDefinitions>
                      . . .
                      . . .
                      <Label LineBreakMode="NoWrap"
                             Style="{StaticResource LabelStyle}"
                             Text="{Binding ContactName}"/>
                      <Label Grid.Row="1"
                             Grid.Column="0"
                             Style="{StaticResource LabelStyle}"
                             Text="{Binding ContactNumber}"/>
                </Grid>
                  . . .
                  . . .
            </Grid>
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
