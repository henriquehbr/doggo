# doggo
> A collection of Pug utils to make your syntax even more concise and readable

Bored of having to google or copy and paste all out these meta-tags everytime you want to use them? or by having to type that extensive and ugly markup to create a simple table? or just wanna simplify your Pug syntax even more? then, doggo is for you!

This library is packed with:

- A small collection of mixins that will provide a cleaner syntax when writing common HTML tags, such as `<link>` or `<script>`
- A medium-sized collection of ready-to-production meta-tags with a cleaner syntax (including OpenGraph meta tags)

## Get started

For meta tags, all the mixins (excluding a few ones) follow a fixed pattern

With pug:

```pug
//- With Pug
meta(name=name content=content)

//- With doggo
+name(content)
```

#### Example:

```pug
//- With Pug
meta(name="charset" content="utf-8")
meta(name="viewport" content="width=device-width, initial-scale=1.0")
meta(name="description" content="Lorem ipsum dolor sit amet consectetur")
meta(http-equiv="X-UA-Compatible" content="ie=edge")
meta(name="keywords" content="lorem, ipsum, lorem ipsum, lipsum")

//- With doggo (both charset and viewport defaults to their respective values if no parameters are passed)
+charset
+viewport
+description("Lorem ipsum dolor sit amet consectetur")
+ie-support
+keywords(["lorem", "ipsum", "lorem ipsum", "lipsum"])
```

For frequently used Pug elements

#### Example:

```pug
//- With Pug
link(rel="stylesheet" href="index.css")
script(src="index.js")
table
	tbody
		th Id
		th Name
		th Phone
	thead
		tr
			td 1
			td John Doe
			td 65645754
		tr
			td 2
			td Jane Doe
			td 54646645

//- With doggo
+css("index.css")
+js("index.js")
+table(["Id", "Name", "Phone"])
	+tr(["1", "John Doe", "65645754"])
	+tr(["2", "Jane Doe", "54646645"])
```