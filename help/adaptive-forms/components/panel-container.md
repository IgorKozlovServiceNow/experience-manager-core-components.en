---
title: Adaptive Forms Core Component - Panel container
description: Using or customizing the Adaptive Forms Panel container Core Component.
role: Architect, Developer, Admin, User
exl-id: 104836fe-8325-47de-978d-1ff2d6a9dd15
---
# Panel container {#panel-container-adaptive-forms-core-component}

In an Adaptive Form, a panel is a container element that can be used to group together related form elements. It allows you to group and organize different form elements in a logical and meaningful way. This can help to improve the overall structure and readability of the form, making it easier for users to understand and navigate. 

Panels can also be used to create collapsible sections, which can be useful for hiding complex or less frequently used form fields, thus keeping the form simple and easy to use. It also allows you to include other components like text, checkbox, button, etc.

It also can be used to set different rule based actions like submitting form, opening a website, show/hide components, or add an instance of a panel. 

**Example**

![](/help/adaptive-forms/assets/panel-container.png)

## Usage {#reasons-to-use-panel-container}

There are several reasons to use a panel in a form, including:

- **Organizing form elements**: A panel can be used to group related form elements together, making it easier for users to understand and navigate the form.

- **Improving form structure**: By grouping form elements into panels, it can improve the overall structure and readability of the form, making it easier to understand.

- **Creating collapsible sections**: Panels can be used to create collapsible sections, which can be useful for hiding complex or less frequently used form fields, thus keeping the form simple and easy to use.

- **Enhancing usability**: By using panels to organize form elements, it can make the form more user-friendly and easier to use, which can lead to higher completion rates.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Panel Container Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|||
|---|---|
|Component Version|AEM as a Cloud Service|
|--- |--- |
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Panel Container Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your panel container experience for visitors with the Configure Dialog. You can also define panel container options with ease for a seamless user experience.

### Basic Tab {#basic-tab} 

![Basic tab](/help/adaptive-forms/assets/basic-panel.png)

- **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

- **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.

- **Hide Title** - Select the option to hide the component's Title.

- **Group child components' data on form submission(Wrap data in object)** - When the option is selected, the data from its child components is nested within the parent component's JSON object. However, if the option is not selected, the submitted JSON data has a flat structure, with no object for the parent component. For example: 

    - When the option is selected, the data from the child components (for example, Street, City, and Zip Code) is nested within the parent component (Address) as a JSON object. This creates a hierarchical structure, and the data is organized under the parent component.
    
        Structure of submitted data:

         ```JSON 
    
         { "Address":

         { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }

         }
    
         ```

    - When the option is not selected, the submitted JSON data has a flat structure with no object for the parent component (Address). All data is at the same level, without any hierarchical organization.

        
        Structure of submitted data:

         ```JSON 
    
            { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
    
         ```

- **Layout** - You can have either a fixed layout (Simple) or a flexible layout (Responsive Grid) for your wizard. The Simple layout keeps everything fixed in the place, while the Responsive Grid allows you to adjust the position of components to suit your needs. For example, use Responsive Grid to align "First Name", "Middle Name" and "Last Name" in a form in a single row. 

- **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enables you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.
- **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 
- **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

### Repeat Panel Tab {#repeat-panel}

![repeat tab](/help/adaptive-forms/assets/repeat-panel.png)

You can use the repeatibility options to duplicate panel container and its child components, define a minimum and maximum repetition count, and facilitates the replication of similar sections within a form. When interacting with the panel container component and accessing its settings, the following options are presented:

- **Make Wizard repeatable**: A toggle feature that allows users to enable or disable the repeatability functionality.
- **Minimum repetitions**: Establishes the minimum number of times the panel container can be repeated. A value of zero indicates that the Wizard panel is not repeated; the default value is zero.
- **Maximum repetitions**: Sets the maximum number of times the panel container can be repeated. By default, this value is unlimited.

To effectively manage repeatable sections within the panel container, follow the steps provided in the [Creating forms with repeatable sections](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html) article.

### Help Content Tab {#help-content}

![Help Content tab](/help/adaptive-forms/assets/helpcontent-panel.png)


- **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

- **Always show short description** - Enable the option to display the Short description below the component.

- **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab {#accessibility}
 
![Accessibility tab](/help/adaptive-forms/assets/accessibilty-panel.png)


- **Text for screen readers** - Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

- **HTML role for screen reader to announce** - The HTML role is an attribute used to specify the purpose of an HTML element to assistive technologies such as screen readers. The role attribute is used to provide additional context and semantic meaning to an element, making it easier for screen readers to interpret and announce the content to the user. For example, in AEM Forms, a form field's label might have the role of "label," and its input field might have the role of "textbox." This helps the screen reader understand the relationship between the label and input field, and correctly announce them to the user.

## Related article {#related-article}

- [Create an Adaptive Form in AEM Sites Page or Experience Fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)

- [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)


## See Also {#see-also}

- [Accordion](/help/adaptive-forms/components/accordion.md)
- [Button](/help/adaptive-forms/components/button.md)
- [Check Box Group](/help/adaptive-forms/components/checkbox-group.md)
- [Date Picker](/help/adaptive-forms/components/date-picker.md)
- [Drop-down list](/help/adaptive-forms/components/drop-down.md)
- [Email-input](/help/adaptive-forms/components/email-input.md)
- [Form Container](/help/adaptive-forms/components/form-container.md)
- [File Attachment](/help/adaptive-forms/components/file-attachment.md)
- [Footer](/help/adaptive-forms/components/footer.md)
- [Header](/help/adaptive-forms/components/header.md)
- [Horizontal Tabs](/help/adaptive-forms/components/horizontal-tabs.md)
- [Image](/help/adaptive-forms/components/image.md)
- [Number Input](/help/adaptive-forms/components/number-input.md)
- [Radio Button](/help/adaptive-forms/components/radio-button.md)
- [Reset Button](/help/adaptive-forms/components/reset-button.md)
- [Submit Button](/help/adaptive-forms/components/submit-button.md)
- [Telephone input](/help/adaptive-forms/components/telephone-input.md)
- [Text Input](/help/adaptive-forms/components/text-input.md)
- [Text](/help/adaptive-forms/components/text.md)
- [Title](/help/adaptive-forms/components/title.md)
- [Wizard](/help/adaptive-forms/components/wizard.md)
