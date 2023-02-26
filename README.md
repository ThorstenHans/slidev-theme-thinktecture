# slidev-theme for Thinktecture

A minimalistic slidev theme for Thinktecture.

## Install

Add the following frontmatter to your `slides.md`. Start Slidev then it will prompt you to install the theme automatically.

<pre><code>---
theme: <b>thinktecture</b>
---</code></pre>

## Layouts

This theme provides the following layouts:

### Cover

By default, the first slide of a deck uses the cover layout.

![Cover Layout](/assets/cover.png)

The main content of the slide becomes the title, subtitle is set via `::subtitle::` slot and footer using `::footer::` slot

#### Red variant

To use the red cover, set `red: true` in frontmatter

![Red Cover Layout](/assets/cover-red.png)


### Profile slide `profile`

![Profile Layout](/assets/profile.png)

You can provide individual profile information using the following frontmatter:

| Property | Type | required | description | default value |
| --- | --- | --- | --- | --- |
| `speaker` | `string` | yes | Your name | |
| `job` | `string` | no | Your job title | `Hausmeister` |
| `mail` | `string` | no | Your mail address | `office@thinktecture.com`|
| `twitter`| `string` | no | Your Twitter handle | `thinktecture` |
| `blog` | `object {name:string, url:string}` | no | your personal blog | `null`|
| `image` | `string` | yes | Path or URL for a picture of you | |
| `tags` | `string[]` | no | Technology Focus Tags | `[]` |
| `awards` | `string[]` | no | Your awards | `[]` |

When omitting the optional `awards` property, profile will render like shown belog

![Profile Layout (no-awards)](/assets/profile-no-awards.png)

### Section slide `section`

![Section Layout](/assets/section.png)

Set the name of the section using the `name` property in frontmatter

### Immersive layout

Render a bold text in front of a fullsize image using the `immersive` layout. Set the `image` in frontmatter:

```markdown
---
layout: immersive
image: 'https://source.unsplash.com/collection/94734566/1920x1080'
---
# this is a test
```

![Immersive](/assets/immersive.png)

#### Red Variant

To use the red immersive layout, set `red: true` in frontmatter

![Immersive](/assets/immersive-red.png)


### 2 Column-Layout

In contrast to the default 2-Column-Layout, ours can render a text spreading accross left and right area.

```markdown
---
layout: two-columns
---

# This is a two column slide

Some general text that goes before the two columns

::left::

With some text that goes on the left side

- And some
- important bullets

::right::

With some other text that goes on the right side

- Again with some
- very important bullets
```

![2-Column-Layout](/assets/two-columns.png)


### Demo time 🚀 `demo`

![Demo Layout](/assets/demo.png)

You can provide the name of the demo using the `name` property in frontmatter.

### Closing slide `closing`

![Closing Layout](/assets/closing.png)

You can set links using the `links` property in frontmatter. Every link consists of `name` and `url`. The footer can be set using the `::footer::` slot.

### Red Variant

To use the red closing layout, set `red: true` in frontmatter

![Red Closing Layout](/assets/closing-red.png)

## Contributing

- `npm install`
- `npm run dev` to start theme preview of `example.md`
- Edit the `example.md` and style to see the changes
- `npm run export` to generate the preview PDF
- `npm run screenshot` to generate the preview PNG
