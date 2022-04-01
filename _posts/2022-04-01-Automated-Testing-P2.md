# Automated Testing P2 - Introduction to Selenium

*You don't **need** to read this bit either, but it does give you a good idea of what Selenium is, Selenium components, the benefits of using Selenium and all that other good stuff. But like I said, you don't **have** to read it - you can just skip to [Part 3](/_posts/2022-04-01-Automated-Testing-P3.md) of the series...* 

---
###### [Automated Testing P1: What is Automated Testing](/_posts/2022-04-01-Automated-Testing-P1.md)  
###### *Automated Testing P2: Introduction to Selenium*  
###### [Automated Testing P3: A quick look at the Selenium IDE](/_posts/2022-04-01-Automated-Testing-P3.md)
---

## So what is this Selenium thing anyway?
We all know that testing our software is an integral part of the software development cycle, and sometimes it involves a lot of repetitive tasks (read performing some tasks over and again). So there was a need for something (some kind of tool) that could help software testers to automate these repetitive tasks. No more slogging through Regression Testing scripts over and over! ***YAY!*** One of these brilliant automation tools is **Selenium**, which allows us to automate user actions on a web application. What's better, is that it is open-source (**FREE** so your client will be ecstatic!) software that enables and supports the automation of web browsers.

<img src="/docs/assets/images/seleniumlogo.jpg" alt="Selenium Logo" width="100"/>

## An overview of Selenium Testing 
As I said above, Selenium is an open source web automation tool. However it is not just a single product - it is a suite of products:

- Selenium IDE
- Selenium RC
- Selenium WebDriver
- Selenium Grid

But, in our case we will be focussing **one** of the tools viz. **Selenium WebDriver*. We will have a brief look at the *Selenium IDE* as well, but we will not delve too deeply into the latter. What Selenium does does, is that it leverages the power of web browsers and allows us to *"automate the workflow of how a user interacts with a web application within a browser"*. Simply put, it decieves the browser into believing that there is an actual human performing operations in the web application. *Cool huh?*

## The components of the Selenium suite (that are important to us)

<img src="/docs/assets/images/SeleniumComponents.png" alt="Components of Selenium" width="500"/>

### Selenium IDE

***Selenium IDE*** is a web Extension that is available for the Chrome, Firefox and Edge Browsers. It can be installed into your browser from the relevant Web Stores. The IDE has the ability to record and replay a set of actions that a user performs in the browser - just like the macro recording facility in some of the Microsoft Office suite of tools. It also has the ability to export said recordings as code (in various languages e.g. C#, Java and Python). It also allows for the use of test cases within another.

### Selenium WebDriver

***Selenium WebDriver*** is the most often used component in the *Selenium* seuite of tools. ***This*** is what we are really interested in. *WebDriver* allows us to write custom code in our language of choice (in this case C# - *sorry Java, Python and other language afficionados - though porting the code is not too onerous*) which can interact with our browser of choice, using browser specific drivers. 

Yeah. I know that right now you're going *"Huh?"*. Think of it this way, WebDriver acts as a sort of interpreter. We write some code in C# and WebDriver takes that code and translates it into something that the browser can understand. Then the browser does whatever WebDriver tells it to do, and when the browser does something, WebDriver then tells our code what the browser did! Like a spy puppet-master (boo ha ha, boo ha ha <- that is supposed to be an evil laugh by the way...) 

## What can it do for me?

There was a song (from the 80's, I think - giving away my age here) the had this line *"What can you do for me?"* and just like the song, what can *Selenium* do for us?

- **Open Source** – it is open source, which means that there is no cost to set up and use Selenium. Just download and use it
- **Mimic User Actions** – Almost every real-world user actions e.g. button click, drag, drop-down selection, checkboxes, keypresses, taps and scrolling, can be automated.
- **Easy Implementation** – it is user friendly. You don't have to be a coding god to write automation tests using *Selenium*.
- **Language Support** – it supports various programming languages. C#, Java, Python, JavaScript, Ruby, Perl, Haskell and Go, among others.
- **Browser Support** – it can work on most of the different browsers that are out there. *Selenium* has support for Chrome, Firefox, Edge, Internet Explorer, Safari, etc.
- **OS Support**  – bindings are available for all the primary OS's like Windows, Linux and macOS.
- **Framework Support** – *Selenium* supports multiple frameworks like NUnit, Maven, TestNG, PYTest, Mocha, Jasmine, etc. It also integrates well with CI tools like Azure DevOps, Jenkins, Circle CI, GOCD, Travis CI, Gitlab, etc.
- **Code Reusability** – the scripts written for *Selenium* are cross-browser compatible i.e. the same code can be run for multiple browsers using the respective browser binaries (don't worry, we'll go into that later),

## What's the catch?

While *Selenium* is one of the best test automation tools, it is not without it's flaws. We will cover these during the course of this series.

## Do I have what it takes?

<img src="/docs/assets/images/whatittakes.jpg" alt="Do you have what it takes?" width="200"/>

I know by now you're wondering if you have what it takes to actually get started with *Selenium*? If it can do so many things, it **must** be difficult. However, even if you have no knowledge of *Selenium*, you will be able to get the basics within a few hours. You will find it a lot easier if you hae some knowledge of the following:

- the basics of Manual Testing
- knowledge of Coding in a programming language that is supported by *Selenium*
- basic knowledge of HTML & CSS
- basic knowledge of XML and JSON
- understand the DOM and identifying a web element using a locator in DOM

## Are we done yet?

***Congratulations!*** You now have a solid background in what *Automated Testing* is and what *Selenium* is. All that remains is for us to get stuck into it.  

#### Let's go...
