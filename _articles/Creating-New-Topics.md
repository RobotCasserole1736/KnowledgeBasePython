---
layout: page
name: Creating New Topics
topic: The Recipe Book
updated: Dec 21 2025
articleBefore: Writing Articles
articleAfter: Recipe Book Tools
---

{% include articleHead.md %}

{% assign codeExample = "{% include topicContents.md " %}

### Creating new topics

To create a new topic start by creating a new markdown file in the `_topics` folder. Use dashed whenever you would normally use spaces for the file name. Your new markdown file will have two components, the front matter and a single line of code. The front matter for topics should look something like this:

```
---
layout: page
name: The Recipe Book
desc: Information about the recipe book, including guides on modifying articles, adding categories, and a (hopefully) simple overveiw about the tools we use for curious software students.
---
```

These should be pretty self-explanatory, but here's what each of these mean and how to format each:
- `layout` - This is used by jekyll to determine how the page will look. This should always be "Page"
- `name` - The name of the topic. Here you should use spaces. Other than that, make sure it matches the file name and that there are no typos.
- `desc` - A description of what the topic will cover. 

After the front matter, you should paste the following line of code:

`{{ codeExample }}%}`
> Note: If you are looking at the source code for this page, you will notice it says something completetly different than what the rendered markdown displays. This is intentional. Copy the example from the rendered website.

This line ensures that the code responsible for organizing each topic's contents gets run. From here, everything else should be taken care of by Jekyll and our team's preexisting code. 