---
title: List group
section: components
cssPrefix: pf-c-list-group
---

import './ListGroup.css'

## Examples

A `.pf-c-list-group__label` can placed adjacent to a `.pf-c-list-group__list` or within a `.pf-c-list-group__list` as a list item.

## Core elements

`.pf-c-list-group` two container elements elements and other elements. `.pf-c-list-group__main`, `.pf-c-list-group__actions` and `.pf-c-list-group__actions`

`.pf-c-list-group__label` can be outside of or nested within a `.pf-c-list-group__list`. If nested within `.pf-c-list-group__list`, the subsequent `__list-item`s will wrap.

### Basic
```hbs title=Basic
{{#> list-group list-group--id="basic-example"}}
  {{#> list-group-label}}
    System count
  {{/list-group-label}}
  {{#> list-group-main}}
    {{#> list-group-list list-group-list--IsLabelledby="true"}}
      {{> list-group-demo-content-labels list-group-demo-content-labels--IsLong="true"}}
    {{/list-group-list}}
  {{/list-group-main}}
  {{#> list-group-actions}}
    {{> list-group-close}}
  {{/list-group-actions}}
{{/list-group}}
```

<!-- ```hbs title=Basic
{{#> list-group list-group--id="basic-example"}}
  {{#> list-group-main}}
    {{#> list-group-label}}
      System count
    {{/list-group-label}}
    {{#> list-group-list list-group-list--IsLabelledby="true"}}
      {{> list-group-demo-content-labels}}
    {{/list-group-list}}
  {{/list-group-main}}
{{/list-group}}
``` -->

```hbs title=Inline-modifier
{{#> list-group list-group--id="inline-modifier-example"}}
  {{#> list-group-main list-group-main--modifier="pf-m-inline"}}
    {{#> list-group-label}}
      System count
    {{/list-group-label}}
    {{#> list-group-list-container}}
      {{#> list-group-list list-group-list--IsLabelledby="true"}}
        {{> list-group-demo-content-labels}}
      {{/list-group-list}}
      {{> list-group-close}}
    {{/list-group-list-container}}
  {{/list-group-main}}
{{/list-group}}
```

### Basic label as li
```hbs title=Basic-label-as-li
{{#> list-group list-group--id="basic-as-li-example"}}
  {{#> list-group-main list-group-main--modifier="pf-m-inline-on-lg pf-m-stack-on-2xl"}}
    {{#> list-group-list list-group-list--attribute=(concat 'aria-labelledby="' list-group--id '-label"')}}
      {{#> list-group-label list-group-label--type="li"}}
        Tags
      {{/list-group-label}}
      {{> list-group-demo-content-chips}}
    {{/list-group-list}}
  {{/list-group-main}}
{{/list-group}}
```

## Nested-example-test

```hbs title=Nested-example-test
{{#> list-group list-group--id="nested-example-test"}}
  {{#> list-group-main list-group-main--modifier=""}}
    {{#> list-group-list list-group-list--modifier="pf-m-parent pf-m-2-col" list-group-list--attribute=(concat 'aria-label="example parent component"')}}
      {{#> list-group-item}}
        {{#> list-group list-group--modifier="pf-m-toolbars" list-group--id=(concat list-group--id '-subgroup1') list-group--attribute=(concat 'aria-labelledby="' list-group--id '-label"')}}
          {{#> list-group-main}}
            {{#> list-group-list list-group-list--modifier="" list-group-list--IsLabelledby="true"}}
              {{#> list-group-label list-group-label--type="li"}}
                System type tags
              {{/list-group-label}}
              {{> list-group-demo-content-chips list-group-demo-content-chips--IsShort="true"}}
            {{/list-group-list}}
          {{/list-group-main}}
          {{> list-group-close list-group-close--attribute=''}}
        {{/list-group}}
      {{/list-group-item}}
      {{#> list-group-item}}
        {{#> list-group list-group--modifier="pf-m-toolbars" list-group--id=(concat list-group--id '-subgroup2') list-group--attribute=(concat 'aria-labelledby="' list-group--id '-label"')}}
          {{#> list-group-main}}
            {{#> list-group-label}}
              Cluster type chips
            {{/list-group-label}}
            {{#> list-group-list list-group-list--modifier="" list-group-list--IsLabelledby="true"}}
              {{> list-group-demo-content-chips list-group-demo-content-chips--IsLong="true"}}
            {{/list-group-list}}
          {{/list-group-main}}
          {{> list-group-close list-group-close--attribute=''}}
        {{/list-group}}
      {{/list-group-item}}
    {{/list-group-list}}
  {{/list-group-main}}
{{/list-group}}
```

