---
title: Select
description: Form component used for selecting a value from a large list of options, with autocomplete support. 
---

<script setup>
import * as examples from '../examples';
</script>


# Select
## Form component used for selecting a value from a large list of options, with autocomplete support

### Basic Example
The most basic use case for a select component is to have all the select options predefined using the `options` property. This component allows you to easily choose from a set of values and display a computed option label of your choice.

Here are some considerations to be made:
- Each option must be an Object `{}`
- Each option must have a unique identifier field, such as `id`
- The `selected` value will be the option itself

<example :component="examples.ISelectBasicExample" :html="examples.ISelectBasicExampleHTML" :js="examples.ISelectBasicExampleJS"></example>

### Disabled State
Setting the `disabled` property will disable all interactions with the select component.

<example :component="examples.ISelectDisabledExample" :html="examples.ISelectDisabledExampleHTML" :js="examples.ISelectDisabledExampleJS"></example>

You can also disable individual options by setting the option's `disabled` field to `true`.

<example :component="examples.ISelectDisabledOptionExample" :html="examples.ISelectDisabledOptionExampleHTML" :js="examples.ISelectDisabledOptionExampleJS"></example>

### Readonly State
Setting the `readonly` property will disable all interactions with the select component, except being able to focus the select.

<example :component="examples.ISelectReadonlyExample" :html="examples.ISelectReadonlyExampleHTML" :js="examples.ISelectReadonlyExampleJS"></example>

### Clearable Variant
If you need to be able to quickly clear the value of an select, you can add the `clearable` property to the select component.

<example :component="examples.ISelectClearableExample" :html="examples.ISelectClearableExampleHTML" :js="examples.ISelectClearableExampleJS"></example>

### Prefix and Suffix
Inkline allows you to easily add a prefix or suffix to your select. Using prefixes and suffixes you can, for example, indicate 
your select type using an icon or text. 

<example :component="examples.ISelectPrefixSuffixExample" :html="examples.ISelectPrefixSuffixExampleHTML" :js="examples.ISelectPrefixSuffixExampleJS"></example>

### Prepend and Append
You can add additional content such as select fields, buttons or plain text, to either side of the select by using the prepend and append slots.

<example :component="examples.ISelectPrependAppendTextExample" :html="examples.ISelectPrependAppendTextExampleHTML" :js="examples.ISelectPrependAppendTextExampleJS"></example>

<example :component="examples.ISelectPrependAppendButtonExample" :html="examples.ISelectPrependAppendButtonExampleHTML" :js="examples.ISelectPrependAppendButtonExampleJS"></example>

### Colors
You can use the `color` property to set a `light` or `dark` color for your select.

<example :component="examples.ISelectColorVariantsExample" :html="examples.ISelectColorVariantsExampleHTML" :js="examples.ISelectColorVariantsExampleJS"></example>

### Sizes
You're able to use the `size` modifier to control the size of your select, using one of the available sizes: `sm`, `md`, and `lg`. The default size is set to `md`.

<example :component="examples.ISelectSizeVariantsExample" :html="examples.ISelectSizeVariantsExampleHTML" :js="examples.ISelectSizeVariantsExampleJS"></example>

### Header and Footer

### Custom Label

### Autocomplete
Autocomplete functionality can be enabled using the `autocomplete` property. There are some considerations to be made when using autocomplete:
- Search functionality is handled externally, using the `@search` event
- You must provide a loading state using the `loading` property, if done asynchronously
- You must update the available `options` array manually

<example :component="examples.ISelectAutocompleteExample" :html="examples.ISelectAutocompleteExampleHTML" :js="examples.ISelectAutocompleteExampleJS"></example>

### Infinite Scrolling
There are some considerations to be made when using infinite scrolling:
- Pagination functionality is handled externally, using the `@pagination` event
- You must provide a total number of options using the `total` property
- You must provide a loading state using the `loading` property
- You must update the available `options` array manually

### Complex Example
The select component provides support for more complex scenarios as well, such as combining asynchronous search with infinite scrolling pagination. 

Here you can see an example using asynchronous autocomplete and infinite scrolling pagination:

<example :component="examples.ISelectComplexExample" :html="examples.ISelectComplexExampleHTML" :js="examples.ISelectComplexExampleJS"></example>





