---
title: ListGroup
section: demos
---

## Demos

### Badge list group

```hbs title=Flex-layout-in-nested-list-groups
{{#> list-group list-group--id="flex-layout-in-nested-list-groups"}}
  {{#> list-group-list list-group-list--attribute='aria-label="example parent component"' list-group-list--IsDiv="true"}}
    {{#> l-flex}}
      {{#> l-flex-item}}
        {{#> list-group list-group--id=(concat list-group--id '-subgroup1') list-group--modifier="pf-m-toolbars" list-group-item--IsListItem="true"}}
          {{#> list-group-main}}
            {{#> list-group-label}}
              System type tags
            {{/list-group-label}}
            {{#> list-group-list list-group-list--modifier="" list-group-list--IsLabelledby="true" list-group-list--type="ul"}}
              {{> list-group-demo-content-chips list-group-demo-content-chips--IsShort="true"}}
            {{/list-group-list}}
          {{/list-group-main}}
          {{> list-group-close list-group-close--attribute=''}}
        {{/list-group}}
      {{/l-flex-item}}
      {{#> l-flex-item}}
        {{#> list-group list-group--modifier="pf-m-toolbars" list-group--id=(concat list-group--id '-subgroup2') list-group-item--IsListItem="true"}}
          {{#> list-group-main}}
            {{#> list-group-label}}
              Cluster type chips
            {{/list-group-label}}
            {{#> list-group-list list-group-list--modifier="" list-group-list--IsLabelledby="true" list-group-list--type="ul"}}
              {{> list-group-demo-content-chips list-group-demo-content-chips--IsLong="true" list-group-item--type="li"}}
            {{/list-group-list}}
          {{/list-group-main}}
          {{> list-group-close list-group-close--attribute=''}}
        {{/list-group}}
      {{/l-flex-item}}
    {{/l-flex}}
  {{/list-group-list}}
{{/list-group}}
```

### Chip list group

```hbs title=Chip-list-group
{{> list-group-border-test}}
{{#> list-group list-group--id="chip-list-group-example"}}
  {{#> list-group-label}}
    Chips
  {{/list-group-label}}
  {{#> list-group-list list-group-list--IsLabelledby="true"}}
    {{> list-group-demo-content-chips}}
  {{/list-group-list}}
{{/list-group}}
{{> list-group-border-test}}
```

### Nested chip groups

```hbs title=List-group-chips-nested
{{> list-group-border-test}}
{{#> list-group list-group--id="list-group-badges-example" list-group--attribute=''}}
  {{#> list-group-list list-group-list--type="div" list-group-list--attribute=(concat 'role="list" aria-label="Chip groups parent group"') list-group-list--modifier="pf-m-column"}}
    {{#> list-group list-group--id=(concat list-group--id '-subgroup1') list-group--attribute=''}}
      {{#> list-group-label list-group-label--attribute=''}}
        Chip set one
      {{/list-group-label}}
      {{#> list-group-list list-group-list--type="ul" list-group-list--attribute='' list-group-list--IsLabelledby="true" list-group-list--modifier=""}}
        {{> list-group-demo-content-chips list-group-demo-content-badges--IsShort="true"}}
      {{/list-group-list}}
    {{/list-group}}
    {{#> list-group list-group--id=(concat list-group--id '-subgroup2') list-group--attribute=''}}
      {{#> list-group-label list-group-label--attribute=''}}
        Chip set two
      {{/list-group-label}}
      {{#> list-group-list list-group-list--type="ul" list-group-list--attribute='' list-group-list--IsLabelledby="true" list-group-list--modifier=""}}
        {{> list-group-demo-content-chips list-group-demo-content-badges--IsShort="true"}}
      {{/list-group-list}}
    {{/list-group}}
  {{/list-group-list}}
{{/list-group}}
{{> list-group-border-test}}
```

### Label list group

```hbs title=Label-list-group
{{> list-group-border-test}}
{{#> list-group list-group--id="label-list-group-example"}}
  {{#> list-group-label}}
    Labels
  {{/list-group-label}}
  {{#> list-group-list list-group-list--IsLabelledby="true"}}
    {{> list-group-demo-content-labels}}
  {{/list-group-list}}
{{/list-group}}
{{> list-group-border-test}}
```

### Button list group

```hbs title=Button-list-group
{{> list-group-border-test}}
{{#> list-group list-group--id="button-list-group-example"}}
  {{#> list-group-list list-group-list--IsLabelledby="true"}}
    {{> list-group-demo-content-buttons}}
  {{/list-group-list}}
{{/list-group}}
{{> list-group-border-test}}
```