If `.pf-c-list-group__label` is applied to a list item, the following list items will wrap around it.

## Nested-toolbar-groups
```hbs title=Nested-toolbar-groups
{{#> list-group list-group--id="basic-example"}}
  {{#> list-group-list list-group-list--attribute='aria-label="Applied filters"'}}
    {{#> list-group-item}}
      {{#> list-group list-group--id=(concat list-group--id '-subgroup-1') list-group--modifier="pf-m-toolbar" list-group--attribute=''}}
        {{#> list-group-main}}
          {{#> list-group-label}}
            Tags
          {{/list-group-label}}
          {{#> list-group-list list-group-list--attribute=(concat 'aria-labelledby="' list-group--id '-label"')}}
            {{> list-group-demo-content-chips list-group-demo-content-chips--IsShort="true"}}
          {{/list-group-list}}
        {{/list-group-main}}
        {{> list-group-close}}
      {{/list-group}}
    {{/list-group-item}}
    {{#> list-group-item}}
      {{#> list-group list-group--id=(concat list-group--id '-subgroup-2') list-group--modifier="pf-m-toolbar" list-group--attribute=''}}
        {{#> list-group-main}}
          {{#> list-group-label}}
            Chips in a group
          {{/list-group-label}}
          {{#> list-group-list list-group-list--attribute=(concat 'aria-labelledby="' list-group--id '-label"')}}
            {{> list-group-demo-content-chips}}
          {{/list-group-list}}
        {{/list-group-main}}
        {{> list-group-close}}
      {{/list-group}}
    {{/list-group-item}}
  {{/list-group-list}}
{{/list-group}}
```

## Label stacked, pf-m-column

A stacked layout can be achieved with by applying `.pf-m-column` to `.pf-c-list-group`.

```hbs title=Label-stacked-(pf-c-column)
{{#> list-group list-group--modifier="pf-m-column" list-group--id="label-stacked-example"}}
  {{#> list-group-label}}
    Tags
  {{/list-group-label}}
  {{#> list-group-list list-group-list--attribute=(concat 'aria-labelledby="' list-group--id '-label"')}}
    {{> list-group-content-items-1}}
  {{/list-group-list}}
{{/list-group}}
```

## Nested groups

