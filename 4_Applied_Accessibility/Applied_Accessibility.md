# Applied Accessibility

## Add a Text Alternative to Images for Visually Impaired Accessibility

```html
<img src="doingKarateWow.jpeg" alt="Camper cat doing karate excitedly">
```

## Know When Alt Text Should be Left Blank

Sometimes images are grouped with a caption already describing them, or they are used for decoration only. In these cases, `alt` text may seem redundant or unnecessary.

When an image is already explained with text content or does not add meaning to a page, the `img` still needs an alt attribute, but it can be set to an empty string. Here's an example:

```html
<img src="visualDecoration.jpeg" alt="">
```

Background images usually fall under the 'decorative' label as well. However, they are typically applied with CSS rules, and therefore not part of the markup screen readers process.

Note: For images with a caption, you may still want to include `alt` text since it helps search engines catalog the image's content.

```html
<h1>Deep Thoughts with Master Camper Cat</h1>
<article>
  <h2>Defeating your Foe: the Red Dot is Ours!</h2>
  <p>To Come...</p>
</article>

<img src="samuraiSwords.jpeg" alt="">

<article>
  <h2>Is Chuck Norris a Cat Person?</h2>
  <p>To Come...</p>
</article>
```

## Use Headings to Show Hierarchical Relationships of Content

Screen readers can be set to read only the headings on a page so the user gets a summary. It is important for the heading tags in your markup to have semantic meaning and relate to each other, not be picked merely for their size values.

Semantic meaning means that the tag you use around content indicates the type of information it contains.

As an example, a page with an `h2` element followed by several subsections labeled with `h4` elements would confuse a screen reader user. With six choices, it's tempting to use a tag because it looks better in a browser, but you can use CSS to edit the relative sizing.

Each page should have one and only one `h1` element.

```html
<h1>How to Become a Ninja</h1>
<main>
  <h2>Learn the Art of Moving Stealthily</h2>
  <h3>How to Hide in Plain Sight</h3>
  <h3>How to Climb a Wall</h3>

  <h2>Learn the Art of Battle</h2>
  <h3>How to Strengthen your Body</h3>
  <h3>How to Fight like a Ninja</h3>

  <h2>Learn the Art of Living with Honor</h2>
  <h3>How to Breathe Properly</h3>
  <h3>How to Simplify your Life</h3>
</main>
```

## Jump Straight to the Content Using the main Element

By default, a browser renders these elements similar to the humble `div`. However, using them where appropriate gives additional meaning to your markup.

The `main` element is used to wrap (you guessed it) the `main` content, and there should be only one per page.

The `main` tag also has an embedded landmark feature that assistive technology can use to navigate to the `main` content quickly.

```html
<header>
  <h1>Weapons of the Ninja</h1>
</header>
<main></main>
<footer></footer>
```

## Wrap Content in the article Element

`article` is a sectioning element and is used to wrap independent, self-contained content.

Remember that folks using assistive technologies rely on organized, semantically meaningful markup to better understand your work.

tbc.