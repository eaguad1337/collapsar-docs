---
weight: 100
title: "Text Input"
description: ""
icon: "article"
date: "2023-10-15T15:13:44-03:00"
lastmod: "2023-10-15T15:13:44-03:00"
draft: false
toc: true
---

## Overview
Use `TextInput` to control text fields.


```python
from collapsar.fields.TextInput import TextInput

TextInput('Name')
```

### Make field

Collapsar will assume the field if you pass only pass 1 parameter. You can define the label and field name this way:

```python
from collapsar.fields.TextInput import TextInput

TextInput('Name', 'name_field')
```

### Computed values

You may use provide a function if you want to render a custom value.

```python
from collapsar.fields.TextInput import TextInput

TextInput('Full name', lambda model: f'{model.name} {model.last_name}')
```

{{<alert context="info" text="Computed values cannot be edited and won't be shown on the creation form."/>}}

## Validation

Use `numeric` to define a string as numeric.

```python
from collapsar.fields.TextInput import TextInput

TextInput('Phone').numeric()
```

### max

Use `max` to set the maxlength value for a string.

```python
from collapsar.fields.TextInput import TextInput

TextInput('Name').rules(['max:10'])
```

### min

Use `min` to set the minlength value for a string.

```python
from collapsar.fields.TextInput import TextInput

TextInput('Name').rules(['min:10'])
```

{{<alert context="info" text="For advanced validations see [Validations](/docs/validation)."/>}}
