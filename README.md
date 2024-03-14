# Cypress
✨Cypress Automation Tests in JS✨

ONLY FOR MY PRIVATE PURPOSES<br>
USING OPEN/FREE MATERIALS <br><br>
- I used this page: [Testing site](https://parabank.parasoft.com/parabank)
- Official documentation: [Cypress documentation](https://docs.cypress.io/guides/overview/why-cypress) 
<br><br>

# SETUP
1. Install  Node.js (not installed if Node not recognized)
2. CMD run as admin/console > npm install cypress / npm install (downloads libraries, cypress and browsers)
3. npx cypress open - Interfejs Test Runner / npx cypress run - background, cli (run from Cy folder)
4. npm run {} - to run applications on dev server, settings on package.json/scripts

More details: [cypress-course-overview-end-to-end-testing-with-cypress](https://egghead.io/lessons/cypress-course-overview-end-to-end-testing-with-cypress)

<br>
Sets: VSC, Git Bash
<br><br><br>

>For Gitlab (to log into remote servers) generate ssh key:  <br>
>ssh-keygen -t rsa -b 4096 -C "twoj_email@domena.com" >enter <br><br>

_Elements: <br>_
```html
tag - "a"
identificator - ("#")  
class - (".")  
attribute - ('[name=""]') 
<button type="submit"> - ('button[type="submit"]') 
checkbox: ('input[type="checkbox"].checkbox').click();  
class="label" for="test" - 'label[for="test"]'  
```
it.only - execute specified it<br>
it.skip - skip the test<br>
<br><br>
<dl><dt> 
Google reCAPTCHA v3:  <br>
</dt></dl>  

- Create an HTML file:  Create an HTML file to hold the reCAPTCHA code. Create a plain text file and renamin the extension to .html.  <br>
- Add the reCAPTCHA code: Inside the HTML file, add the reCAPTCHA v3 code snippet:  <br>  
```
<div class="g-recaptcha" data-sitekey="YOUR_SITE_KEY"></div>
```
  Replace YOUR_SITE_KEY with the actual Site Key you obtained from Google reCAPTCHA.
- Save the HTML file: Save the file containing the reCAPTCHA code. <br>
- Run Cypress tests: Now run Cypress tests that interact with this HTML file. Cypress will interact with your HTML file containing the reCAPTCHA, allowing you to test interactions with reCAPTCHA v3. <br>

Note: You can add reCAPTCHA v3 to your website and test it using Cypress, no need to directly add the reCAPTCHA v3 code to Cypress test files.

<dl><dt> 
Tree:  <br>
</dt></dl> 

- e2e: sample tests from cypress
- fixtures: 1 file 'example.json' (for *.json files: used attributes, urls)
- integration: e.g. \api-tests, *.js Test files: body/status/header response, console errors, resolution checking, requestBody/requestParams, expected Data
- cypress.config.js:
```
module.exports = {
  e2e: {
    baseUrl: 'https://{}.com/'
    specPattern: [
      'cypress/integration/api-tests/*.spec.{js,jsx,ts,tsx}',
      'cypress/integration/api-tests/*.cy.{js,jsx,ts,tsx}',
    ],
    setupNodeEvents(on, config) {
      // implement node event listeners here      
    }
  }
}
```
- package.json:
```
{
    "scripts": {
        "sample": "cypress open"
  }
}
```
(```npm sample``` should run the test if not: 1. ```npm install``` - checks if everything is installed 2.```npm install -g cypress``` - cy framework installed globally)

<br><br>
- To get expected result on console: <br>
inspect>console>choose test 
<br><br>
- To get headers ('Content-type': 'application/json; charset=UTF-8'): <br>
network>fetch/XHR>name>Headers>Response headers>Content-type (or sourcepage> ALL)

