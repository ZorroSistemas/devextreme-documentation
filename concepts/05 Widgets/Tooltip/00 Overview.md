The **Tooltip** widget displays a tooltip for a specified element on the page.

<a href="https://js.devexpress.com/Demos/WidgetsGallery/#demo/dialogs_and_notifications-tooltip-overview" class="button orange small fix-width-155" style="margin-right: 20px;" target="_blank">View Demo</a>

The following code creates a simple **Tooltip** on your page and attaches it to another element (in this example, to an image).

    <!--HTML--><img id="image" src="https://www.devexpress.com/DXR.axd?r=9999_17-FD0Id" />
    <div id="tooltipContainer">
        <p>Tooltip content</p>
    </div>

<!---->

    <!--JavaScript-->$(function() {
        $("#tooltipContainer").dxTooltip({
    		target: "#image",
            showEvent: 'dxhoverstart',
            hideEvent: 'dxhoverend'
        });
    });

#####See Also#####
- [Widget Basics - jQuery](/concepts/00%20Getting%20Started/10%20Widget%20Basics%20-%20jQuery '/Documentation/Guide/Getting_Started/Widget_Basics_-_jQuery/')
- [Widget Basics - AngularJS](/concepts/00%20Getting%20Started/20%20Widget%20Basics%20-%20AngularJS '/Documentation/Guide/Getting_Started/Widget_Basics_-_AngularJS/')
- [Widget Basics - Knockout](/concepts/00%20Getting%20Started/25%20Widget%20Basics%20-%20Knockout '/Documentation/Guide/Getting_Started/Widget_Basics_-_Knockout/')
- [Tooltip - Show and Hide](/concepts/05%20Widgets/Tooltip/05%20Show%20and%20Hide%20the%20Tooltip '/Documentation/Guide/Widgets/Tooltip/Show_and_Hide_the_Tooltip/')
- [Tooltip - Customize the Content](/concepts/05%20Widgets/Tooltip/10%20Customize%20the%20Content.md '/Documentation/Guide/Widgets/Tooltip/Customize_the_Content/')
- [Tooltip - Resize and Relocate](/concepts/05%20Widgets/Tooltip/15%20Resize%20and%20Relocate.md '/Documentation//Guide/Widgets/Tooltip/Resize_and_Relocate/')
- [Tooltip API Reference](/api-reference/10%20UI%20Widgets/dxTooltip '/Documentation/ApiReference/UI_Widgets/dxTooltip/')

[tags]tooltip, overview, overlay