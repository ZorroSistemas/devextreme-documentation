If none of the available editors suit your requirements, you can define a custom one or even place anything you find useful instead. For this purpose, implement a custom template and pass it to the [template](/api-reference/10%20UI%20Widgets/dxForm/5%20Item%20Types/SimpleItem/template.md '/Documentation/ApiReference/UI_Widgets/dxForm/Item_Types/SimpleItem/#template') option.

    <!--JavaScript-->
    $(function() {
        $("#formContainer").dxForm({
            formData: {
                name: "John Heart",
                picture: "https://js.devexpress.com/Content/images/doc/16_2/PhoneJS/person2.png"
            },
            items: [ "name", {
                dataField: "picture",
                template: function (data, itemElement) {
                    itemElement.append("<img src='" + data.editorOptions.value + "'>");
                }
            }]
        });
    });

A simple item can be accompanied by a line of text that gives a hint, for example, of the values that this item accepts. To specify this text, use the [helpText](/api-reference/10%20UI%20Widgets/dxForm/5%20Item%20Types/SimpleItem/helpText.md '/Documentation/ApiReference/UI_Widgets/dxForm/Item_Types/SimpleItem/#helpText') option. If filling an item is required, assign *true* to its [isRequired](/api-reference/10%20UI%20Widgets/dxForm/5%20Item%20Types/SimpleItem/isRequired.md '/Documentation/ApiReference/UI_Widgets/dxForm/Item_Types/SimpleItem/#isRequired') option. In this case, a special mark appears near the item. For more information, see the [Additional Marks](/concepts/05%20Widgets/Form/15%20Configure%20Item%20Labels/10%20Additional%20Marks.md '/Documentation/Guide/Widgets/Form/Configure_Item_Labels/Additional_Marks/') topic.

    <!--JavaScript-->
    $(function() {
        $("#formContainer").dxForm({
            formData: {
                name: "John Heart",
                phone: "+1(360)684-1334"
            },
            items: [{ 
                dataField: "name",
                isRequired: true
            }, {
                dataField: "phone",
                helpText: "Example: +1(111)111-1111"
            }]
        });
    });

You can modify automatically generated items using the [customizeItem](/api-reference/10%20UI%20Widgets/dxForm/1%20Configuration/customizeItem.md '/Documentation/ApiReference/UI_Widgets/dxForm/Configuration/#customizeItem') function. This function is called for each item before it is rendered. To access the item, use the function's parameter. Its structure mirrors the [Simple Item](/api-reference/10%20UI%20Widgets/dxForm/5%20Item%20Types/SimpleItem '/Documentation/ApiReference/UI_Widgets/dxForm/Item_Types/SimpleItem/') structure, therefore, you can modify any option available for a simple item.

    <!--JavaScript-->
    $(function() {
        $("#formContainer").dxForm({
            formData: {
                firstName: "John",
                lastName: "Heart",
                email: "jheart@dx-email.com",
                phone: "+1(213) 555-9392"
            },
            customizeItem: function (item) {
                if (item.itemType == "simple") {
                    item.label = {
                        location: "top"
                    };
                    if (item.dataField === "email" || item.dataField === "phone") {
                        item.colSpan = 3;
                    }
                    if (item.dataField === "phone") {
                        item.helpText = "Example: +1 (111) 111-1111";
                    }
                }
            }
        });
    });

[note]The **customizeItem** function is called for each item including [group](/api-reference/10%20UI%20Widgets/dxForm/5%20Item%20Types/GroupItem '/Documentation/ApiReference/UI_Widgets/dxForm/Item_Types/GroupItem/'), [tabbed](/api-reference/10%20UI%20Widgets/dxForm/5%20Item%20Types/TabbedItem '/Documentation/ApiReference/UI_Widgets/dxForm/Item_Types/TabbedItem/') and [empty](/api-reference/10%20UI%20Widgets/dxForm/5%20Item%20Types/EmptyItem '/Documentation/ApiReference/UI_Widgets/dxForm/Item_Types/EmptyItem/') items, although such items can be declared only in the [items](/api-reference/10%20UI%20Widgets/dxForm/1%20Configuration/items.md '/Documentation/ApiReference/UI_Widgets/dxForm/Configuration/#items') array, and there is no need to customize them afterwards. Therefore, we recommend you to check the [itemType](/api-reference/10%20UI%20Widgets/dxForm/5%20Item%20Types/SimpleItem/itemType.md '/Documentation/ApiReference/UI_Widgets/dxForm/Item_Types/SimpleItem/#itemType') option to ensure that the item you are going to customize is indeed a simple item.

#####See Also#####
- [Form - Organize Simple Items in Groups](/concepts/05%20Widgets/Form/10%20Organize%20Simple%20Items/05%20In%20Groups '/Documentation/Guide/Widgets/Form/Organize_Simple_Items/In_Groups/')
- [Form - Organize Simple Items in Tabs](/concepts/05%20Widgets/Form/10%20Organize%20Simple%20Items/10%20In%20Tabs '/Documentation/Guide/Widgets/Form/Organize_Simple_Items/In_Tabs/')
- [Form - Organize Simple Items in Columns](/concepts/05%20Widgets/Form/10%20Organize%20Simple%20Items/15%20In%20Columns '/Documentation/Guide/Widgets/Form/Organize_Simple_Items/In_Columns/')
- [Form - Add an Empty Space Between Simple Items](/concepts/05%20Widgets/Form/10%20Organize%20Simple%20Items/20%20Add%20an%20Empty%20Space.md '/Documentation/Guide/Widgets/Form/Organize_Simple_Items/Add_an_Empty_Space/')
- [Form - Configure Item Labels](/concepts/05%20Widgets/Form/15%20Configure%20Item%20Labels/05%20Location%20and%20Alignment '/Documentation/Guide/Widgets/Form/Configure_Item_Labels/Location_and_Alignment/')
- [Form Demos](https://js.devexpress.com/Demos/WidgetsGallery/#demo/forms_and_multi-purpose-form-customize_item)
- [Form API Reference](/api-reference/10%20UI%20Widgets/dxForm '/Documentation/ApiReference/UI_Widgets/dxForm/')