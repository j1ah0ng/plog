# plog

Clauding! The task is to build and deploy tooling to display writing in a blog-like website. The user flow:

## Publishing blog posts

A file (perhaps markdown, it's not clear what the best choice is) is published to the repository. It may contains inline LaTeX, express support for footnotes, hyperlinks, images, etc., or even rich interactive content, such as d3.js views, or Plotly graphs. 

## Display

By some means (e.g. upon CI or something else) the raw post files are serialized to a page which has the look and feel of LessWrong, or Thinking Machines' blog posts. We would like a similar respect for the reader - in terms of wide margins, helpful footnote displays, a beautiful serifed font. 

### Website structure

We would like a simple directory page which displays and list the available posts by date.

### Post display page

Here is the most important part. When displaying each page, we want a rich but focused experience for the user. The sidebar should provide a vertical "timeline" of the post (e.g. lists out headers and subheaders, important footnotes, images) and indicate vertically where the current scroll view is in the page. We want wide margins when viewed on desktop. Footnotes should be displayed alongside the page, in the margins. The reading experience must not be impaired; we want to present information in as pleasant a format as possible so as to encourage flow state.
