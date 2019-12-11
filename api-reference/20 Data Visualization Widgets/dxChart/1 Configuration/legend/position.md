---
default: 'outside'
acceptValues: 'outside' | 'inside'
type: String
---
---
##### shortDescription
Specifies whether the legend is located outside or inside the chart's plot.

---
In addition to this option, use the legend's [horizontalAlignment](/api-reference/20%20Data%20Visualization%20Widgets/BaseChart/1%20Configuration/legend/horizontalAlignment.md '/Documentation/ApiReference/Data_Visualization_Widgets/dxChart/Configuration/legend/#horizontalAlignment'), [verticalAlignment](/api-reference/20%20Data%20Visualization%20Widgets/BaseChart/1%20Configuration/legend/verticalAlignment.md '/Documentation/ApiReference/Data_Visualization_Widgets/dxChart/Configuration/legend/#verticalAlignment') and [orientation](/api-reference/20%20Data%20Visualization%20Widgets/BaseChart/1%20Configuration/legend/orientation.md '/Documentation/ApiReference/Data_Visualization_Widgets/dxChart/Configuration/legend/#orientation') options to specify the legend layout.

When configuring the widget using [ASP.NET MVC Wrappers](/concepts/35%20ASP.NET%20MVC%20Wrappers/20%20Fundamentals '/Documentation/Guide/ASP.NET_MVC_Wrappers/Fundamentals/'), specify this option using the `RelativePosition` enum. This enum accepts the following values: `Inside` and `Outside`.