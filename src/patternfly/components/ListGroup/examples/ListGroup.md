---
title: List group
section: components
cssPrefix: pf-c-list-group
---

import './ListGroup.css'

## Examples

A `.pf-c-list-group__label` can placed adjacent to a `.pf-c-list-group__list` or within a `.pf-c-list-group__list` as a list item.

```hbs title=Basic
{{#> list-group list-group--id="list-group-basic-example"}}
  {{#> list-group-label}}
    Label
  {{/list-group-label}}
  {{#> list-group-list list-group-list--attribute=(concat 'aria-labelledby="' list-group--id '-label"')}}
    {{> list-group-content-items-1}}
  {{/list-group-list}}
{{/list-group}}
```

If `.pf-c-list-group__label` is applied to a list item, the following list items will wrap around it.

```hbs title=Basic-label-as-list-item
{{#> list-group list-group--id="list-group-label-as-list-item"}}
  {{#> list-group-list}}
    {{#> list-group-list-item list-group-list-item--IsLabel="true"}}
      Label
    {{/list-group-list-item}}
    {{> list-group-content-items-1}}
  {{/list-group-list}}
{{/list-group}}
```

```hbs title=Basic-group-stacked
{{#> list-group list-group--modifier="pf-m-stacked" list-group--id="basic-group-stacked-example"}}
  {{#> list-group-label}}
    Label
  {{/list-group-label}}
  {{#> list-group-list}}
    {{> list-group-content-items-1}}
  {{/list-group-list}}
{{/list-group}}
```

`.pf-m-toolbar` can be applied to `.pf-c-list-group` or isolated to `.pf-c-list-group__list`.

```hbs title=Chip-groups
{{#> list-group list-group--modifier="pf-m-stacked" list-group--parent-id="chip-group-example"}}
  {{#> list-group list-group--id=(concat list-group--parent-id '-sub-group1') list-group--IsNested="true"}}
    {{#> list-group-label}}
      List title
    {{/list-group-label}}
    {{#> list-group-list}}
      {{> list-group-example-labels-1}}
    {{/list-group-list}}
  {{/list-group}}
  {{#> list-group list-group--id=(concat list-group--parent-id '-sub-group2') list-group--IsNested="true"}}
    {{#> list-group-label}}
      Longer title list
    {{/list-group-label}}
    {{#> list-group-list}}
      {{> list-group-example-labels-2}}
    {{/list-group-list}}
  {{/list-group}}
{{/list-group}}
```

```hbs title=Stacked-example
{{#> list-group list-group--modifier="pf-m-stacked" list-group--parent-id="list-group-stacked-example"}}
  {{#> list-group}}
    {{#> list-group-label list-group-label--id="description"}}
      List 1
    {{/list-group-label}}
    {{#> list-group-list list-group-list--title="List group"}}
      {{> list-group-example-labels-1}}
    {{/list-group-list}}
  {{/list-group}}
  {{#> list-group}}
    {{#> list-group-label list-group-label--id="description"}}
      List 1
    {{/list-group-label}}
    {{#> list-group-list list-group-list--title="List group"}}
      {{> list-group-example-labels-2}}
    {{/list-group-list}}
  {{/list-group}}
{{/list-group}}
```

```hbs title=Nested-pill-groups-example
{{#> list-group list-group--modifier="pf-m-stackeds" list-group--parent-id="nested-pill-groups-example" list-group--attribute='role="list"'}}
  {{#> list-group-label list-group-label--id=(concat list-group '-description1') list-group-label--modifier="pf-m-header"}}
    Group label. This label describes the group of nested list groups.
  {{/list-group-label}}

  {{#> list-group list-group--id=(concat list-group--parent-id '-nested-list1') list-group--attribute='' list-group--modifier='pf-m-toolbar'}}
    {{#> list-group-label list-group-label--id="label1"}}
      Label
    {{/list-group-label}}
    {{#> list-group-list}}
      {{> list-group-example-labels-2}}
    {{/list-group-list}}
  {{/list-group}}

  {{#> list-group list-group--id=(concat list-group--parent-id '-nested-list2') list-group--attribute='' list-group--modifier='pf-m-toolbar'}}
    {{#> list-group-label list-group-label--id="label2"}}
      Label of different length
    {{/list-group-label}}
    {{#> list-group-list}}
      {{> list-group-example-labels-1}}
    {{/list-group-list}}
  {{/list-group}}

  {{#> list-group list-group--id=(concat list-group--parent-id '-nested-list3') list-group--attribute='' list-group--modifier=''}}
    {{#> list-group-list list-group-list--modifier="pf-m-toolbar"}}
      {{#> list-group-list-item list-group-list-item--IsLabel="true" list-group-list-item--id=(concat list-group-id '-label3')}}
        Label, this is hidden from assistive technologies
      {{/list-group-list-item}}
      {{> list-group-example-labels-2}}
    {{/list-group-list}}
  {{/list-group}}

  {{#> list-group list-group--id=(concat list-group--parent-id '-nested-list4') list-group--attribute='' list-group--modifier=''}}
    {{#> list-group-list list-group-list--modifier="pf-m-toolbar"}}
      {{#> list-group-list-item list-group-list-item--IsLabel="true" list-group-list-item--id=(concat list-group-id '-label4')}}
        Label for group 2, this is hidden from assistive technologies
      {{/list-group-list-item}}
      {{> list-group-example-labels-1}}
    {{/list-group-list}}
  {{/list-group}}
{{/list-group}}
```

