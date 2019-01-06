# Aronfield QA Testing Guide

This document will lay out an overview for the process, procedure and tools used to do a full Quality Aassurance test on a client site.


### Validation/Content Testing
* Make sure all CSS is contained in the style.css file in the theme folder. Custom CSS should not be added through the Wordpress customizer or built in theme settings.
* Click through every link on the site and verify they are NOT broken and lead to the desired page.
* Verify all links are relative (//page) and not (http://devsite.com/page). This includes images.
* Verify no dead or empty pages with no content
* Check for spelling mistakes or innacurate or out of date information.

### Accessability Testing
* Verify color choices have enough contract with page elements to accomodate color blind users.
* Make sure all images/links have alt/title tags with a summary of the image/link
* Use http://wave.webaim.org and correct any Errors, and bring Warnings to attention of Project Manager.

### Input Testing
* Go through every form field and verify any required or optional fields behave as required.
* Verify fields that are restricted (eg numbers only) only allow numbers and not alpha characters or punctuation
* Verify any date fields are correctly recieving input, and correcting or rejecting malformed dates.
* Verify text area inputs preserve new line spacing when submitted.

### Browser Testing
* Identify the major page layouts on a site. (eg a site with 30 pages, might have only 3 layouts that need to be tested. Ask developer)
* Use BrowserStack (http://browserstack.com) to load/click through the website, the layouts, and contact forms.
* Use the following browsers/devices for testing:
  * Mac OS Safari
  * Mac OS Firefox
  * Mac OS Chrome
  * Windows Chrome
  * Windows Firefox
  * iOS iPhone X
  * iOS iPhone 8
  * iOS iPhone 7
  * iOS iPhone 6
  * iOS iPhone 5S
  * iOS iPad 6th
  * iOS iPad Air 4
  * iOS iPad Mini 4
  * Android Galaxy S9
  * Android Galaxy S6
  * Android Pixel 3 XL
  * Android Pixel 2
  * Android G5
  * Android Moto G 2nd Gen
* Make a note of any issues that you find, and mark them in the pulse comments along with the device/page/element for the develope to reproduce


### Performance Testing
* Establish a baseline test using http://webpagetest.org (use default settings). Copy down the Performance Results in the QA pulse comments as the starting data.
* Run an initial test through Google Page Speed Insights - https://developers.google.com/speed/pagespeed/insights/. Place any low score results in the pulse.
* Verify SSL present by running a test through SSL Labs - https://www.ssllabs.com/ssltest/. Post results of the test (Grade) in the pulse. If there are issues, take a screenshot and post that in the pulse and alert a developer.

### QA Process
* Create individual pulses with the issues grouped by testing category here. (eg, all content/validation issues go in one validation pulse, all performance issues go in a performance pulse)
* If issues are outstanding, make a PM aware of them, you may be asked to assign them to a developer.
* When the developer resolves the issues, go back through the entire QA test, as new issues could have arisen.
* If no issues exist, the QA pulse can be marked completed.
