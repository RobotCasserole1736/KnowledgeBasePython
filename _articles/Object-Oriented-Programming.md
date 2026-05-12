---
layout: page
name: Object Oriented Programming
topic: Python
updated: April 30 2026
articleBefore: Python Basics
articleAfter: Inheritance and Polymorphism
---

{% include articleHead.md %}

## OOO: What is Object Oriented Programming: The Short Version

Object Oriented Programming: A way to structure code such that distinct functionalities are contained within their own Objects. That is a lot of words to say, simplified, things that need to be used together are together in code. Objects in code are defined in Classes (not the school kind).

## OOO: What is Object Oriented Programming: The Long Version

When baking cookies, you don't put everything into a bowl at once, mix it, and use the sun to bake the dough in the bowl. If you do, those must be some funky cookies. Cookies require multiple different tools, or *objects*, when being made. Each object has its own purpose, and the logic to run that purpose: an oven bakes things and knows how to do that. A bowl holds things, and knows how to do that. But a bowl doesn't know how to bake, so it cannot. Now to turn this cookie analogy into code: an Object (capitalized for emphasis) is a tool that has a purpose, and contains the logic and data required to do that purpose. An Object called "ScreenColorChanger" has the purpose of changing the color of the screen, and would contain the logic to do so when called.

Now for the hard part: Objects within Objects. Back to cookies (go bake some after reading this), an oven does bake things. But the oven itself is also made up of pieces that have their own, more specific purposes. The coils that produce heat, the temperature sensor that reads how hot the inside is, the display that tells the humans how hot it is, and many many more. Objects in code, same thing. The ScreenColorChanger does know how to change the color of the screen, but it is made up of smaller parts that have more specific tasks. One Object contained within could be "PixelColorChanger" - an Object whose sole purpose is to change the color of a single pixel on the screen. ScreenColorChanger doesn't know how PixelColorChanger does its thing, all the ScreenColorChanger needs to know is that PixelColorChanger works and by telling it "Blue" that pixel is now blue. This nesting of Objects within Objects can go quite deep, though there are practical limits - the more Objects the more things need to be kept track of at once by the programmer and the more memory is used on the computer.

That PixelColorChanger Object seems useful... Good thing it can be used elsewhere outside of ScreenColorChanger too! Objects are not bound to only being used in one place - they can be used aywhere their definition can be found (for better or worse, this can lead to massie spaghetti). Lets add a new Object to the pile here: "ImageRenderer". Rendering an image to the screen does require changing the color of pixels, so we will include PixelColorChanger in ImageRenderer - no need to rewrite that same code if we aready did for ScreenColorChanger! 

This does bring up a question though: are the PixelColorChangers in ScreenColorChanger and ImageRenderer the same Object? The answer......... no! They are not the same Object! Every time you use an Object you are making a new Instance (again, capitalized for emphasis) of it. Each Instance uses the same template (the Object you wrote), but the values contained within are entirely disconnected (yes, person who said "static", we will get to that). Lets use cars as the analogy this time, I'm no longer hungry. If you and your friend both by the exact same model, color, and trim of 2002 Honda Civic, you did not buy the same car. You sitting and driving your car has no effect on your friend doing the same in theirs - the same thing applies with Objects and their Instances. Each Instance is separate from the others, but is spawned off the same base template. In general, an Object can have as many Instances as you want, right up until your computer crashes from being out of memory.

Now it is time for the excepions to the rules. Starting with the second most recently mentioned: each Instance being entirely separate from the others. That's not entirely true if you use something called a static variable. Statics contain the same value across all Instances - this can be useful for things that need all Instances to have the same information and there is no other way to reach it. The next exception is Objects having as many Instances as you want - unless you have what is called a Singleton. Singltons are Objects where only one Instance can exist at a time. The wonderful third exception: thats all folks there isn't a third.