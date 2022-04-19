# APA-Word-Template

A Microsoft Word template for creating documents in APA 7 format.

## Updates

See the changelog for updates or the GitHub issues for the development pathway.

Issues and PRs are welcomed.

# How to Use

## Initial Install

Download the template into your User templates directory, or any convenient location. Double-click the template to create a new blank document using the template.

# Issues

## Heading 4 and Heading 5

These styles are inlined in APA. (Really, who invents this stuff?) Anyway, that means you'll have to use character styles for them, but you can also choose the template's `Heading 4` and `Heading 5` experimental styles which are -- not kidding -- embedded in frames. You'll have to make the first paragraph after these styles `Body Flush`.

## Widows and Orphans

APA style does not have a problem with widows and orphans. That is, a heading can be the last line of a page, and a sentence can end in the first line of a new page. The justification for this is that these are presentation considerations, and APA is all about preparing an article to submit to a journal. The journal itself will handle all these little details for you.

But... it looks pretty stupid. I've put an on/off switch for widows an orphans on the development pathway.

## Paragraph After Block Quotes

In APA, the first paragraph of a section should not differ from any other paragraph. However, the first paragraph after block quotes (style: `Block Text`) is (usually) a continuation of the paragraph from before the block. A style `Body Flush` exists for that 

## Playing Nicely

There are some packages (like Writage, that allows you to paste markdown; and pandoc) that create certain styles by default. These are handled by creating synonyms. Here are the examples and how they are handled:

| package | style issue |
| - | - |
| pandoc | If you have a `title` value in the file's frontmatter, it will be added to your final document with style `Title`, which has been created as a synonym to `Title Page Title`. If you're writing a manuscript with sections, however, you probably want this to be `Header 1`. (The best practice is probably not to use a `title` in your frontmatter; just include headings in the text.) |
| pandoc, Writage | These packages create a `First Paragraph` style; in this template is is considered a synonym for `Body Text`. See the note above about block quotes, however. |