<!-- {{#> list-group list-group--parent-id="nested-groups-example" list-group--modifier="pf-m-container" list-group--attribute='role="list" aria-label="Nested group example"'}} -->
```hbs title=Nested-groups
{{#> list-group list-group--id="nested-groups-example" list-group--attribute=(concat 'aria-label="Parent list label" role="list"')}}
  {{#> list-group-label}}
    {{#> title titleType="h3"}}
      Tags
    {{/title}}
  {{/list-group-label}}
  {{#> list-group-list list-group-list--type="div"}}
    {{#> list-group list-group--id=(concat list-group--id '-sub-group1') list-group--attribute='' list-group--IsNested="true" list-group--modifier=""}}
      {{#> list-group-label}}
        {{#> title titleType="h3"}}
          Tags
        {{/title}}
      {{/list-group-label}}
      {{#> list-group-list list-group-list--type="ul" list-group-list--attribute=(concat 'aria-labelledby="' list-group--id '-label"')}}
        {{> list-group-content-items-1 list-group-content-items-1--IsShort="true"}}
      {{/list-group-list}}
    {{/list-group}}
    {{#> list-group list-group--id=(concat list-group--id '-sub-group2') list-group--attribute='' list-group--IsNested="true" list-group--modifier=""}}
      {{#> list-group-label}}
        {{#> title titleType="h3"}}
          Labels
        {{/title}}
      {{/list-group-label}}
      {{#> list-group-list list-group-list--type="ul" list-group-list--attribute=(concat 'aria-labelledby="' list-group--id '-label"')}}
        {{> list-group-content-items-2 list-group-content-items-2--IsShort="true"}}
      {{/list-group-list}}
    {{/list-group}}
    {{#> list-group list-group--id=(concat list-group--id '-sub-group3') list-group--attribute='' list-group--IsNested="true" list-group--modifier=""}}
      {{#> list-group-label}}
        {{#> title titleType="h3"}}
          Labels
        {{/title}}
      {{/list-group-label}}
      {{#> list-group-list list-group-list--type="ul" list-group-list--attribute=(concat 'aria-labelledby="' list-group--id '-label"')}}
        {{> list-group-content-items-2}}
      {{/list-group-list}}
    {{/list-group}}
  {{/list-group-list}}
{{/list-group}}
```

## Stacked
`.pf-m-toolbar` can be applied to `.pf-c-list-group` or isolated to `.pf-c-list-group__list`.

```hbs title=Stacked-example
{{#> list-group list-group--parent-id="list-group-column-example" list-group--attribute='role="list" aria-label="Stacked example"'}}
  {{#> list-group-list list-group-list--type="div" list-group-list--modifier="pf-m-column"}}
    {{#> list-group list-group--attribute='' list-group--attribute='role="listitem"'}}
      {{#> list-group-label}}
        Tags
      {{/list-group-label}}
      {{#> list-group-list list-group-list--attribute=(concat 'aria-labelledby="' list-group--id '-label"') list-group-list--modifier=""}}
        {{> list-group-content-items-1}}
      {{/list-group-list}}
    {{/list-group}}
    {{#> list-group list-group--attribute='' list-group--attribute='role="listitem"'}}
      {{#> list-group-label}}
        Labels
      {{/list-group-label}}
      {{#> list-group-list list-group-list--attribute=(concat 'aria-labelledby="' list-group--id '-label"') list-group-list--modifier=""}}
        {{> list-group-content-items-2}}
      {{/list-group-list}}
    {{/list-group}}
  {{/list-group-list}}
{{/list-group}}
```

```hbs title=Nested-pill-groups-example
{{#> list-group list-group--modifier="pf-m-columns" list-group--parent-id="nested-pill-groups-example" list-group--attribute=(concat 'role="list" aria-labelledby=" nested-pill-groups-example-label"')}}
  {{#> list-group-label list-group-label--id=(concat list-group--parent-id '-label') list-group-label--modifier="pf-m-header"}}
    Group label. This label describes the group of nested list groups.
  {{/list-group-label}}

  {{#> list-group list-group--id=(concat list-group--parent-id '-nested-list1') list-group--attribute='' list-group--modifier='pf-m-toolbar'}}
    {{#> list-group-label list-group-label--id="label1"}}
      Tags
    {{/list-group-label}}
    {{#> list-group-list}}
      {{> list-group-content-items-1}}
    {{/list-group-list}}
  {{/list-group}}

  {{#> list-group list-group--id=(concat list-group--parent-id '-nested-list2') list-group--attribute='' list-group--modifier='pf-m-toolbar'}}
    {{#> list-group-label list-group-label--id="label2"}}
      Labels
    {{/list-group-label}}
    {{#> list-group-list}}
      {{> list-group-content-items-2}}
    {{/list-group-list}}
  {{/list-group}}

  {{#> list-group list-group--id=(concat list-group--parent-id '-nested-list3') list-group--attribute='' list-group--modifier=''}}
    {{#> list-group-list list-group-list--modifier="pf-m-toolbar"}}
      {{#> list-group-item list-group-item--IsLabel="true" list-group-item--id=(concat list-group-id '-label3')}}
        Tags
      {{/list-group-item}}
      {{> list-group-content-items-1}}
    {{/list-group-list}}
  {{/list-group}}

  {{#> list-group list-group--id=(concat list-group--parent-id '-nested-list4') list-group--attribute='' list-group--modifier=''}}
    {{#> list-group-list list-group-list--modifier="pf-m-toolbar"}}
      {{#> list-group-item list-group-item--IsLabel="true" list-group-item--id=(concat list-group-id '-label4')}}
        Labels
      {{/list-group-item}}
      {{> list-group-content-items-1}}
    {{/list-group-list}}
  {{/list-group}}
{{/list-group}}
```

```hbs title=Nested-example
{{#> list-group list-group--parent-id="nested-example" list-group--attribute='role="list"'}}
  {{#> list-group-label list-group-label--id=(concat list-group '-label1')}}
    Group label. This label describes the group of nested list groups.
  {{/list-group-label}}

  {{#> list-group list-group--id=(concat list-group--parent-id '-sub-group1') list-group--attribute='' list-group--modifier=''}}
    {{#> list-group-list}}
      {{#> list-group-item list-group-item--IsLabel="true" list-group-item--id=(concat list-group-id '-label1')}}
        Label, this is hidden from assistive technologies
      {{/list-group-item}}
      {{> list-group-content-items-1}}
    {{/list-group-list}}
  {{/list-group}}

  {{#> list-group list-group--id=(concat list-group--parent-id '-sub-group2') list-group--attribute='' list-group--modifier=''}}
    {{#> list-group-list}}
      {{#> list-group-item list-group-item--IsLabel="true" list-group-item--id=(concat list-group-id '-label2')}}
        Label for group 2, this is hidden from assistive technologies
      {{/list-group-item}}
      {{> list-group-content-items-2}}
    {{/list-group-list}}
  {{/list-group}}
{{/list-group}}
```

```hbs title=Nested-stacked-example
{{#> list-group list-group--modifier="pf-m-column" list-group--parent-id="nested-stacked-example" list-group--attribute=(concat 'role="list" aria-labelledby="' list-group--parent-id '-label')}}
  {{#> list-group-label list-group-label--id="label"}}
    Group label. This label describes the group of nested list groups.
  {{/list-group-label}}

  {{#> list-group list-group--id=(concat list-group--parent-id '-nested-list1') list-group--attribute='' list-group--modifier=''}}
    <!-- {{#> list-group-label list-group-label--id="description1"}}
      Nested group one label
    {{/list-group-label}} -->
    {{#> list-group-list}}
      {{#> list-group-item list-group-item--IsLabel="true" list-group-item--id=(concat list-group-id '-label1')}}
        Label, this is hidden from assistive technologies
      {{/list-group-item}}
      {{> list-group-content-items-1}}
    {{/list-group-list}}
  {{/list-group}}

  {{#> list-group list-group--id="list-group-nested-list2" list-group--attribute='' list-group--modifier=''}}
    <!-- {{#> list-group-label list-group-label--id="description2"}}
      Nested group two label
    {{/list-group-label}} -->
    {{#> list-group-list}}
      {{#> list-group-item list-group-item--IsLabel="true" list-group-item--id=(concat list-group-id '-label2')}}
        Label for group 2, this is hidden from assistive technologies
      {{/list-group-item}}
      {{> list-group-content-items-2}}
    {{/list-group-list}}
  {{/list-group}}
{{/list-group}}
```

`.pf-m-column` can also be applied to `.pf-c-list-group__list`, which will stack the list items.

```hbs title=Group-and-list-stacked
{{#> list-group list-group--modifier="pf-m-column" list-group--id="group-and-list-column-example"}}
  {{#> list-group-label}}
    Tags
  {{/list-group-label}}
  {{#> list-group-list list-group-list--modifier="pf-m-column"}}
    {{> list-group-content-items-1}}
  {{/list-group-list}}
{{/list-group}}
```

```hbs title=No-wrap-example
{{#> list-group list-group--modifier="pf-m-nowrap" list-group--id="nested-groups-example"}}
  {{#> list-group-label list-group-label--attribute='aria-label="Tags"'}}
    <i class="fas fa-tag" aria-hidden="true"></i>
  {{/list-group-label}}
  {{#> list-group-list}}
    {{> list-group-content-items-1 list-group-content-items-1--IsLong="true"}}
  {{/list-group-list}}
{{/list-group}}
```

```hbs title=Nested-example-inline-labels
{{#> list-group list-group--parent-id="list-group-nested-example" list-group--attribute='role="list"'}}
  {{#> list-group-label}}
    List header
  {{/list-group-label}}
  {{#> list-group list-group--id=(concat list-group--parent-id '-list-group-nested-list1') list-group--modifier="pf-m-row" list-group--attribute=''}}
    {{#> list-group-label list-group-label--id="label1"}}
      Nested list header
    {{/list-group-label}}
    {{#> list-group-list list-group-list--id="List group 1"}}
      {{> list-group-content-items-1}}
    {{/list-group-list}}
  {{/list-group}}

  {{#> list-group list-group--id=(concat list-group--parent-id '-list-group-nested-list2') list-group--modifier="pf-m-row" list-group--attribute=""}}
    {{#> list-group-label list-group-label--id="label2"}}
      Nested list label
    {{/list-group-label}}
    {{#> list-group-list list-group-list--id=(concat list-group--id '-list2')}}
      {{> list-group-content-items-2}}
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
| `.pf-m-column` | `.pf-c-list-group` | Modifies list group layout. |
| `.pf-m-toolbar` | `.pf-c-list-group__list` | Modifies list group list presentation. |