### Badge-list-label-as-list-item

The label will wrap with other list items

```hbs title=Badge-list-label-as-list-item
{{> list-group-border-test}}
{{#> list-group list-group--id="badge-list-label-as-list-item-example"}}
  {{#> list-group-list list-group-list--IsLabelledBy="true"}}
    {{#> list-group-item list-group-item--IsLabel="true"}}
      Tags
    {{/list-group-item}}
    {{> list-group-demo-content-badges list-group-demo-content-badges--IsLong="true" badge--modifier="pf-m-unread"}}
  {{/list-group-list}}
{{/list-group}}
{{> list-group-border-test}}
```

### Stacked-label-badge-list-group

```hbs title=stacked-label-badge-list-group
{{> list-group-border-test}}
{{#> list-group list-group--modifier="pf-m-column" list-group--id="stacked-label-badge-list-group-example"}}
  {{#> list-group-label}}
    Tags
  {{/list-group-label}}
  {{#> list-group-list list-group-list--IsLabelledBy="true"}}
    {{> list-group-demo-content-badges list-group-demo-content-badges--IsShort="true" badge--modifier="pf-m-unread"}}
  {{/list-group-list}}
{{/list-group}}
{{> list-group-border-test}}
```

### Badges-list-group-with-toolbar-modifier

```hbs title=Badges-list-group-with-toolbar-modifier
{{> list-group-border-test}}
{{#> list-group list-group--modifier="pf-m-toolbar" list-group--id="badges-list-group-with-toolbar-modifier"}}
  {{#> list-group-label}}
    Tags
  {{/list-group-label}}
  {{#> list-group-list list-group-list--IsLabelledBy="true"}}
    {{> list-group-demo-content-badges list-group-demo-content-badges--IsLong="true" badge--modifier="pf-m-unread"}}
  {{/list-group-list}}
{{/list-group}}
{{> list-group-border-test}}
```

### Grouped-nested-badge-list

Nested groups will wrap by default

```hbs title=Grouped-nested-badges
{{> list-group-border-test}}
{{#> list-group list-group--id="grouped-nested-badges-example" list-group--attribute=''}}
  {{#> list-group-list list-group-list--type="div" list-group-list--attribute='role="list" aria-label="Grouped-nested-badges"'}}
    {{#> list-group list-group--attribute='' list-group--id=(concat list-group--id '-subgroup1') list-group--attribute=''}}
      {{#> list-group-label}}
        Unread tags
      {{/list-group-label}}
      {{#> list-group-list list-group-list--type="ul" list-group-list--IsLabelledBy="true" list-group-list--attribute=''}}
        {{> list-group-demo-content-badges list-group-demo-content-badges--IsShort="true" badge--modifier="pf-m-unread"}}
      {{/list-group-list}}
    {{/list-group}}
    {{#> list-group list-group--attribute='' list-group--id=(concat list-group--id '-subgroup2') list-group--attribute=''}}
      {{#> list-group-label}}
        Read tags
      {{/list-group-label}}
      {{#> list-group-list list-group-list--type="ul" list-group-list--IsLabelledBy="true" list-group-list--attribute=''}}
        {{> list-group-demo-content-badges badge--modifier="pf-m-read"}}
      {{/list-group-list}}
    {{/list-group}}
  {{/list-group-list}}
{{/list-group}}
{{> list-group-border-test}}
```

Nested groups will wrap by default

```hbs title=List-group-badges-nested-and-stacked
{{> list-group-border-test}}
{{#> list-group list-group--id="list-group-badges-example" list-group--attribute=''}}
  {{#> list-group-list list-group-list--type="div" list-group-list--attribute=''}}
    {{#> list-group list-group--id="list-group-badges-example" list-group--attribute=''}}
      {{#> list-group-label list-group-label--attribute=''}}
        Unread tags
      {{/list-group-label}}
      {{#> list-group-list list-group-list--attribute=''}}
        {{> list-group-demo-content-badges list-group-demo-content-badges--IsLong="true" badge--modifier="pf-m-unread"}}
      {{/list-group-list}}
    {{/list-group}}
    {{#> list-group list-group--id="list-group-badges-example" list-group--attribute=''}}
      {{#> list-group-label list-group-label--attribute=''}}
        Read tags
      {{/list-group-label}}
      {{#> list-group-list list-group-list--attribute=''}}
        {{> list-group-demo-content-badges badge--modifier="pf-m-unread"}}
      {{/list-group-list}}
    {{/list-group}}
  {{/list-group-list}}
{{/list-group}}
{{> list-group-border-test}}
```

## Documentation
This demo implements the drawer in context of the page component.
