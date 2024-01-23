# BADGES FOR [OBSIDIAN.MD](https://github.com/obsidianmd)


## INTRO

This is light-weight plugin for displaying inline "badges" in [**Obsidian.md**](https://github.com/obsidianmd).

It acts similarly to a key:value store(database) for querying via default search or [Dataview](https://github.com/blacksmithgu/obsidian-dataview) plugin.

#### **ON THIS PAGE**
- [How to use this plugin](#how-to)
	- [Github Styled Badges](#github-style)
	- [Plain-text](#plain-text)
	- [Custom badges](#custom)
- [CSS styles](#css)
- [Dataview scripts](#dataview-scripts)
- [Installation](#installation)
- [Development](#development)
- [Notes](#notes)


## HOW-TO

##### DEFAULT SYNTAX

```markdown
`[!!KEY:VAL]`
```

| SYNTAX | DETAILS                         |
| ------ | ------------------------------- |
| `KEY`  | the type and name of the `ICON` |
| `VAL`  | the value and text displayed    |

> [!IMPORTANT]
> `VAL` cannot contain either the `|` pipe or the `:` colon symbols. They are used as delimiters for the [custom syntax](#custom).

##### CALLOUTS's BADDGES EXAMPLES

You can use the same names from the deafult [Obsidian's Callouts](https://help.obsidian.md/Editing+and+formatting/Callouts).

```markdown
`[!!note:note]`
`[!!info:info]`
`[!!todo:todo]`
...
`[!!cite:cite]`
```

##### RESULTS OF CALLOUTS's BADDGES EXAMPLES

![](assets/Badges-demo-Obsidian-v1.3.7-20230709144540.png)

![](assets/Badges-demo-Obsidian-v1.3.7-20230709144545.png)

##### EXAMPLES AVAIABLE IN PLUGIN

```markdown

###### Yellow and orange shades
`[!!faq:faq]` `[!!help:help]` `[!!question:question]` `[!!notice:notice]`
`[!!hat-tip:hat-tip]` `[!!clue:clue]` `[!!branch:branch]` `[!!highlight:highlight]`
`[!!snippet:snippet]` `[!!claim:claim]` `[!!profile:profile]`
`[!!attention:attention]` `[!!caution:caution]` `[!!warning:warning]`

###### Purple and pink shades
`[!!vault:vault]` `[!!honor:honor]` `[!!love:love]` `[!!command:command]`
`[!!account:account]` `[!!balance:balance]` `[!!home:home]`

###### Blue shades
`[!!image:image]` `[!!abstract:abstract]` `[!!hint:hint]` `[!!important:important]`
`[!!summary:summary]` `[!!tip:tip]` `[!!tldr:tldr]` `[!!info:info]` `[!!note:note]`
`[!!todo:todo]``[!!compute:compute]` `[!!party:party]` `[!!process:process]`
`[!!refine:refine]`  `[!!meta:meta]` `[!!compass:compass]` `[!!component:component]`
`[!!dream:dream]` `[!!polish:polish]`

###### Green shades
`[!!complete:complete]` `[!!attachment:attachment]` `[!!witness:witness]`
`[!!lightbulb:lightbulb]` `[!!verse:verse]` `[!!charge:charge]`
`[!!extract:extract]` `[!!hold:hold]` `[!!milestone:milestone]`
`[!!power:power]` `[!!sprout:sprout]`

###### Red shades
`[!!bomb:bomb]` `[!!bug:bug]` `[!!danger:danger]` `[!!error:error]`
`[!!fail:fail]` `[!!failure:failure]` `[!!missing:missing]`
`[!!magnet:magnet]` `[!!emergency:emergency]` `[!!lock:lock]` `[!!stop:stop]`

```

##### RESULTS AVAIABLE IN PLUGIN

![image](https://github.com/todearaujo/badges/assets/88564332/f2fe51da-18a3-4f05-9e03-3492c70b1b49)

![image](https://github.com/todearaujo/badges/assets/88564332/ce267c35-4806-469b-a789-531c68d1440f)


### GITHUB STYLE

##### SYNTAX

```markdown
`[!!|GHX>KEY:VAL]`
```

| SYNTAX          | DETAILS                                                                             |
| --------------- | ----------------------------------------------------------------------------------- |
| <code>\|</code> | Start pipe symbol                                                                   |
| `GHX`           | Github style, either `ghb` for the blue style or `ghs` for the green success style  |
| `>`             | Greater than symbol as delimiter                                                    |
| `KEY:VAL`       | `KEY` is the type or label, `VAL` is the value text displayed. e.g. `release:1.0.0` |

##### EXAMPLES IN GITHUB STYLE

```markdown
`[!!|ghb>release:1.2.1]`
`[!!|ghb>issues:2]`
`[!!|ghb>open issues:0]`
`[!!|ghb>closed issues:2]`
`[!!|ghb>contributors:3]`
`[!!|ghb>license:MIT]`
`[!!|ghs>checks:success]`
`[!!|ghs>build:success]`
```

##### RESULTS

![](assets/Badges-demo-Obsidian-v1.3.7-20230709171043.png)

![](assets/Badges-demo-Obsidian-v1.3.7-20230709171053.png)


### PLAIN-TEXT

##### SYNTAX

```markdown
`[!!|KEY:VAL]`
```

| SYNTAX          | DETAILS                               |
| --------------- | ------------------------------------- |
| <code>\|</code> | start pipe symbol                     |
| `KEY:VAL`       | `KEY` is the type, `VAL` is the value |

##### EXAMPLE

```markdown
`[!!|foo:bar]`
```

##### RESULTS

![](assets/Badges-demo-Obsidian-v1.3.7-20230709171707.png)

![](assets/Badges-demo-Obsidian-v1.3.7-20230709171713.png)



## CUSTOM

##### SYNTAX

```markdown
`[!!|ICON|KEY:VAL|COLOR-RGB]`
```

| SYNTAX                                               | DETAILS                                                                                                                |
| ---------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| <code>\|</code>                                      | start pipe symbol                                                                                                      |
| `ICON`                                               | name of icon. e.g. `lucide-dice`                                                                                       |
| <code>\|</code>                                      | pipe symbol                                                                                                            |
| `KEY:VAL`                                            | `KEY` is the type or label, `VAL` is the value text displayed. e.g. `release:1.0.0`                                    |
| <code>\|</code>                                      | pipe symbol                                                                                                            |
| `COLOR-RGB` <br>(optional, defaults to currentColor) | 3 (R.G.B.) numeric (0-255) values, separated by commas. e.g. `144,144,144` or CSS variable e.g. `var(--color-red-rgb)` |

##### EXAMPLES

```markdown
`[!!|message-square|comment:edited by j.d.|var(--color-cyan-rgb)]`
`[!!|dice|roll:eleven|120,82,238]`
`[!!|gem|mineral:emerald|var(--my-custom-rgb)]`
`[!!|apple|fruit:snack|var(--color-red-rgb)]`
`[!!|brain|brain:pkm|var(--color-purple-rgb)]`
`[!!|sun|weather:sunny|var(--color-yellow-rgb)]`
`[!!|cloudy|weather:cloudy|var(--mono-rgb-100)]`
`[!!|sunset|weather:8.44pm|var(--color-orange-rgb)]`
`[!!|dumbbell|reps:3 sets of 50|var(--mono-rgb-00)]`
`[!!|gift|event:wedding|var(--color-blue-rgb)]`
`[!!|plus-square|credit:$100|var(--color-green-rgb)]`
`[!!|minus-square|debit:$10|var(--color-pink-rgb)]`
```

##### RESULTS

![](assets/Badges-demo-Obsidian-v1.3.7-20230709171541.png)
![](assets/Badges-demo-Obsidian-v1.3.7-20230709171534.png)

## CSS

Custom `CSS` styles can be applied via [CSS snippets](https://help.obsidian.md/Extending+Obsidian/CSS+snippets).

All colors and styles can be over-written.

Check this page [CSS snippets](https://help.obsidian.md/Extending+Obsidian/CSS+snippets) from [Obsidian Help](https://help.obsidian.md/Extending+Obsidian/CSS+snippets/)

#### AVAIBLE VARIABLES

```css
body {
	/* Define badges' borders with this variables */
	--inline-badge-border-color: transparent;
	--inline-badge-border-radius: var(--radius-s);
	--inline-badge-border: 1px solid var(--inline-badge-border-color);
	/* Define 'custom-rgb" */
	--custom-rgb-1: var(--color-green-rgb);
}

.inline-badge[data-inline-badge^="vault"] {
	/* Now use '--custom-rgb-1" for consistency */
	color: rgba(var(--custom-rgb-1), .88);
	background-color: rgba(var(--custom-rgb-1),.22);
}
```


## DATAVIEW SCRIPTS

You're welcome to use `dataview` scripts avaiable at [badges-dataview.md](assets/badges-dataview.md) file of this repo.

## INSTALLATION

For fast **Badges** plugin setup:

1. Just click in this link [Badges for Obsidian.md](obsidian://show-plugin?id=badges) to open this plugin on the aplication.

Or open Obsidian's "Settings" and then...

1. Community Plugins > Browse
2. Search for "Badges"
3. Install

Manual setup:

1. Download the latest [release archive](https://github.com/gapmiss/badges/releases/download/1.1.0/badges-v1.1.0.zip)
2. Uncompress the downloaded archive
3. Move the `badges` folder to `/path/to/vault/.obsidian/plugins/` 
4. Settings > Community plugins
5. Click in the "Reload" icon in **Installed plugins**" section
6. Enable plugin changing the toggle

Or, you can download files and create a new "badges" folder yourself - manually.

1.  Download [`main.js`](src/main.ts), [`manifest.json]`](manifest.json) and [`styles.css`](styles.css) files from this repo
2.  Create a new folder at `/path/to/vault/.obsidian/plugins/badges`
3.  Move all the files you've just download to `/path/to/vault/.obsidian/plugins/badges`
4.  Settings > Community plugins > reload **Installed plugins**
5.  Enable plugin


## DEVELOPMENT

Have an idea and want to improve **Badges** plugin?

##### CLONE THIS REPO

```bash
cd /path/to/vault/.obsidian/plugins
git clone https://github.com/gapmiss/badges.git
cd badges
```
###### INSTALL PACKAGES AND RUN
```bash
npm i
npm run dev
```


## NOTES

Thanks to [Markdown Furigana Plugin](https://github.com/steven-kraft/obsidian-markdown-furigana) as an example implementation of Live Preview.

[Lucide](https://github.com/lucide-icons/lucide) icons from [https://lucide.dev](https://lucide.dev). Check their [LICENSE](https://lucide.dev/license). 
