---
layout: page
name: Modifying The Recipe Book
subject: The Recipe Book
updated: Dec 7 2025
articleBefore: none
articleAfter: Recipe Book Tools
---

{% include articleHead.md %}

This article is currently intended for Robot Casserole students. If you are not a member of Robot Casserole, we encourage you to submit a pull requests to modify any of our software. This article also assumes you are working with windows, so if you are using MacOS or Linux you may need to tweak a couple commands.

In order to test your modifications, you are going to need to have some tools installed. Please navigate to [this link](https://jekyllrb.com/docs/installation/) and follow the instructions to install and configure Jekyll. Do not worry about downloading GCC or Make, Jekyll should work for our purposes without them. 


Once you have completed installing Jekyll, pull the commit you would like to work from or make a new branch. Please refrain from working on Main, as that branch is what the webpage is based on and it is best to have your work reviewed by a mentor and availble in a seperate commit outside of main just in case there is an error.

Open the command prompt and navigate to the KnowledgeBasePython folder (using the `cd` command). Then, run `gem install github-pages` . 

Now, modify the code as you need. I will add instructions on how to add pages or topics soon.

Once you are ready to test your code, open the command prompt and navigate to the KnowledgeBasePython folder again. Once there, run `bundle exec jekyll serve` which will compile your page at http://localhost:4000/. To view your page, navigate to http://localhost:4000/ in your web browser. Whenever you save a change, Jekyll will automatically recompile the change and update the page, so just refresh to see your changes. To stop viewing the page, navigate to the terminal and hit ctrl+c and type `y` and hit enter when prompted to terminate batch job.

Note - use spaces in article name variables but use dashes in file names