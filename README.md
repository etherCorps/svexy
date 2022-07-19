# Svexy UI

## Note

<p>This is an under development project. I have changed the whole library on the basis of design system.</p>
<p>
  <img alt="" src="https://img.shields.io/apm/l/atomic-design-ui.svg" />
  <img alt="" src="https://img.shields.io/badge/for-svelte-green" />
  <img alt="" src="https://badgen.net/badge/icon/typescript?icon=typescript&label" />
</p>
It's a Svelete Component Library which is built using Tailwind CSS. This UI Library focuses on Structure of a Component not on designing it.

This is my first open source package. So please help me to make it best UI Library for Svelte. Everyone is invite to play and help me build this.

## Getting started

- Add following lines into your tailwind config

```javascript
/** @type {import('tailwindcss').Config} */
const colors = require('tailwindcss/colors.js');
module.exports = {
	content: [
		'./src/**/*.{html,js,svelte,ts}',
		'./node_modules/svexy-ui/components/**/*.{html,js,svelte,ts}'
	],
	theme: {
		colors: {
			gray: colors.gray,
			black: colors.black,
			white: colors.white,
			danger: colors.rose,
			info: colors.sky,
			warning: colors.amber,
			success: colors.teal,
			primary: colors.orange,
			secondary: colors.violet,
			tertiary: colors.rose
		},
		extend: {}
	},
	plugins: []
};
```

- Do not change variable names.
- You can config all the color as per your need but have to follow this method

## How to use Button

- let variants = ['solid', 'outlined', 'soft'] : 'solid' is default.
- let colors = ['primary', 'secondary', 'tertiary', 'dark', 'info', 'warning', 'danger', 'success'] : 'primary' is default.
- let sizes = ['xs', 'sm', 'md', 'lg', 'xl'] : 'md' is default.

```javascript
let variants = ['solid', 'outlined', 'soft'];
let colors = ['primary', 'secondary', 'tertiary', 'dark', 'info', 'warning', 'danger', 'success'];
<script>
  import Button from 'svexy-ui';
</script>
<Button variant={variant} color={color} shadow >Button<Button/>
```

- Pass `pill` if want to rounded.
- Pass `shadow` if need shadow of same color.
- Pass `href` for `<a>` tag.
- Pass `disabled` for disabled Button

## Useful Links

- [POC Documentation](https://docs.google.com/document/d/12QiB-en4Zf4h46a6WBzH7x5aX9oHBAsu_dv9CmIijMU/edit?usp=sharing)
- [Similiar to smelte](https://github.com/matyunya/smelte)
- [Inspiration](https://github.com/illright/attractions)

## Authors

- [@theetherGit](https://www.github.com/theetherGit)
- [@etherCorps](https://www.github.com/etherCorps)
