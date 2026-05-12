---
layout: page
name: Inheritance And Polymorphism
topic: Python
updated: April 30 2026
articleBefore: Object Oriented Programming
articleAfter: none
---

{% include articleHead.md %}

## Two Large Words

Inheritance, not the kind when someone passes away, is when an Object can Inherit the properties of another one.
Polymorphism, try saying that 3 times fast, is when an Object that Inherited properties can be transformed into its parent Object.

## Two Large Explanations Part 1: Inheritance

The name actually lends itself quite well to the analogy here: Person A is the child of Person B, who is in turn the child of Person C. Here is a visual:
C --> B --> A
In typical, real world inheritance, C's assets go to B, which then go to A. Only one person at a time has them. In code, the same idea applies but the ownership is not exclusive. Let's apply some properties to A, B, and C:
### C
- Favorite Cheese
- Lease Favorite Cheese
### B
- Name of Pet Duck
### A
- Aglet Color
- Shoe Sole Material

OK, now that everyone has properties, lets demonstrate programmatic inheritance!
C, the highest level of this inverse pyramid, only has the two properties directly on them: Favorite and Least Favorite Cheese (Gouda and Provolone respectivley). Easy so far
B, the middle layer has access to its properties, Name of Pet Duck (Gerald), and the two of the Object they inherit from, Favorite and Least Favorite Cheese (Calderwood and Kunik respectivley).
A, the last in the chain, has access to all thos above in addition to its own. Favorite Cheese, Oma. Lease Favorite Cheese, Verano. Name of Pet Duck, Subaru. Aglet Color, neon pink. Shoe Sole Material, depleted uranium.

An Inheriting Object gains access to all (pin here for the exceptions section!) properties of those it Inherits from, all the way up the chain to the top. The final thing to note with Inheritiance is an Object can (typically) Inherit from one other Object at a time - Python allows this, it will be touched on later.

## Polymorphism

It's time for the scarier word! Polymorphism is a *very* fancy way of saying that an Object that Inherits from another Object is that other object. This is best phrased as such: A 2002 Honda Civic IS A car IS A vehicle. The Inheritance chain here is:
Vehicle --> Car --> 2002 Honda Civic
Polymorphism doesn't change anything about Inheritance, so all the Inheriting rules above apply. It instead extends it: Lets have our pretend 2002 Honda Civic get some cleaning. We take it first to a 2012 Toyota Corrolla Wash. No luck, a 2002 Honda Civic is not a 2012 Toyota Corrolla, we'll need to go somewhere else. Now we find a Car Wash. Ah, we are in luck! A 2002 Honda Civic IS A car, so it can go into the Car Wash! As we enter, we also see a 2012 Toyota Corrolla exit, - a 2012 Toyota Corrolla IS A car as well. Now lets trade in the newly cleaned car for a brand new 7000 Series L Train from Chicago. This thing also needs cleaning, so we take it to the Car Wash - a Train IS NOT A Car, so no dice. We are in luck though, we find a Vehicle Wash! A Train IS A Vehicle, so this great 7000 Series can get clean. As can the Plane that entered after.

Directly applying to code, any Object that Inherits from another Object is the other object - its Type is both its own (2002 Honda Civic), and the Inherited Type (Car). This means a variable of type Car can hold any Object that Inherits Car, regardless of what its specific make or model is. The catch, as there always is one, is only properties that all Cars have are accessible - without knowing if you have the features of a Bugatti Veyron or Model T.

## Exceptions

They always exist. Starting with multiple Inheritance - Python does allow this to happen. Some languages don't (ex. C#, Java), some do (ex. Python, C++). The same principles apply with multiple Inheritance as with single Inheritance, the child Objects just get more properties and can be Polymorphed into more things.

Next on the chopping block, what actually gets Inherited. When declaring a variable or function in a Class, you can define a privacy level: public, protected, or private (there are more than this, but these are by far the most common and least confusing). Public means anyone can access this property, both from within the Object and from outside via an Instance. Protected means only the Object and those that Inherit from it can access that property, it is not available in the Instance. Lastly, private means only that Object can access it, not Inheriting Objects, not Instances.