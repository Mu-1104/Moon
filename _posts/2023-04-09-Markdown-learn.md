---
layout: post
title: "M's Markdown Learning Log"
date: 2023-04-09
excerpt: "This is a collection of resources about Markdown"
tags: [Markdown, CS]
comments: true
---


# Learning Resources

* [the Markdown official website](https://daringfireball.net/projects/markdown/) 

* [GitHub's Markdown guide](https://guides.github.com/features/mastering-markdown/)

* Check out Markdown tutorial websites:
  - [Markdown Tutorial](https://www.markdowntutorial.com/) 
  - [Learn X in Y minutes](https://learnxinyminutes.com/docs/markdown/)
  - [Markdown 官方教程](https://markdown.com.cn/)
  - [Markdown 菜鸟教程](https://www.runoob.com/markdown/md-tutorial.html)
  - [Awesome Markdown](https://github.com/mundimark/awesome-markdown)

* Download Markdown editors for practice: 
  - [Typora](https://typora.io/)
  - [StackEdit](https://stackedit.io/)
  
* Explore online Markdown editors:
  - [Dillinger](https://dillinger.io/)
  - [Markdown Live Preview](https://markdownlivepreview.com/)
  
# Excerpts 

> From [Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

## Headings

```
# A first-level heading
## A second-level heading
### A third-level heading
```

![](https://docs.github.com/assets/cb-43514/mw-1000/images/help/writing/headings-rendered.webp)

## Styling text

Indicate emphasis with **bold**, _italic_, ~~strikethrough~~, ***all bold and italic***, <sub>subscript</sub>, or <sup>superscript</sup> text in comment fields and .md files.

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

Text that is a quote

`> Text that is a quote`

![](https://docs.github.com/assets/cb-30028/mw-1000/images/help/writing/quoted-text-rendered.webp)

> Tip: When viewing a conversation, you can automatically quote text in a comment by highlighting the text, then typing R. You can quote an entire comment by clicking , then Quote reply. For more information about keyboard shortcuts, see "[Keyboard shortcuts](https://docs.github.com/en/get-started/using-github/keyboard-shortcuts)

## Quoting code

Use \`git status\` to list all new or modified files that haven't yet been committed.

![](https://docs.github.com/assets/cb-34564/mw-1000/images/help/writing/inline-code-rendered.webp)

Some basic Git commands are:

\```

git status

git add

git commit

\```

![](https://docs.github.com/assets/cb-53043/mw-1000/images/help/writing/code-block-rendered.webp)

> For more information, see ["Creating and highlighting code blocks."](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks)
>
> If you are frequently editing code snippets and tables, you may benefit from enabling a fixed-width font in all comment fields on GitHub. For more information, see ["About writing and formatting on GitHub."](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/about-writing-and-formatting-on-github#enabling-fixed-width-fonts-in-the-editor)

## Images

\!\[Alt\](https://myoctocat.com/assets/images/base-octocat.svg)

![](https://myoctocat.com/assets/images/base-octocat.svg)

> GitHub supports embedding images into your issues, pull requests, discussions, comments and .md files. You can display an image from your repository, add a link to an online image, or upload an image. For more information, see ["Uploading assets."](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#supported-color-models)
> 
> Tip: when you want to display an image that is in your repository, use relative links instead of absolute links.

### Here are some examples for using relative links to display an image.

| Context  | Relative Link |
| :------------ |:-------------|
| In a `.md` file on the same branch  | `/assets/images/electrocat.png`     |
| In a `.md` file on another branch   | `/../main/assets/images/electrocat.png`|
| In issues, pull requests and comments of the repository | `../blob/main/assets/images/electrocat.png?raw=true`|
| In a `.md` file in another repository | `/../../../../github/docs/blob/main/assets/images/electrocat.png`|
| In issues, pull requests and comments of another repository| `../../../github/docs/blob/main/assets/images/electrocat.png?raw=true`|

> Note: The last two relative links in the table above will work for images in a private repository only if the viewer has at least read access to the private repository that contains these images.
> 
> For more information, see ["Relative Links."](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#relative-links)

## Lists

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

```
1. First list item
   - First nested list item
     - Second nested list item
```

> Note: In the web-based editor, you can indent or dedent one or more lines of text by first highlighting the desired lines and then using Tab or Shift+Tab respectively.

![](https://docs.github.com/assets/cb-27649/mw-1000/images/help/writing/nested-list-example-2.webp)

> For more examples, see the [GitHub Flavored Markdown Spec.](https://github.github.com/gfm/#example-265)

## Task lists

To create a task list, preface list items with a hyphen and space followed by [ ]. To mark a task as complete, use [x].

```
- [x] #739
- [ ] https://github.com/octo-org/octo-repo/issues/740
- [ ] Add delight to the experience when all tasks are complete :tada:
```

![](https://docs.github.com/assets/cb-64629/mw-1000/images/help/writing/task-list-rendered-simple.webp)

If a task list item description begins with a parenthesis, you'll need to escape it with \:

` - [ ] \(Optional) Open a followup issue `

- [ ] \(Optional) Open a followup issue

> For more information, see  ["About task lists."](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/about-task-lists)

## Uploading assets

You can upload assets like images by dragging and dropping, selecting from a file browser, or pasting. You can upload assets to issues, pull requests, comments, and `.md` files in your repository.

## Using emoji
You can add emoji to your writing by typing :EMOJICODE:, a colon followed by the name of the emoji.

`@octocat :+1: This PR looks great - it's ready to merge! :shipit:`

![](https://docs.github.com/assets/cb-28666/mw-1000/images/help/writing/emoji-rendered.webp)

> For a full list of available emoji and codes, see the [Emoji-Cheat-Sheet.](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)

## Paragraphs

You can create a new paragraph by leaving a blank line between lines of text. 

## Footnotes

You can add footnotes to your content by using this bracket syntax:

```
Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].

[^1]: My reference.

[^2]: To add line breaks within a footnote, prefix new lines with 2 spaces.
  This is a second line.
```


The footnote will render like this:

![](https://docs.github.com/assets/cb-59577/mw-1000/images/help/writing/footnote-rendered.webp)

> Note: The position of a footnote in your Markdown does not influence where the footnote will be rendered. You can write a footnote right after your reference to the footnote, and the footnote will still render at the bottom of the Markdown.

## Hiding content with comments

You can tell GitHub to hide content from the rendered Markdown by placing the content in an HTML comment.

\<!-- This content will not appear in the rendered Markdown --\> 

<!-- This content will not appear in the rendered Markdown -->

## Ignoring Markdown formatting

You can tell GitHub to ignore (or escape) Markdown formatting by using \ before the Markdown character.

` Let's rename \*our-new-project\* to \*our-old-project\*. `

![](https://docs.github.com/assets/cb-16282/mw-1000/images/help/writing/escaped-character-rendered.webp)

> For more information on backslashes, see Daring Fireball's ["Markdown Syntax."](https://daringfireball.net/projects/markdown/syntax#backslash)

## Disabling Markdown rendering

When viewing a Markdown file, you can click  at the top of the file to disable Markdown rendering and view the file's source instead.

![](https://docs.github.com/assets/cb-36071/mw-1000/images/help/writing/display-markdown-as-source.webp)

Disabling Markdown rendering enables you to use source view features, such as line linking, which is not possible when viewing rendered Markdown files.

# Further reading

* [GitHub Flavored Markdown Spec](https://github.github.com/gfm/)

* ["About writing and formatting on GitHub"](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/about-writing-and-formatting-on-github)

* ["Working with advanced formatting"](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting)

* ["Quickstart for writing on GitHub"](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/quickstart-for-writing-on-github)

# Learning Record
  
Starting time: 2023-04-09
  
Ending time: 2023-04-10

What I learnt: 

* [Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) 

* [Organizing information with tables](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/organizing-information-with-tables)

* [Organizing information with collapsed sections](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/organizing-information-with-collapsed-sections)

* [Creating and highlighting code blocks](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks)

* [Awesome Markdown](https://github.com/mundimark/awesome-markdown)

# Others

Just wanna speak out, I wrote this blog using Markdown!
