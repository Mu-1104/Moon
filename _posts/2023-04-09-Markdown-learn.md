---
layout: post
title: "My journey with Markdown"
date: 2023-04-09
excerpt: "This is a collection of resources about Markdown"
tags: [Markdown, CS]
comments: true
---


# Learning Resources

1. [the Markdown official website](https://daringfireball.net/projects/markdown/) 

2. [GitHub's Markdown guide](https://guides.github.com/features/mastering-markdown/)

3. Check out Markdown tutorial websites:
    1. [Markdown Tutorial](https://www.markdowntutorial.com/) 
    2. [Learn X in Y minutes](https://learnxinyminutes.com/docs/markdown/)

4. Download Markdown editors for practice: 
    1. [Typora](https://typora.io/)
    2. [StackEdit](https://stackedit.io/)
  
5. Explore online Markdown editors:
    1. [Dillinger](https://dillinger.io/)
    2. [Markdown Live Preview](https://markdownlivepreview.com/)
  
# Some Notes

## Headings

To create a heading, add one to six # symbols before your heading text. The number of # you use will determine the hierarchy level and typeface size of the heading.

```
# A first-level heading
## A second-level heading
### A third-level heading
```

![](https://docs.github.com/assets/cb-43514/mw-1000/images/help/writing/headings-rendered.webp)

## Styling text

You can indicate emphasis with **bold**, _italic_, ~~strikethrough~~, ***all bold and italic***, <sub>subscript</sub>, or <sup>superscript</sup> text in comment fields and .md files.

| Style	| Syntax | Keyboard shortcut | Example | Output |
| :---- | :----  | :---- | :---- | :---- |
|Bold	|** ** or __ __	| Command+B (Mac) or Ctrl+B (Windows/Linux)	| `**This is bold text**` | **This is bold text** |
|Italic	|* * or _ _  | Command+I (Mac) or Ctrl+I (Windows/Linux) |	`*This text is italicized*` |	*This text is italicized* |
| Strikethrough |	~~ ~~	| |	`~~This was mistaken text~~` |	~~This was mistaken text~~ |
| Bold and nested italic |	** ** and _ _	| |	`**This text is _extremely_ important**` |	**This text is _extremely_ important** |
| All bold and italic |	*** ***	| |	`***All this text is important***` | ***All this text is important*** |
| Subscript	| `<sub> </sub>`  |  | `<sub>This is a subscript text</sub>` | <sub>This is a subscript text</sub> |
| Superscript |	`<sup> </sup>` |  | `<sup>This is a superscript text</sup>` | <sup> This is a superscript text</sup> |


## Quoting text

You can quote text with a >.

Text that is not a quote

> Text that is a quote

Quoted text is indented, with a different type color.

![](https://docs.github.com/assets/cb-30028/mw-1000/images/help/writing/quoted-text-rendered.webp)

###### Tip: When viewing a conversation, you can automatically quote text in a comment by highlighting the text, then typing R. You can quote an entire comment by clicking , then Quote reply. For more information about keyboard shortcuts, see "[Keyboard shortcuts](https://docs.github.com/en/get-started/using-github/keyboard-shortcuts)"

## Quoting code
You can call out code or a command within a sentence with single backticks. The text within the backticks will not be formatted. You can also press the Command+E (Mac) or Ctrl+E (Windows/Linux) keyboard shortcut to insert the backticks for a code block within a line of Markdown.

Use `git status` to list all new or modified files that haven't yet been committed.

![](https://docs.github.com/assets/cb-34564/mw-1000/images/help/writing/inline-code-rendered.webp)

To format code or text into its own distinct block, use triple backticks.

Some basic Git commands are:

```
git status
git add
git commit
```

![](https://docs.github.com/assets/cb-53043/mw-1000/images/help/writing/code-block-rendered.webp)

For more information, see ["Creating and highlighting code blocks."](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks)

If you are frequently editing code snippets and tables, you may benefit from enabling a fixed-width font in all comment fields on GitHub. For more information, see ["About writing and formatting on GitHub."](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/about-writing-and-formatting-on-github#enabling-fixed-width-fonts-in-the-editor)

## Supported color models
In issues, pull requests, and discussions, you can call out colors within a sentence by using backticks. A supported color model within backticks will display a visualization of the color.

The background color is `#ffffff` for light mode and `#000000` for dark mode.

![](https://docs.github.com/assets/cb-24193/mw-1000/images/help/writing/supported-color-models-rendered.webp)

```
Notes:

A supported color model cannot have any leading or trailing spaces within the backticks.
The visualization of the color is only supported in issues, pull requests, and discussions.

```

## Section links

You can link directly to a section in a rendered file by hovering over the section heading to expose .

![](https://docs.github.com/assets/cb-113027/mw-1000/images/help/repository/readme-links.webp)

## Relative links

You can define relative links and image paths in your rendered files to help readers navigate to other files in your repository.

A relative link is a link that is relative to the current file. For example, if you have a README file in root of your repository, and you have another file in docs/CONTRIBUTING.md, the relative link to CONTRIBUTING.md in your README might look like this:

[Contribution guidelines for this project](docs/CONTRIBUTING.md)
GitHub will automatically transform your relative link or image path based on whatever branch you're currently on, so that the link or path always works. The path of the link will be relative to the current file. Links starting with / will be relative to the repository root. You can use all relative link operands, such as ./ and ../.

Relative links are easier for users who clone your repository. Absolute links may not work in clones of your repository - we recommend using relative links to refer to other files within your repository.

## Images
You can display an image by adding ! and wrapping the alt text in [ ]. Alt text is a short text equivalent of the information in the image. Then, wrap the link for the image in parentheses ().

![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://myoctocat.com/assets/images/base-octocat.svg)

GitHub supports embedding images into your issues, pull requests, discussions, comments and .md files. You can display an image from your repository, add a link to an online image, or upload an image. For more information, see ["Uploading assets."](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#supported-color-models)

Tip: When you want to display an image that is in your repository, use relative links instead of absolute links.

Here are some examples for using relative links to display an image.

| Context  | Relative Link |
| :------------ |:-------------|
| In a `.md` file on the same branch  | `/assets/images/electrocat.png`     |
| In a `.md` file on another branch   | `/../main/assets/images/electrocat.png`|
| In issues, pull requests and comments of the repository | `../blob/main/assets/images/electrocat.png?raw=true`|
| In a `.md` file in another repository | `/../../../../github/docs/blob/main/assets/images/electrocat.png`|
| In issues, pull requests and comments of another repository| `../../../github/docs/blob/main/assets/images/electrocat.png?raw=true`|

Note: The last two relative links in the table above will work for images in a private repository only if the viewer has at least read access to the private repository that contains these images.

For more information, see ["Relative Links."](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#relative-links)

## Specifying the theme an image is shown to

You can specify the theme an image is displayed for in Markdown by using the HTML `<picture>` element in combination with the `prefers-color-scheme` media feature. We distinguish between light and dark color modes, so there are two options available. You can use these options to display images optimized for dark or light backgrounds. This is particularly helpful for transparent PNG images.

For example, the following code displays a sun image for light themes and a moon for dark themes:

```
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/25423296/163456776-7f95b81a-f1ed-45f7-b7ab-8fa810d529fa.png">
  <source media="(prefers-color-scheme: light)" srcset="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>
The old method of specifying images based on the theme, by using a fragment appended to the URL (#gh-dark-mode-only or #gh-light-mode-only), is deprecated and will be removed in favor of the new method described above.
```

The old method of specifying images based on the theme, by using a fragment appended to the URL (`#gh-dark-mode-only` or `#gh-light-mode-only`), is deprecated and will be removed in favor of the new method described above.

## Lists

You can make an unordered list by preceding one or more lines of text with -, *, or +.
```
- George Washington
* John Adams
+ Thomas Jefferson
```

![](https://docs.github.com/assets/cb-29639/mw-1000/images/help/writing/unordered-list-rendered.webp)

To order your list, precede each line with a number.

```
1. James Madison
2. James Monroe
3. John Quincy Adams
```

![](https://docs.github.com/assets/cb-30507/mw-1000/images/help/writing/ordered-list-rendered.webp)

## Nested Lists

You can create a nested list by indenting one or more list items below another item.

To create a nested list using the web editor on GitHub or a text editor that uses a monospaced font, like Visual Studio Code, you can align your list visually. Type space characters in front of your nested list item until the list marker character (- or *) lies directly below the first character of the text in the item above it.

```
1. First list item
   - First nested list item
     - Second nested list item
```

Note: In the web-based editor, you can indent or dedent one or more lines of text by first highlighting the desired lines and then using Tab or Shift+Tab respectively.

![](https://docs.github.com/assets/cb-24122/mw-1000/images/help/writing/nested-list-alignment.webp)

![](https://docs.github.com/assets/cb-26191/mw-1000/images/help/writing/nested-list-example-1.webp)

To create a nested list in the comment editor on GitHub, which doesn't use a monospaced font, you can look at the list item immediately above the nested list and count the number of characters that appear before the content of the item. Then type that number of space characters in front of the nested list item.

In this example, you could add a nested list item under the list item 100. First list item by indenting the nested list item a minimum of five spaces, since there are five characters (100. ) before First list item.

```
1.   First list item
     - First nested list item
```

![](https://docs.github.com/assets/cb-17039/mw-1000/images/help/writing/nested-list-example-3.webp)

You can create multiple levels of nested lists using the same method. For example, because the first nested list item has seven characters (␣␣␣␣␣-␣) before the nested list content First nested list item, you would need to indent the second nested list item by seven spaces.

```
1.   First list item
     - First nested list item
       - Second nested list item
```

![](https://docs.github.com/assets/cb-27649/mw-1000/images/help/writing/nested-list-example-2.webp)

For more examples, see the [GitHub Flavored Markdown Spec.](https://github.github.com/gfm/#example-265)


> Please stay tuned for updates.

# Learning Record
  
Starting time: 2023-04-09
  
Ending time: 

What I learnt: 



