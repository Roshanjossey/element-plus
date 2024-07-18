---
title: Mention
lang: en-US
---

# Mention

Used to mention someone or something in an input.

## Basic Usage

The most basic usage.

:::demo

mention/basic

:::

## Textarea

The input type can be set to `textarea`.

:::demo

mention/textarea

:::

## Customize label

Customize label by `label` slot.

:::demo

mention/label

:::

## Load remote options

Load options asynchronously.

:::demo

mention/loading

:::

## Customize Trigger Token

Customize Trigger Token by `prefix` props. Default to `@`, `Array<string>` also supported.

:::demo

mention/prefix

:::

## Work with form

to work with `el-form`.

:::demo

mention/form

:::

## API

### Attributes

::: tip
Since this component is developed based on the component [`el-input`](./input.md#attributes) , the original properties have not changed, so no repetition here,
and please go to the original component to view the documentation.
:::

| Name                                 | Description                                                                                  | Type                                                                         | Default    |
| ------------------------------------ | -------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------- |
| options                              | mention options list                                                                         | ^[array]`MentionOption[]`                                                    | []         |
| prefix                               | prefix character to trigger mentions. The string length must be exactly 1                    | ^[string]                                                                    | `'@'`      |
| split                                | character to split mentions. The string length must be exactly 1                             | ^[string]                                                                    | `' '`      |
| filter-option                        | customize filter option logic                                                                | ^[false] \| ^[Function]`(pattern: string, option: MentionOption) => boolean` | -          |
| placement                            | set popup placement                                                                          | ^[string]`'bottom' \| 'top'`                                                 | `'bottom'` |
| whole                                | when pressing the Backspace key to delete, whether the mention content is deleted as a whole | ^[boolean]                                                                   | `true`     |
| loading                              | whether the dropdown panel of mentions is in a loading state                                 | ^[boolean]                                                                   | `false`    |
| model-value / v-model                | input value                                                                                  | ^[string]                                                                    | -          |
| popper-class                         | custom class name for dropdown panel                                                         | ^[string]                                                                    | -          |
| popper-options                       | [popper.js](https://popper.js.org/docs/v2/) parameters                                       | ^[object] refer to [popper.js](https://popper.js.org/docs/v2/) doc           | -          |
| [input props](./input.md#attributes) | -                                                                                            | -                                                                            | -          |

### Events

| Name                              | Description                         | Type                                                         |
| --------------------------------- | ----------------------------------- | ------------------------------------------------------------ |
| search                            | trigger when prefix hit             | ^[Function]`(pattern: string, prefix: string) => void`       |
| select                            | trigger when user select the option | ^[Function]`(option: MentionOption, prefix: string) => void` |
| [input events](./input.md#events) | -                                   | -                                                            |

### Slots

| Name                            | Description                           |
| ------------------------------- | ------------------------------------- |
| label                           | content as option label               |
| loading                         | content as option loading             |
| header                          | content at the top of the dropdown    |
| footer                          | content at the bottom of the dropdown |
| [input slots](./input.md#slots) | -                                     |

### Exposes

| Name    | Description                   | Type                                    |
| ------- | ----------------------------- | --------------------------------------- |
| input   | el-input component instence   | ^[object]`Ref<InputInstance \| null>`   |
| tooltip | el-tooltip component instence | ^[object]`Ref<TooltipInstance \| null>` |

## Type Declarations

<details>
  <summary>Show declarations</summary>

```ts
type MentionOption = {
  value: string
  label?: string
  disabled?: boolean
  [key: string]: any
}
```

</details>