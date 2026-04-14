# Learn easy way to consume ASP.NET Core Web API in Xamarin application

This sample demonstrates the easy steps to consume the [ASP.Net Core Web API](https:\ej2services.syncfusion.com\production\web-services\api\Orders) service in Syncfusion Xamarin.Forms [ListView](https://help.syncfusion.com/xamarin/sflistview/getting-started).

## Sample

```xaml
    <Grid>
        <Grid.RowDefinitions>
            <RowDefinition Height="50"/>
            <RowDefinition Height="*"/>
        </Grid.RowDefinitions>
        <Label Text="Load data from web Api" BackgroundColor="SlateBlue" FontSize="18" FontAttributes="Bold" TextColor="White" VerticalTextAlignment="Center" HorizontalTextAlignment="Center"/>
        <syncfusion:SfListView x:Name="listView" ItemSize="90" ItemSpacing="5" Grid.Row="1"
                               BackgroundColor="AliceBlue" ItemsSource="{Binding Items}">
            <syncfusion:SfListView.ItemTemplate>
                <DataTemplate>
                    <Frame BorderColor="#757575" Padding="5">
                        <Grid>
                            <Grid.ColumnDefinitions>
                                <ColumnDefinition Width="*"/>
                                <ColumnDefinition Width="*"/>
                            </Grid.ColumnDefinitions>
                            <Grid.RowDefinitions>
                                <RowDefinition Height="Auto"/>
                                <RowDefinition Height="Auto"/>
                                <RowDefinition Height="Auto"/>
                            </Grid.RowDefinitions>
                            <Label Grid.Row="0" Grid.Column="0" Text="Order ID  " HorizontalOptions="Start" TextColor="Black" FontSize="16" FontAttributes="Bold"/>
                            <Label Grid.Row="1" Grid.Column="0" Text="Customer ID  " HorizontalOptions="Start" TextColor="Black" FontSize="16" FontAttributes="Bold"/>
                            <Label Grid.Row="2" Grid.Column="0" Text="Ship Country  " HorizontalOptions="Start" TextColor="Black" FontSize="16" FontAttributes="Bold"/>

                            <Label Grid.Row="0" Grid.Column="1" Text="{Binding OrderID}" HorizontalOptions="Start" TextColor="Black" FontSize="16" WidthRequest="100"/>
                            <Label Grid.Row="1" Grid.Column="1" Text="{Binding CustomerID}" HorizontalOptions="Start" TextColor="Black" WidthRequest="100"/>
                            <Label Grid.Row="2" Grid.Column="1" Text="{Binding ShipCountry}" HorizontalOptions="Start" TextColor="Black" WidthRequest="100"/>
                        </Grid>
                    </Frame>
                </DataTemplate>
            </syncfusion:SfListView.ItemTemplate>
        </syncfusion:SfListView>
    </Grid>
```

## Requirements to run the demo

* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/) or [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/)
* Xamarin add-ons for Visual Studio (available via the Visual Studio installer).

## Troubleshooting

### Path too long exception

If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.
