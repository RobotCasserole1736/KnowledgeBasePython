---
layout: mainPage
---

# Python Basics

Python is a high level dynamically typed language which is widely used for data analyics, processing, machine learning, and automation scripts. The rest of this page will break down what each part of that means. <!-- Do students new to programming need to know this? -->

## High Level vs Low Level

What is a high level language? What makes one high level? A high level language is one that is designed, primarily, for human readabiliy ([https://en.wikipedia.org/wiki/High-level_programming_language]). A high level language may read like a sentence, and needs to be translated into the actual 1's and 0's that the computer itself understands. Soem popular high level languages are JavaScript, Java, and of course, Python.

On the opposite end of the spectrum, you have low level languages. These are your C, C++, Rust, and Fortran's of the world. They forego human readability in favor of more direct, and faster, processing. The speed increase comes from the or fewer number of translation layers - low level languages only need a few steps to be binary.

Pop quiz, what is the lowest level language? At its core, all computers run in binary and every program needs to be translate into binary to be run. However, binary isn't really a language, you can't (realistically) program anything in binary. So, to clarify the question, what is the lowest level language that can actually be written in? The answer to that is assembly. Assembly is one step above binary, and directly relates to the physical processor running the code. Different physical differences in processors necessitate different assembly code, which is a can of worms that will be covered on a different page. Just know that if you want things to be as fast as computerly possible, assembly is what you use.

## Typing: Dynamic vs Static

No, not typing as in typing on a keyboard. Type in programming refers to what a certain piece of data is - is it a number, text, true/false, or something else? It's kinda like the shape of the data, it defines what can fit into that bucket and how it can be used.

Static typing is when the type (shape) of the data is set by the programmer explicitly. That data can only be that one shape, and trying to shove a different shape into it will cause problems. For example, defining data `x` to be a number, I can assign it the value `1`. But if I try to assign itt `"cake"`, there will be an error because "cake" is not a number. And if I take `x` (currently `1`) and try to add `"1"` (the actual character `"1"`, not the number), it will also error.

Dyamic typing is a lot looser. Types still exist, but they are not defined ahead of time. The data takes the shape that is needed at the time and can be changed on the fly. Instead of defining `x` to be a number, `x` is just defined as data. `x` can be assigned to `1` with no issues. If `x` is then assigne to `"cake"`, the type of `x` will change to text. The value of `x` will be `"cake"` even though it started as a number. Now, let's set `x` back to `1` and see what happens when we try adding `"1"`. We get `"11"`! Errors like this in a dynamically typed language are more common as the computer won't check to ensure the data has the right shape before using it.

## Using Python <!-- Do we want our own tutorials for general python or just for the tools/libraries that we use --> 
<!-- https://github.com/RobotCasserole1736/OffseasonTraining/blob/master/Chapter_1/readme.md -->

So, now that we know what Python is, lets write out first program. For now we will assume that you have WPILib VSCode installed. If you need to install WPILib VSCode, click [here.](https://frcdocs.wpi.edu/en/2020/docs/getting-started/getting-started-frc-control-system/wpilib-setup.html#:~:text=Download%20the%20appropriate%20installer%20for%20your%20Windows%20installation,installer%20is%20extracted%20before%20attempting%20to%20run%20it.) 