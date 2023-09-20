

## Introduction

> `莜面鱼鱼`  home page.

[Online browsing](http://sen26.cn)

Do you want to install such a cool homepage for your website?

Let's start now!



## Prerequisites

- Nodejs 6.0 above
- Git available






## Features

1. Highly encapsulates all the information in the page
2. Use [WebGL-Fluid-Simulation](https://github.com/PavelDoGreat/WebGL-Fluid-Simulation/) as background
3. Use `scss` as `css` preprocessor
4. Use `pug` as `html` preprocessor
5. Use `gulp` as a build tool and configure the build script
6. Comfortable animation and beautiful UI
7. Responsive, mobile support
8. The referenced `css` and`js` files do not exceed `18.5` kb in total!
9. Delayed response switch page event
10. There are many features left for you to explore...



## Structure

According to the characteristics of the project, it is divided into two categories：
1. `intro` First screen
2. `main` Secondary screen

The corresponding functions, styles and configurations are also based on this standard.



## Basic configuration

Each key name in the config.json file`config.json` corresponds to the corresponding component name.

such as：

```json
{
	"head": {
		"title": "莜面鱼鱼",
		"description": "Author:SimonMa,Category:Personal Blog",
		"favicon": "favicon.ico"
	}
}

```
The above configuration information corresponds to the information in the following `layout/head.pug` component.
```html
head
	title #{head.title}
	meta(charset="utf-8")
	meta(name="Description" content=`${head.description}`)
	link(rel="icon" href=`${head.favicon}` type="image/x-icon")
```



## Advanced configuration

### WebGL-Fluid-Simulation

Use [WebGL-Fluid-Simulation](https://github.com/PavelDoGreat/WebGL-Fluid-Simulation/) as background at home.

If you want to turn it off, set `intro.background: false`.

### supportAuthor

The `supportAuthor` option is turned on by default for configuration information, that is, authors are supported.

All support items are as follows：

1. The `octopus cat` will be displayed in the upper right corner of the home page.
2. The console prints the author's site information

If you want to turn it off, set `intro.author: false`.


### Icon replacement
Icons in the project, all from [阿里巴巴矢量图标库](https://www.iconfont.cn)

The replacement steps are as follows:

1. Please select your icon, add it to the project, and change the color to white.
2. Click Font Class method
3. Copy the contents of the generated link
4. Replace the contents of the file `/src/css/common/icon.scss`, where the contents of the `icon` selector must be preserved.
5. Config.json the corresponding item in the `config.json`file`main.ul. * .icon`

```css
.icon {
	display: block;
	width: 1.5em;
	height: 1.5em;
	margin: 0 auto;
	fill: currentColor;
	font-family: 'iconfont' !important;
	font-size: inherit;
	font-style: normal;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
}
```

