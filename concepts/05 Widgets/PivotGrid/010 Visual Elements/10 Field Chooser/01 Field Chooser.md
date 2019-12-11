The Field Chooser is a complementary widget integrated in the pivot grid that allows you to manage the displayed data. To invoke the Field Chooser, right-click the row or column header, and choose the "Show Field Chooser" option. Also, the Field Chooser can be invoked by clicking the top-left empty area of the pivot grid.

![DevExtreme PivotGrid FieldChooser](/images/DataGrid/PivotGridFieldChooser.png)

To configure the Field Chooser, use the [fieldChooser](/api-reference/10%20UI%20Widgets/dxPivotGrid/1%20Configuration/fieldChooser '/Documentation/ApiReference/UI_Widgets/dxPivotGrid/Configuration/fieldChooser/') object. It has a number of options, which can be specified:

- [enabled](/api-reference/10%20UI%20Widgets/dxPivotGrid/1%20Configuration/fieldChooser/enabled.md '/Documentation/ApiReference/UI_Widgets/dxPivotGrid/Configuration/fieldChooser/#enabled') &#8212; enables or disables the Field Chooser;
- [layout](/api-reference/10%20UI%20Widgets/dxPivotGrid/1%20Configuration/fieldChooser/layout.md '/Documentation/ApiReference/UI_Widgets/dxPivotGrid/Configuration/fieldChooser/#layout') &#8212; specifies the field chooser layout;
- [width](/api-reference/10%20UI%20Widgets/dxPivotGrid/1%20Configuration/fieldChooser/width.md '/Documentation/ApiReference/UI_Widgets/dxPivotGrid/Configuration/fieldChooser/#width'), [height](/api-reference/10%20UI%20Widgets/dxPivotGrid/1%20Configuration/fieldChooser/height.md '/Documentation/ApiReference/UI_Widgets/dxPivotGrid/Configuration/fieldChooser/#height') &#8212; specifies the field chooser size;
- [title](/api-reference/10%20UI%20Widgets/dxPivotGrid/1%20Configuration/fieldChooser/title.md '/Documentation/ApiReference/UI_Widgets/dxPivotGrid/Configuration/fieldChooser/#title') &#8212; specifies the text to display as a title of the Field Chooser popup window.

Although the Field Chooser is already integrated in **PivotGrid** and can be invoked using the context menu, you can add it as a [separate widget](/api-reference/10%20UI%20Widgets/dxPivotGridFieldChooser '/Documentation/ApiReference/UI_Widgets/dxPivotGridFieldChooser/') on your page. In this case, the Field Chooser will be displayed continuously and will not overlay the pivot grid.

<a href="http://js.devexpress.com/Demos/WidgetsGallery/#demo/data_grid-pivot_grid-field_chooser" class="button orange small fix-width-155" style="margin-right: 20px;" target="_blank">View Demo</a>