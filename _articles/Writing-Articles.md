---
layout: page
name: Writing Articles
topic: The Recipe Book
updated: Dec 21 2025
articleBefore: Modifying The Recipe Book
articleAfter: Creating New Topics
---

{% include articleHead.md %}

{% assign articleHeadExample = "{% include articleHead.md" %}

{% assign articleLinkExample = "[What the user sees]{% link _articles/Creating-New-Articles "%}

{% assign articleImageExample = "![Text describing image]{% link /assets/hat.png " %}

### Article Code Layout

There are 3 main parts of the code for our article pages. The front matter, article head, and article body. The front matter declairs the values of certain attrabutes for that page and is always surrounded by three dash (-) characters before and after. Here's an example of what the variable declerations in the front matter for this page look like: 

```
---
layout: page
name: Writing Articles
topic: The Recipe Book
updated: Dec 21 2025
articleBefore: Modifying The Recipe Book
articleAfter: Creating New Topics
---
```

Here's what each of these mean:

 - `layout` - This is used by jekyll to determine how the page will look. This should always be "Page"
 - `name` - This is the name of your article. The file name and article name should be the same except the spaces in the article name variable should be replaced by dashes for the file name. The file name should also end in .md to indicate a markdown file.
 - `topic` - This is what your article is about. Make sure that this exactly matches the name of the topic as defined by its file in the _topics folder. More information can be found at the [Creating New Topics article]({% link _articles/Creating-New-Topics.md %})
 - `updated` - When the article was last updated. Sadly this must be changed manually. Sorry about that. Also try to keep the format consistant, month day year (no commas).
 - `articleBefore` - What article came before this one. Like with `topic` this must be an exact match. Set its value to `none` if it is the first article.
 - `articleAfter` - What article comes after this one. Like `articleBefore` this must be an exact match and set its value to `none` if this is the last article. 

For the article head, simply paste the following line of code after the front matter:

`{{ articleHeadExample }} %}`
 > Note: If you are looking at the source code for this page, you will notice it says something completetly different than what the rendered markdown displays. This is intentional. Copy the example from the rendered website.  
 
The article body is where the contents of the article go, put all of the cool things there!

### Some tricks. 

Linking to other articles with markdown and liquid is really easy. For example, linking to this article would look like so:

[What the user sees]({% link _articles/Writing-Articles.md %})

`{{ articleLinkExample }} %})`

If you are linking to a seperate website, replace everything inside the parentheses with just the link to the website.

Displaying images is also easy. Here is another example:

![Text describing image]({% link /assets/hat.png %})

`{{ articleImageExample }} %})`

Of course replacing the links to each article/image with the one you would like to link to.

For more information on markdown, use [this very handy cheatsheet](markdownguide.org/cheat-sheet/).
For more information on Liquid (the tool that does a lot of the handy code stuff) visit [the official liquid website](shopify.github.io/liquid) or for a brief introduction to Liquid for Jekyll check out [Jekyll's guide](jekyllrb.com/docs/liquid).