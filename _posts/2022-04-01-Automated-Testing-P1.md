# Automated Testing - Part 1

*You don't **need** to read this bit, but it does give you a good idea of what Automated Testing is, why we do it, benefits of Automated Testing and all that other good stuff. But like I said, you don't **have** to read it - you can just skip to Part 2 of the series...* 

---
###### [Automated Testing P2: Introduction to Selenium](/_posts/2022-04-01-Automated-Testing-P2.md)
---

## Here is where we are...
We have new releases of the software being released every 4 weeks. We are supposed to Regression Test each release as it comes out. The client expects the Testing Team to find **all** bugs during the testing - every time! The bottom line is that it takes a team of three testers roughly 2 days (about 48 man hours) to execute the testing. However even the Testing Team is human...and humans make mistakes. This is where **Automated Testing** comes in...

## What is Automated Testing
**Automation Testing** is a software testing technique that uses special automated testing software tools to execute a test case suite (*just a fancy way of saying a bunch of grouped tests*). On the other hand (*Darryl*), **Manual Testing** is performed by a human sitting in front of a computer carefully executing the test steps - hopinng that there is no new features that have been added, which have secretly broken something that *was* working! 

The automation testing software can also (sometimes, if configured correctly) enter test data into the System Under Test (SUT), compare expected and actual results and generate detailed test reports. However software test automation demand **considerable investments** of money and resources - which is why the Test Team is always under pressure to complete the test coding *yesterday* (*everything seemed so far away...*).

Any successful development cycle will require execution of the same test suite repeatedly. By using a test automation tool, it’s possible to 'record' this test suite and re-play it as required. Once the test suite is automated, no human is required - so make sure about your union rules. This improves the ROI of Test Automation. The ultimate goal of Test Automation is to reduce the number of test cases to be run manually, limit mistakes (by tired (or hungover) humans) and **not** to eliminate Manual Testing altogether.

## Why automate your tests? Isn't this like torturing ourselves more?

![why](/docs/assets/images/why.jpg)

**No! This has nothing to do with S&M!**

**Test Automation** is the ***best*** way to increase the effectiveness, test coverage, and execution speed of software testing. Automated software testing makes sense due to some of the following reasons:

- Manual Testing of all workflows, all fields, all negative scenarios is time and money consuming (read, long & mind-numbing)
- Test Automation in software testing does not require human intervention. They can run unattended (no humans required) = even at 2 a.m (no complaining about working overtime!)
- Test Automation increases the speed of test execution (practical experience shows a day's manual testing completed in just over 4 minutes!)
- Automation helps increase Test Coverage
- Manual Testing can become boring and hence error-prone

## OK. So how do we do this thing?

![how](/docs/assets/images/how.png)

The following steps are generally followed. 
1. Test tool selection
2. Define the scope of automation
3. Planning, design and development
4. Test execution
5. Maintenance

I'm not going to go into lengthy details of each - that's why Google is your best friend - and besides, this post is getting pretty long already.

### Test tool selection

This is where you select the automation software testing tool that you will use. This should be based on the type of application that you're going to test. Not *all* testing tools do the same thing! **It is a very good idea to perform a Proof of Concept** first. 

### Define the scope of automation

This is where the parts of the application to be tested is defined. Sometimes there isn't enough time (or money) to automate everything at once! Consider the following points when deciding the scope of work:

1. What features are most important to the business?
2. What sort of scenarios are there where you will need to use **large amounts of data**?
3. **Common functions** in the application that can use the same test (albeit with different data)
4. How feasible is it to automate a test? - complex tests require too much of effort = too much time = too much money
5. Can you use the same test for cross browser testing? Different browsers might be used - even within the same site!

### Planning, design and development

Here is where you create an Automation strategy (AKA a plan), where you decide the following:

1. What tool are we going to use?
2. What features does this tools have?
3. What is *In-Scope* and *Out-Of-Scope*?
4. Preparing your machines for testing
5. Set up a timeline for scripting and execution
6. What are the deliverables? How do we know that the job is done?

### Test execution

This is where we execute the plan (Go Testing Team AKA The A-Team!). Remember sometimes you might have to agree (and set up test data) before the tests can be executed. Once executed we would need a detailed Test Report - how else will you know what tests passed or failed? 

The test execution can be performed by the automation tool itself or through a Test Management tool (like Azure DevOps) which will invoke the automation tool e.g. a DevOps pipeline can be configured to execute the tests for you at 2 a.m when no-one is around to interfere!

### Test Maintenance

![how](/docs/assets/images/maintain.jpg)

This is when the Testing Team have to write new (automated) tests to check that any new functionality introduced in any new release **is** working as expected. The team needs to remember to ensure that these tests are written and included in the overall Test suites.

## Conclusion

Automated Testing is a software testing technique that allows tests to be run without human intervention. It increases the effectiveness, quality and speed of testing. It is important to define the scpe of testing and the definition of *done*. Constant maintenance will be required to ensure that any new features are tested as they are released.

So now that we have a decent idea as to ***WHY*** we need automated testing, lets start with ***HOW*** you would actually perform some Automated Testing. 

***Testers, get ready to code...***
