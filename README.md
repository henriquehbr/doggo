# doggo
> A collection of Pug utils to make your syntax even more concise and readable

Bored of having to google or copy and paste all out these meta-tags everytime you want to use them? or just wanna simplify your Pug syntax even more? then, doggo is for you!

This library is packed with:

- A small collection of mixins that will provide a cleaner syntax when writing common HTML tags, such as `<link>` or `<script>`
- A medium-sized collection of ready-to-production meta-tags with a cleaner syntax (including OpenGraph meta tags)

## Included mixins

#### `+charset`

#### Output

```pug
meta(charset=charset)
```

#### Parameters

| Name    | Type     | Default   |
| ------- | -------- | --------- |
| charset | `string` | `"utf-8"` |

#### `+viewport`

#### Output

```pug
meta(name="viewport" content="width=device-width, initial-scale=1.0")
```

#### Parameters

| Name     | Type     | Default                                   |
| -------- | -------- | ----------------------------------------- |
| viewport | `string` | `"width=device-width, initial-scale=1.0"` |

#### `+ie-support`

#### Output

```pug
meta(http-equiv="X-UA-Compatible" content=content")
```

#### Parameters

| Name    | Type     | Default     |
| ------- | -------- | ----------- |
| content | `string` | `"ie=edge"` |

#### `+keywords`

#### Output

```pug
meta(name="keywords" content=keywords)
```

#### Parameters

| Name     | Type    | Default     |
| -------- | ------- | ----------- |
| keywords | `array` | `undefined` |

#### `+description`

#### Output

```pug
meta(name="description" content=description)
```

#### Parameters

| Name        | Type     | Default     |
| ----------- | -------- | ----------- |
| description | `string` | `undefined` |