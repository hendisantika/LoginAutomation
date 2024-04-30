# LoginAutomation

### Things todo list:

1. Clone this repository: `git clone https://github.com/hendisantika/LoginAutomation.git`
2. Navigate to the folder: `cd LoginAutomation`
3. Run the test: `npx playwright test`

### Test cases

The demo page — [practicetestautomation](https://practicetestautomation.com/practice-test-login/)

Some of the possible test cases are outlined in the demo page itself:

### Positive LogIn test

1. Open page
2. Type username student into Username field
3. Type password Password123 into Password field
4. Click Submit button
5. Verify new page URL contains practicetestautomation.com/logged-in-successfully/
6. Verify button Log out is displayed on the new page
— — — — — — —

### Negative username test

1. Open page
2. Type username incorrectUser into Username field
3. Type password Password123 into Password field
4. Click Submit button
5. Verify error message is displayed
6. Verify error message text is Your username is invalid!
— — — — — — —

### Negative password test

1. Open page
2. Type username student into Username field
3. Type password incorrectPassword into Password field
4. Click Submit button
5. Verify error message is displayed
6. Verify error message text is Your password is invalid!
— — — — — — —

However, there are more test cases that could be executed:

### Negative empty log in form test

1. Open page
2. Click Submit button
3. Verify error message is displayed
4. Verify error message text is Your username is invalid!
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

### Set up
Installations

I will be writing code in JavaScript, which does not need any additional installations.

Node.js is necessary for downloading Playwright. You can find the documentation for downloading Node.js right here —
download Node.js.

Playwright — you can find the documentation for installing Playwright right here — [Playwright installation
documentation.](https://playwright.dev/docs/intro#:~:text=Installing%20Playwright%E2%80%8B&text=Run%20the%20install%20command%20and,easily%20run%20tests%20on%20CI)

I will use Visual Studio code as my code editor, you can find the documentation for downloading it here — download VS
code.

_________________________________________________________________

File structure

LoginAutomation — this is the main folder. It will contain all the project related files.

Pages — this folder will contain files related to web pages.

login-page.js — this file will contain methods for the login page.

Tests — this folder contains test files.

test.spec.js — this file will contain our test cases and assertions.

LoginAutomation
|_Pages
| |_login-page.js
|_Tests
| |_test.spec.js
_________________________________________________________________

### Let’s automate the test cases

Visibility tests

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
— — — — — — —
_________________________________________________________________

### Negative Log in test cases:

Negative username test

1. Open page
2. Type username incorrectUser into Username field
3. Type password Password123 into Password field
4. Click Submit button
5. Verify error message is displayed
6. Verify error message text is Your username is invalid!
   — — — — — — —

Negative password test

1. Open page
2. Type username student into Username field
3. Type password incorrectPassword into Password field
4. Click Submit button
5. Verify error message is displayed
6. Verify error message text is Your password is invalid!
   — — — — — — —

Negative empty log in form test

1. Open page
2. Click Submit button
3. Verify error message is displayed
4. Verify error message text is Your username is invalid!
   — — — — — — —

All of our negative test cases require verification of the error message visibility and text. We’ll need a locator to
perform these actions. Let’s define this locator in the constructor of the LoginPage class: