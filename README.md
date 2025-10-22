
# rounded-corner-expander-xamarin

In this article, we demonstrate how to create an Expander with rounded corners in Xamarin.Forms using Syncfusion's SfExpander control. The sample showcases custom header and content styling, rounded corners, and dynamic icon changes based on expansion state. The implementation leverages PancakeView for advanced UI effects and value converters for dynamic properties.

To learn more about these features, check out the official user guide:
- [Getting Started with Xamarin Expander (SfExpander)](https://help.syncfusion.com/xamarin/expander/getting-started)

**KB Link:** **[View document in Syncfusion Xamarin Knowledge base](https://www.syncfusion.com/kb/12315/how-to-add-rounded-corners-for-xamarin-forms-expander-sfexpander)**

## xaml
```
<syncfusion:SfExpander x:Name="expander1" HeaderIconPosition="None">
    <syncfusion:SfExpander.Header>
        <pancake:PancakeView CornerRadius="{Binding IsExpanded, Source={x:Reference expander1}, Converter={StaticResource CornerRadiusConverter}}" BackgroundColor="#bbbfca" HeightRequest="50">
            <Grid>
                <Label Text="Veg Pizza" TextColor="#495F6E" VerticalTextAlignment="Center" Margin="10,0,0,0"/>
                <Image Margin="10" HorizontalOptions="End" HeightRequest="20" WidthRequest="20" Source="{Binding IsExpanded,Source={x:Reference expander1},Converter={StaticResource ExpanderIconConverter}}"/>
            </Grid>
        </pancake:PancakeView>
    </syncfusion:SfExpander.Header>
    <syncfusion:SfExpander.Content>
        <pancake:PancakeView CornerRadius="0,0,20,20" BackgroundColor="#dddddd" >
            <Grid Padding="10,10,10,10" >
                <Label HeightRequest="50" Text="Veg pizza is prepared with the items that meet vegetarian standards by not including any meat or animal tissue products." TextColor="#303030" VerticalTextAlignment="Center"/>
            </Grid>
        </pancake:PancakeView>
    </syncfusion:SfExpander.Content>
</syncfusion:SfExpander>

<syncfusion:SfExpander x:Name="expander2" HeaderIconPosition="None">
    <syncfusion:SfExpander.Header>
        <pancake:PancakeView CornerRadius="{Binding Path=IsExpanded, Source={x:Reference expander2}, Converter={StaticResource CornerRadiusConverter}}" BackgroundColor="#bbbfca" HeightRequest="50">
            <Grid>
                <Label Text="Non-veg Pizza" TextColor="#495F6E" VerticalTextAlignment="Center" Margin="10,0,0,0"/>
                <Image Margin="10" HorizontalOptions="End" HeightRequest="20" WidthRequest="20" Source="{Binding IsExpanded, Source={x:Reference expander2},Converter={StaticResource ExpanderIconConverter}}"/>
            </Grid>
        </pancake:PancakeView>
    </syncfusion:SfExpander.Header>
    <syncfusion:SfExpander.Content>
        <pancake:PancakeView CornerRadius="0,0,20,20" BackgroundColor="#dddddd" >
            <Grid Padding="10,10,10,10">
                <Label Text="Non-veg pizza is prepared by including the meat and animal tissue products." HeightRequest="50" TextColor="#303030" VerticalTextAlignment="Center"/>
            </Grid>
        </pancake:PancakeView>
    </syncfusion:SfExpander.Content>
</syncfusion:SfExpander>
```

## How it works
- **Rounded corners:** PancakeView is used to provide rounded corners for both the header and content of the Expander. The CornerRadius is dynamically set using a value converter based on the expansion state.
- **Custom header and icon:** The header includes a label and an icon that changes depending on whether the Expander is expanded or collapsed. This is achieved using ExpanderIconConverter and data binding to the IsExpanded property.
- **Content styling:** The content area uses PancakeView for rounded corners and a distinct background color, enhancing the visual separation between header and content.
- **Multiple expanders:** The sample demonstrates two expanders (Veg Pizza and Non-veg Pizza), each with its own header, icon, and content, showing how to reuse the same pattern for different sections.

##### Conclusion
 
I hope you enjoyed learning about how to to add rounded corners for Xamarin.Forms Expander (SfExpander).
 
You can refer to our [.NET MAUI DataGrid’s feature tour](https://www.syncfusion.com/maui-controls/maui-datagrid) page to learn about its other groundbreaking feature representations. You can also explore our [.NET MAUI DataGrid Documentation](https://help.syncfusion.com/maui/datagrid/getting-started) to understand how to present and manipulate data. 
For current customers, you can check out our .NET MAUI components on the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/maui) to explore our .NET MAUI DataGrid and other .NET MAUI components.
 
If you have any queries or require clarifications, please let us know in the comments below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [Direct-Trac](https://support.syncfusion.com/create) or [feedback portal](https://www.syncfusion.com/feedback/maui?control=sfdatagrid), or the feedback portal. We are always happy to assist you!
