# ns-inputter

## Introduction

Inputters are used to help people enter and select information. Inputters are normally found within forms. There are different types of inputters including text, radio button, checkbox and select (drop-downs).

> A way to communicate with British Gas (that isn't picking up the ☎)  
> A wrapper of native inputs to create a form. There are many types of inputs including text, radio button, checkbox and select.

[What and why details here (2-3 lines)] Use an inputter to capture and validate information from users and inform them why they need to give it.

## Usage

To see examples visit [Storybook](https://nucleus.bgdigital.xyz/demo/index.html?path=/story/ns-inputter--text)

```html
<ns-inputter validation="['isRequired']" helper="So we can send you love letters">
    <label slot="label">First name</label>
    <input type="text">
</ns-inputter>
```

## Component Relationship

* Does it live in a panel? (yes)
  * What layout classes can be used? (Splash)
* Does it live inside other components?
  * ns-inputter components are typically contained within a ns-form
* Atomic type: (molecule)

## Specification

| **Name** | Value |
| :--- | :--- |
| **Description** | The value of the input or group of inputs inside ns-inputter. This can be used to add an intial value |
| **Type** | string |
| **Default** | n/a |
| **Options** | |

| **Name** | Validation |
| :--- | :--- |
| **Description** | A way to assist valid values are added and to show an error message when they're not. |
| **Type** | array |
| **Default** | n/a |
| **Options** | isRequired, isNumber,  isInteger, isPostcode, isFirstName, isLastName, isTitle, isEmail, isPhoneNumber, isMobileNumber, isDateOfBirth, minLength(x), maxLength(x) |
| **Notes** | It is possible to have multiple validations. For example: ["isRequired", "isNumber", "isInteger"] |



### Advanced validation

Some of the validation options can be configured by passing in values within the parentheses:

minLength(x) - Shows error if the input value is less than x chars.

maxLength(x) - Shows error if the input value is greater than x chars.



| **Name** | Execute |
| :--- | :--- |
| **Description** | Executes the validation to check the input's validity |
| **Type** | boolean |
| **Default** | false |
| **Options** | true, false |

| **Name** | Helper |
| :--- | :--- |
| **Description** | A single line of text between the label and input |
| **Type** | string |
| **Default** | n/a |
| **Options** | "" |
| **Notes** | A way to help the user understand why or why not enter information |

| **Name** | LabelID |
| :--- | :--- |
| **Description** | The ID of the element that you'd like as an alternative to the label |
| **Type** | string |
| **Default** | n/a |
| **Options** | "" |
| **Notes** | Always try to use a label or the heading. Only use this if the element and the label are the same. |

| **Name** | Heading |
| :--- | :--- |
| **Description** | This is used instead of a label for grouped inputs such as radio and checkbox. |
| **Type** | string |
| **Default** | n/a |
| **Options** | "" |
| **Notes** | This will generate the `<label>`. Don't use for single `<input>` such as text. |

| **Name** | Anonymous slot |
| :--- | :--- |
| **Description** | This is the place to add the `<label>` and `<input>` html elements |
| **Type** | HTMLElement |
| **Default** | n/a |
| **Options** | "" |
| **Notes** | There's no need to add id/for unless you need to on the `<label>` and `<input>` |

| **Name** | Named slot `tip-details` |
| :--- | :--- |
| **Description** | Additional information that corresponds to the helper |
| **Type** | HTMLElement |
| **Default** | n/a |
| **Options** | "" |
| **Notes** | This requires helper property which is intially hidden and can be revealed by the user when they click on the helper text |

## Best practises

### Headings

| 💚 Do's | 💔 Don'ts |
| :--- | :--- |
| Use to Introduce a set of checkboxes or radio buttons | |
| Use for questions | |
| Use sentence case | |
| Only use text | |
| Punctuate sentences | |

### Labels

| 💚 Do's | 💔 Don'ts |
| :--- | :--- |
| Be concise | Use full stops |
| Use `<label>` element | Add classes to labels |
| Use sentence case | Use as links |
| Only use text | |

### Helper text

| 💚 Do's | 💔 Don'ts |
| :--- | :--- |
| Keep it to one line | Use for error messaging |
| Use it to explain why we need information | Put examples of inputs inside |
| Use it when the reason for asking maybe unclear | |
| Use as a prompt | |

### Tip Detail

| 💚 Do's | 💔 Don'ts |
| :--- | :--- |
| Use to provide additional context to helper text | Repeat helper text |
| Use basic formatting for copy | Add imagery |
| Use as an explanation | Exceed two paragraphs. Link off if necessary |
| Use as a prompt | |

### Placeholder

| 💚 Do's | 💔 Don'ts |
| :--- | :--- |
| Provide example of expected input | Use real data |
| Use 'eg.' before example | Use as an explanation or a prompt |

### Validation

| 💚 Do's | 💔 Don'ts |
| :--- | :--- |
| Use only when required | Use real data |
| Only use to validate the format of the input | Don't used for... |

### Text Input

| 💚 Do's | 💔 Don'ts |
| :--- | :--- |
| Only use our specified text type. (eg. Text, Password, etc) | Use more than one text input within an inputter |
| Use autocomplete attribute | Put anything inside the text input |
| Base width of input on expected length of input | |

### Radio Buttons

| 💚 Do's | 💔 Don'ts |
| :--- | :--- |
| Use a label with each radio button | Use just one |
| Associate  every radio button with it's label using ID & for attributes | |
| Consider using a select for more than 5 | |

Note - Currently we don't have the ability to have radio button side by side

### Checkboxes

| 💚 Do's | 💔 Don'ts |
| :--- | :--- |
| Use only one label with each checkbox | Use as lists |
| Allow user to opt in as opposed to opt out | Don't try and use as a radio button |
| Consider splitting question out for when more than 5 checkboxes are required | |

### Select

| 💚 Do's | 💔 Don'ts |
| :--- | :--- |
| If adding a "Please Select" option then add value="" | |

### Considerations of best practices

* Use defined conventions for common fields
* Use standard examples for placeholder copy
* If you are asking for first and last name within a text input, spell check should be disabled
* Refer to the text input auto complete definitions
* Always try and have a default selected radio button unless....

## Feedback

* Do you have insights or concerns to share? You can raise an issue via [Github bugs](https://github.com/ConnectedHomes/nucleus/issues/new?assignees=&labels=Bug&template=a--bug-report.md&title=[bug]%20[NAME%20OF%20COMPONENET]).
* See all the issues already raised via [Github issues](https://github.com/connectedHomes/nucleus/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+label%3ABug+[NAME%20OF%20COMPONENET])

💩 🎉 🦄 You can also contact the team on Slack on the `product-nucleus` channel!

## Related links
