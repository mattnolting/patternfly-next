---
title: Description List
section: beta
cssPrefix: pf-c-description-list
---

## Examples

## Basic-example
```hbs title=Basic-example
{{#> description-list description-list--id="basic-example"}}
  {{#> description-list-label description-list-label--attribute=''}}
    {{#> title title--type="h2" title--modifier="pf-m-lg"}}System properties{{/title}}
  {{/description-list-label}}
  {{#> description-list-list description-list-list--modifier="pf-m-inline pf-m-2-col pf-m-3-col"}}
    {{#> description-list-group}}
      {{#> description-list-term description-list-term--attribute='id="name"'}}
        System name
      {{/description-list-term}}
      {{#> description-list-description description-list-description--attribute=''}}
        <ul aria-labelledby="name">
          <li>
            Apache
          </li>
          <li>
            MySql
          </li>
          <li>
            Node
          </li>
        </ul>
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

## Inline-example
```hbs title=Inline-example
{{#> description-list description-list--id="inline-example"}}
  {{#> description-list-label description-list-label--attribute=''}}
    {{#> title title--type="h2" title--modifier="pf-m-lg"}}System properties{{/title}}
  {{/description-list-label}}
  {{#> description-list-list description-list-list--modifier='pf-m-inline'}}
    {{#> description-list-group}}
      {{#> description-list-term description-list-term--attribute='id="name"'}}
        System name
      {{/description-list-term}}
      {{#> description-list-description description-list-description--attribute=''}}
        <ul aria-labelledby="name">
          <li>
            Apache
          </li>
          <li>
            MySql
          </li>
          <li>
            Node
          </li>
        </ul>
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

## Multi-col
```hbs title=Multi-column
{{#> description-list description-list--id="multi-column-example"}}
  {{#> description-list-label description-list-label--attribute=''}}
    {{#> title title--type="h2" title--modifier="pf-m-lg"}}System properties{{/title}}
  {{/description-list-label}}
  {{#> description-list-list description-list-list--modifier='pf-m-2-col pf-m-3-col-on-lg pf-m-4-col-on-xl'}}
    {{#> description-list-group}}
      {{#> description-list-term description-list-term--attribute='id="name"'}}
        System name
      {{/description-list-term}}
      {{#> description-list-description description-list-description--attribute=''}}
        <ul aria-labelledby="name">
          <li>
            Apache
          </li>
          <li>
            MySql
          </li>
          <li>
            Node
          </li>
        </ul>
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

## Inline-2-col
```hbs title=Inline-multi-column-example
{{#> description-list description-list--id="inline-multi-column-example"}}
  {{#> description-list-label description-list-label--attribute=''}}
    {{#> title title--type="h2" title--modifier="pf-m-lg"}}System properties{{/title}}
  {{/description-list-label}}
  {{#> description-list-list description-list-list--modifier='pf-m-inline pf-m-2-col pf-m-3-col-on-lg pf-m-4-col-on-xl'}}
    {{#> description-list-group}}
      {{#> description-list-term description-list-term--attribute='id="name"'}}
        System name
      {{/description-list-term}}
      {{#> description-list-description description-list-description--attribute=''}}
        <ul aria-labelledby="name">
          <li>
            Apache
          </li>
          <li>
            MySql
          </li>
          <li>
            Node
          </li>
        </ul>
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

## Auto-fill
```hbs title=Auto-fill
{{#> description-list description-list--id="auto-fill-example"}}
  {{#> description-list-label description-list-label--attribute=''}}
    {{#> title title--type="h2" title--modifier="pf-m-lg"}}System properties{{/title}}
  {{/description-list-label}}
  {{#> description-list-list description-list-list--modifier='pf-m-auto-fill'}}
    {{#> description-list-group}}
      {{#> description-list-term description-list-term--attribute='id="name"'}}
        System name
      {{/description-list-term}}
      {{#> description-list-description description-list-description--attribute=''}}
        <ul aria-labelledby="name">
          <li>
            Apache
          </li>
          <li>
            MySql
          </li>
          <li>
            Node
          </li>
        </ul>
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

## Inline-auto-fill
```hbs title=Inline-auto-fill
{{#> description-list description-list--id="inline-auto-fill-example"}}
  {{#> description-list-label description-list-label--attribute=''}}
    {{#> title title--type="h2" title--modifier="pf-m-lg"}}System properties{{/title}}
  {{/description-list-label}}
  {{#> description-list-list description-list-list--modifier='pf-m-inline pf-m-auto-fill'}}
    {{#> description-list-group}}
      {{#> description-list-term description-list-term--attribute='id="name"'}}
        System name
      {{/description-list-term}}
      {{#> description-list-description description-list-description--attribute=''}}
        <ul aria-labelledby="name">
          <li>
            Apache
          </li>
          <li>
            MySql
          </li>
          <li>
            Node
          </li>
        </ul>
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

<!--
```hbs title=Basic
{{#> grid grid--modifier="pf-m-all-6-col-on-lg"}}
  {{#> grid-item}}
{{#> description-list description-list--id="basic-example"}}
  {{#> description-list-label description-list-label--attribute=''}}
    {{#> title title--type="h2" title--modifier="pf-m-lg"}}System properties{{/title}}
  {{/description-list-label}}
  {{#> description-list-list description-list-list--modifier='pf-m-inline pf-m-auto-fill'}}
    {{#> description-list-group}}
      {{#> description-list-term}}
        Name
      {{/description-list-term}}
      {{#> description-list-description}}
        Apache
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
  {{/grid-item}}
  {{#> grid-item}}
{{#> description-list description-list--id="basic-example"}}
  {{#> description-list-label description-list-label--attribute=''}}
    {{#> title title--type="h2" title--modifier="pf-m-lg"}}System properties{{/title}}
  {{/description-list-label}}
  {{#> description-list-list description-list-list--modifier='pf-m-inline'}}
    {{#> description-list-group}}
      {{#> description-list-term}}
        Name
      {{/description-list-term}}
      {{#> description-list-description}}
        Apache
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
  {{/grid-item}}
{{/grid}}
```
-->

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