![DevExtreme ChartJS AvailableFormats](/images/ChartJS/AvailableFormats_NumericFormats.png)

[note]Formats from the left column can be paired with formats from the right column using a space separator, e.g., *'fixedPoint thousands'*.

To set a numeric format, use the **format** | [type](/api-reference/50%20Common/Object%20Structures/format/type.md '/Documentation/ApiReference/Common/Object_Structures/format/#type') option. Also, you can apply a precision to numeric values using the **format** | [precision](/api-reference/50%20Common/Object%20Structures/format/precision.md '/Documentation/ApiReference/Common/Object_Structures/format/#precision') option. For example, the following configuration makes **Chart**'s [series point labels](/concepts/05%20Widgets/Chart/10%20Visual%20Elements/030%20Series%20Point%20Labels.md '/Documentation/Guide/Widgets/Chart/Visual_Elements/#Series_Point_Labels') display values rounded up to the nearest hundredth.

    <!--JavaScript-->var data = [
        { quarter: 'QI', quantity: 26.252 },
        { quarter: 'QII', quantity: 26.5 },
        { quarter: 'QIII', quantity: 26.375 },
        { quarter: 'QIV', quantity: 25.75 }
    ];
    
    var chartOptions = {
		dataSource: data,
		series: {
			// ...
			label: {
                // ...
				format: {
                    type: 'fixedPoint',
                    precision: 2
                }
			}
		}
	};
    
![DevExpress HTML5 DataVisualizationWidgets Chart Format Precision](/images/ChartJS/Format_Precision.png)

The **format** option also accepts strings. Use this capability as a shortcut for specifying a predefined format.

    <!--JavaScript-->var widgetOptions = {
        // ...
        customizableElement: {
            format: 'fixedPoint'
        }
    };
    
Alternatively, you can use a native formatter of the Globalize library. In this case, the **format** option accepts an object whose fields are the same as the options passed to the [numberFormatter](https://github.com/jquery/globalize/blob/master/doc/api/number/number-formatter.md).

    <!--JavaScript-->var widgetOptions = {
        // ...
        customizableElement: {
            format: {
                // ...
                minimumIntegerDigits: 1
            }
        }
    };

Note that you must not set the **type** option if you use a Globalize formatter. Also, this approach might require additional [CLDR modules](https://github.com/jquery/globalize/blob/master/README.md#2-cldr-content) not shipped with the DevExtreme package.