# LoginAutomation

Test cases
The demo page — practicetestautomation

Some of the possible test cases are outlined in the demo page itself:

Positive LogIn test

Open page
Type username student into Username field
Type password Password123 into Password field
Click Submit button
Verify new page URL contains practicetestautomation.com/logged-in-successfully/
Verify button Log out is displayed on the new page
— — — — — — —

Negative username test

Open page
Type username incorrectUser into Username field
Type password Password123 into Password field
Click Submit button
Verify error message is displayed
Verify error message text is Your username is invalid!
— — — — — — —

Negative password test

Open page
Type username student into Username field
Type password incorrectPassword into Password field
Click Submit button
Verify error message is displayed
Verify error message text is Your password is invalid!
— — — — — — —

However, there are more test cases that could be executed:

Negative empty log in form test

Open page
Click Submit button
Verify error message is displayed
Verify error message text is Your username is invalid!
— — — — — — —

And some simple element visibility checks:

Username input field is visible

Open page
Verify Username input field is visible
— — — — — — —

Password input field is visible

Open page
Verify Password input field is visible
— — — — — — —

Submit button is visible

Open page
Verify Submit button is visible
Set up
Installations

I will be writing code in JavaScript, which does not need any additional installations.

Node.js is necessary for downloading Playwright. You can find the documentation for downloading Node.js right here —
download Node.js.

Playwright — you can find the documentation for installing Playwright right here — Playwright installation
documentation.

I will use Visual Studio code as my code editor, you can find the documentation for downloading it here — download VS
code.

_________________________________________________________________