```hbs title=Nested-example
{{#> list-group list-group--modifier="pf-m-stacked" list-group--parent-id="list-group-nested-example" list-group--attribute='role="list"'}}
  {{#> list-group-label list-group-label--id=(concat list-group '-description1')}}
    Group label. This label describes the group of nested list groups.
  {{/list-group-label}}

  {{#> list-group list-group--id=(concat list-group--parent-id '-nested-list1') list-group--attribute='' list-group--modifier=''}}
    <!-- {{#> list-group-label list-group-label--id="description1"}}
      Nested group one label
    {{/list-group-label}} -->
    {{#> list-group-list}}
      {{#> list-group-list-item list-group-list-item--IsLabel="true" list-group-list-item--id=(concat list-group-id '-label1')}}
        Label, this is hidden from assistive technologies
      {{/list-group-list-item}}
      {{> list-group-example-labels-1}}
    {{/list-group-list}}
  {{/list-group}}

  {{#> list-group list-group--id="list-group-nested-list2" list-group--attribute='' list-group--modifier=''}}
    <!-- {{#> list-group-label list-group-label--id="description2"}}
      Nested group two label
    {{/list-group-label}} -->
    {{#> list-group-list}}
      {{#> list-group-list-item list-group-list-item--IsLabel="true" list-group-list-item--id=(concat list-group-id '-label2')}}
        Label for group 2, this is hidden from assistive technologies
      {{/list-group-list-item}}
      {{> list-group-example-labels-2}}
    {{/list-group-list}}
  {{/list-group}}
{{/list-group}}
```

```hbs title=Nested-example-inline-labels
{{#> list-group list-group--parent-id="list-group-nested-example" list-group--attribute='role="list"'}}
  {{#> list-group-label}}
    List header
  {{/list-group-label}}
  {{#> list-group list-group--id=(concat list-group--parent-id '-list-group-nested-list1') list-group--modifier="pf-m-inline" list-group--attribute=''}}
    {{#> list-group-label list-group-label--id="label1"}}
      Nested list header
    {{/list-group-label}}
    {{#> list-group-list list-group-list--id="List group 1"}}
      {{> list-group-example-labels-1}}
    {{/list-group-list}}
  {{/list-group}}

  {{#> list-group list-group--id=(concat list-group--parent-id '-list-group-nested-list2') list-group--modifier="pf-m-inline" list-group--attribute=""}}
    {{#> list-group-label list-group-label--id="label2"}}
      Nested list label
    {{/list-group-label}}
    {{#> list-group-list list-group-list--id=(concat list-group--id '-list2')}}
      {{> list-group-example-labels-1}}
    {{/list-group-list}}
  {{/list-group}}
{{/list-group}}
```

## Documentation

### Overview

The list group component provides a default SVG icon. If an image is used it should be 36px by 36px.

### Accessibility

| Attribute | Applied to | Outcome |
| -- | -- | -- |
| `role="list"` | `.pf-c-list-group` | Indicates that the list group is a list. **Required** when using nested lists. |
| `aria-label="[list label text]"` | `.pf-c-list-group` | Provides an accessible name for a list group. **Required** when `.pf-c-list-group__description` is not present. |

### Usage

| Class | Applied to | Outcome |
| -- | -- | -- |
| `.pf-c-list-group` | `<div>` | Initiates a list group. **Required** |
| `.pf-c-list-group__description` | `<div>` | Initiates a list group description. |
| `.pf-c-list-group__list` | `<div>` | Initiates a list group list. **Required** |
| `.pf-c-list-group__list-item` | `<div>` | Initiates a list group list item. **Required** |
| `.pf-m-stacked` | `.pf-c-list-group` | Modifies list group layout. |
| `.pf-m-toolbar` | `.pf-c-list-group__list` | Modifies list group list presentation. |
