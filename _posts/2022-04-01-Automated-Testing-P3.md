# Automated Testing P3 - A quick look at the Selenium IDE

---
#### [Automated Testing P1: What is Automated Testing](/_posts/2022-04-01-Automated-Testing-P1.md)  
#### [Automated Testing P2: Introduction to Selenium](/_posts/2022-04-01-Automated-Testing-P2.md)
#### *Automated Testing P3: A quick look at the Selenium IDE*
---

## What is the Selenium IDE
The Selenium IDE (**I**ntegrated **D**evelopment **E**nvironment) is a plugin that has been developed to be used in various browsers. It was created to speed up the creation of automation scripts. This allows for quick prototyping of scripts and is easy enoug to be used by engineers with no programming knowledge whatsoever!

## So how does this thing work?
The IDE uses three stages:
- Recording
- Play back
- Saving  

Easy huh?

<img src="/docs/assets/images/selenium-working.jpg" alt="Selenium working principles" width="700"/>

### Recording
The IDE allows you to record all of the actions that you perform in the browser. All these (recorded) actions are saved as a test script.

### Playing Back
Once the recording is completed, it can be executed as often as you'd like. *"Why would I want to do that?"* - just to make sure that the script is making the browser do exactly what you expected it to do. Now you can measure the stability and succes rate of your test script.

### Saving
The recorded script can now be saved. The script is saved with a ".side" extension. Now you can run this script again and again for future regressions (and just to annoy your colleagues).

<img src="/docs/assets/images/pitfall.png" alt="Pitfall" width="50"/>

**<span id="pitfall-1">PITFALL:</span>** Like I said before, Selenium is not without its flaws. Sometimes when you save your test, it does two things:
- it saves it with an unintuitive name e.g. **0e0c5abd-2c69-4155-8477-f912f0c82892**. *WTF?*
- it sometimes saves the file without an extension i.e. there is no ".side" on the end - just **0e0c5abd-2c69-4155-8477-f912f0c82892**

<img src="/docs/assets/images/remember.png" alt="Remember" width="50"/>

**REMEMBER:** Once you save a recording as a script, check the name of the file in File Explorer. If it has a wierd name like **0e0c5abd-2c69-4155-8477-f912f0c82892**, give it a useful name like **open_google_homepage** and if it **is** missing an extension, add the ".side" on the end - like so: **open_google_homepage.side**. This way when you browse for the test script later on, the Selenium IDE will pick it up. *Hurray!*

