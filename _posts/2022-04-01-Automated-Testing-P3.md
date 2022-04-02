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

**PITFALL** Like I said before, Selenium is not without its flaws. Sometimes when you save your test, it does two things:
- it saves it with an unintuitive name e.g. **0e0c5abd-2c69-4155-8477-f912f0c82892**. *WTF?*
- it sometimes saves the file without an extension i.e. there is no ".side" on the end - just **0e0c5abd-2c69-4155-8477-f912f0c82892**

<img src="/docs/assets/images/remember.png" alt="Remember" width="50"/>

**REMEMBER** Once you save a recording as a script, check the name of the file in File Explorer. If it has a wierd name like **0e0c5abd-2c69-4155-8477-f912f0c82892**, give it a useful name like **open_google_homepage** and if it **is** missing an extension, add the ".side" on the end - like so: **open_google_homepage.side**. This way when you browse for the test script later on, the Selenium IDE will pick it up. *Hurray!*

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

**DEFINITION** *Um...what does **Assert** mean?* By definition, **Assert** is *"an expression, which encapsulates some testable logic specified about a target under test"*, which is a fancy way of saying ***check that some condition (that we want to check) is true***!

**Onward brave coders...!**

### Step 1 - Recording

1. Launch Chrome and open te Selenium IDE plugin (by clicking the icon in the toolbar)
2. Select **Record a test in a new project**. Provide a name for your test, and click **OK**.

<img src="/docs/assets/images/ide-demo-step-1.png" alt="Step 1" width="400"/> 

3. Next, enter the url (in the BASE URL input box) for the Facebook landing page. This url acts as the starting point for all subsequent navigation/actions in the test being recorded. Click the **START RECORDING** button. The IDE starts the recording by navigating to the web page.

<img src="/docs/assets/images/ide-demo-step-2.png" alt="Step 2" width="400"/>

4. Once the website opens, type in the fake UserID & Password into the relevant fields and click the **Log In** button.



