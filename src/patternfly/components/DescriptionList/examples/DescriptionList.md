---
title: Description List
section: beta
cssPrefix: pf-c-description-list
---

## Examples

```hbs title=Basic
{{#> description-list description-list--id="basic-example"}}
  <!-- {{#> description-list-label description-list-label--attribute=''}}
    {{#> title title--type="h2" title--modifier="pf-m-lg"}}System properties{{/title}}
  {{/description-list-label}} -->
  {{#> description-list-list description-list-list--modifier='pf-m-inline'}}
    {{#> description-list-group}}
      {{#> description-list-term}}
        Name
      {{/description-list-term}}
      {{#> description-list-description}}
        Apache
      {{/description-list-description}}
      {{#> description-list-description}}
        Linux
      {{/description-list-description}}
      {{#> description-list-description}}
        OScent
      {{/description-list-description}}
    {{/description-list-group}}
    {{#> description-list-group}}
      {{#> description-list-term}}
        Number of CPUs
      {{/description-list-term}}
      {{#> description-list-description}}
        2
      {{/description-list-description}}
    {{/description-list-group}}
    {{#> description-list-group}}
      {{#> description-list-term}}
        Sockets
      {{/description-list-term}}
      {{#> description-list-description}}
        2
      {{/description-list-description}}
    {{/description-list-group}}
    {{#> description-list-group}}
      {{#> description-list-term}}
        Cores per socket
      {{/description-list-term}}
      {{#> description-list-description}}
        1
      {{/description-list-description}}
    {{/description-list-group}}
    {{#> description-list-group}}
      {{#> description-list-term}}
        RAM (GB)
      {{/description-list-term}}
      {{#> description-list-description}}
        3.74 GB
      {{/description-list-description}}
    {{/description-list-group}}
    {{#> description-list-group}}
      {{#> description-list-term}}
        Storage
      {{/description-list-term}}
      {{#> description-list-description}}
        <a href="#">5 disks</a>
      {{/description-list-description}}
    {{/description-list-group}}
  {{/description-list-list}}
{{/description-list}}
```

## Documentation

### Overview

The description list component.

### Accessibility

| Attribute | Applied to | Outcome |
| -- | -- | -- |
| `aria-labelledby` | `.pf-c-description-list` | . **Required** |

### Usage

| Class | Applied to | Outcome |
| -- | -- | -- |
| `.pf-c-description-list` | `<div>` |  Initiates a description list. **Required** |