## How do I install the IDE?
1. Open your Chrome browser.
2. Navigate to the [Chrome Web Store](https://chrome.google.com/webstore/category/extensions).
3. Type **Selenium IDE** in the *Search the store* input box.

<img src="/docs/assets/images/selenium-chrome-extension.png" alt="Selenium IDE in the Chrome Web Store" width="700"/>

4. Click the extension to install it. You will be presented with the Selenium IDE install page. Click the **Add to Chrome** button to install the extension.

<img src="/docs/assets/images/install-selenium-extension.png" alt="Install the Selenium IDE" width="700"/>

5. Click the **Add extension** button to confirm the installation of the extension.

<img src="/docs/assets/images/confirm-install.png" alt="Confirm the installation of the Selenium IDE extension" width="700"/>

6. Click the **Extensions** icon in the toolbar. In the pop-up that opens, click the **pin** next to the *Selenium IDE extension*. This will add the *Selenium IDE icon* to the toolbar.

<img src="/docs/assets/images/pinning-the-selenium-ide.png" alt="Pinning the Selenium IDE icon to the toolbar" width="300"/>

7. Now we're ready to rock-n-roll!

## Recording your first test

Now that we're done with installing the Selenium IDE, let's take it for a test run. Here is a simple use case. We're going to the Facebook site. Login using fake credentials. Check that the title is *"Facebook"*. If we break it all down, we get: 

- Navigate to https://wwww.facebook.com
- Provide a fake UserID and Password
- Log into Facebook using these credentials
- Assert the title of the application


<img src="/docs/assets/images/definition.png" alt="Definition" width="100"/> 

**DEFINITION:** *Um...what does **Assert** mean?* By definition, **Assert** is *"an expression, which encapsulates some testable logic specified about a target under test"*, which is a fancy way of saying ***check that some condition (that we want to check) is true***!

**Onward brave coders...!**

### Step 1 - Recording

1. Launch Chrome and open te Selenium IDE plugin (by clicking the icon in the toolbar)
2. Select **Record a test in a new project**. Provide a name for your test, and click **OK**.

<img src="/docs/assets/images/ide-demo-step-1.png" alt="Step 1" width="400"/> 

3. Next, enter the url (in the BASE URL input box) for the Facebook landing page. This url acts as the starting point for all subsequent navigation/actions in the test being recorded. Click the **START RECORDING** button. The IDE starts the recording by navigating to the web page.

<img src="/docs/assets/images/ide-demo-step-2.png" alt="Step 2" width="400"/>

4. Once the website opens, type in the fake UserID & Password into the relevant fields and click the **Log In** button.

<img src="/docs/assets/images/ide-demo-step-3.png" alt="Step 3" width="400"/>

<img src="/docs/assets/images/remember.png" alt="Remember" width="50"/>

**REMEMBER:** The fake log in details that you enter **have to be** valid credentials for this demo to work! Also note that you will see a notice at the bottom right corner that indicates thet the *Selenium IDE is recording*. 

<img src="/docs/assets/images/ide-demo-step-3-1.png" alt="Recording in progress" width="200"/>

5. Now, we can verify the title of our application. To do that, right click anywhere on the page body -> select the Selenium IDE link in the context menu that appears -> select the Assert link -> select the Title link. As soon as this is done, a test step would be appended in the IDE editor.

<img src="/docs/assets/images/ide-demo-step-4.png" alt="Step 4" width="200"/>

6. Now you can go back to the IDE editor and click on the **Stop** icon on the top right corner. Voila! We’ve successfully recorded our test case.
7. Once the recording is stopped, the Selenium IDE editor will look *...a little something like this...*[^1]

<img src="/docs/assets/images/ide-demo-step-5.png" alt="Step 5" width="700"/>

### Step 2 - Playing it back

Once the recording is done, we can play it back to verify that:
- the script executes properly
- the browser does exactly what we did

In order for us to do that, we...*click the **play** button* (on the main menu bar).

<img src="/docs/assets/images/ide-demo-step-6.png" alt="Step 6" width="700"/>

<img src="/docs/assets/images/pitfall.png" alt="Pitfall" width="50"/>

**PITFALL:** One of the most common mistakes that noobs make, is to **forget to log out** before they finish off the test. What ths actually does is that it leaves the test in an *"incomplete"* state. When you try and tun the test again, the script is going to look for the log in input box. But you're already (still) logged in! So it will never find the control that it needs. It will sit around twiddling its thumbs and then say *"Hey I've tried to find this control, but it ain't here, so I'm off to the pub! Cheers."* I hear you saying *"But we specified the base url at the start. Shouldn't the test restart from that?"* - but let's take a second to think this through. What we specified is the **base** url. When we're logged into the Facebook landing page, the base url has not changed...there's just more parameters, etc. tacked on to the end of it.    

<img src="/docs/assets/images/remember.png" alt="Remember" width="50"/>

**REMEMBER:** If you have had to log in to perform any of the actions in your test, ensure that you log out **before** you complete your test. In that way you leave the system in a state where your tests can be repeated.

If you look at the IDE, all the commands that were successfully executed will be coloured in green. The log tab at the bottom of teh IDE will display any errors that were encountered during the execution of the test script. If the test completed all the commands successfully it wil indicate that the test was successful by displaying a success message in the log.

### Step 3 - Lets save this...test

Once you have verified that the test script has executed successfully, you can save it. Click the **Save** button in the top right hand corner of the IDE.  

<img src="/docs/assets/images/ide-demo-step-7.png" alt="Step 7" width="700"/>

Once clicked, the Windows **Save** dialog will be displayed, where you can choose the location to ave your files. The file will (should - ref. the <a href="#pitfall-1">Pitfall</a> above) be saved with a ".side" extension. You can then select the file when performing future Regression tests, etc.

## A sneak peek at Selenium Commands

<img src="/docs/assets/images/selenium-commands.jpg" alt="Selenium Commands" width="400"/>


The Selenium IDE has a whole host of commands. However, we are not going into a detailed examination of them now (this article is long enough already!). Selenium commands can be broadly classified into three categories, viz. **Actions**, **Accessors** and **Assertions**.

1. **Actions** - These are commands that interact directly with the web application itself.
  1. clickAndWait()
  2. typeAndWait()
2. **Accessors** - These are commands that enable the user to store values to user defined variables.
  1. storeTitle()
3. **Assertions** - These are commands that verify the current (actual) state of teh web application with an expected state.
  1. **Assert** - this command ensures that the execution of the test will be ended in the case of a failure.
  2. **Verify** - this command ensures that the execution of the test will continue even if a verification fails. 
  3. **WaitFor** - this command waits for a specific condition to be true, before continuing the execution of teh next step.

There are many more commands and features that can be found in the Selenium IDE, but those will be saved for another article. At this point you know enough to create basic tests which you can use to quickly prototype the Selenium WebDriver tests that you will be coding.

## But why are we coding tests if we can just record them?

The Selenium IDE has some significant drawbacks when compared to tests written in Selenium WebDriver. Some of them include:
- no support for data-driven testing
- unable to perform database testing
- unable to provide any reporting after test execution
- 
and the one that I found the most frustrating

- learning the advanced features (variables, flow control, test reuse, etc.) of the IDE took far more time than achieving the same functionality by coding tests for Selenium WebDriver 

## So what now?

The next part delves into Selenium WebDriver. This is where (in my opinion) things get a lot more fun (and complicated)...

---

[^1]: :microphone: <a href="https://www.youtube.com/watch?v=TLGWQfK-6DY" target="_blank">A little bit of Run-DMC</a>
