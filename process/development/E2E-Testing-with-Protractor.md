# E2E Testing with Protractor

## tl;dr:

```
cd src/web
npm start &
npm run e2e
```

## Documentation

Our project is configured to use the test framework [Mocha](https://mochajs.org/#getting-started). The examples on the [protractor website](https://www.protractortest.org/) use Jasmine instead (which as far as used in the tutorial works the same way).

[Protractor](https://www.protractortest.org/#/tutorial) is the system used for E2E testing through a browser.

If anyone already knows about WebDriverJS the [comparison page](https://www.protractortest.org/#/webdriver-vs-protractor) might be interesting.

[Chai](https://www.chaijs.com/api/bdd/) is used to express assertions. We have Chai plugins set up for [tests on strings](https://www.chaijs.com/plugins/chai-string/) and for [using promises](https://www.chaijs.com/plugins/chai-as-promised/).


## Overview

### Structure
Usually a call to `describe()` contains the subject and forms a sentence together with text of contained calls to `it()` (see [mocha documentation](https://mochajs.org/) for details):

```
describe("hello world example", () => {
    it("prints hello world", async () => {
        // ...
    });
});
```

### Locators
[Locators](https://www.protractortest.org/#/locators) are used to select DOM elements.

```
by.model("somename");
by.binding("somebinding");
by.id("someid");
// ...
```

### Actions
[Elements](https://www.protractortest.org/#/locators#actions) are necessary to carry out actions on DOM elements. When calling `element()` nothing is done yet other than the construction of an ElementFinder object. Only when an action is carried out, the browser will be contacted:

```
const elem = element(locator);
elem.click();
elem.sendKeys("input text");
// ...
```

### Assertions
Emplying a BDD testing style, `chai.expect()` is called on something that is being tested. Using that, a chain of [other methods](https://www.chaijs.com/api/bdd/) is called to form an assertion in somewhat natural language:

```
const expect = chai.expect;
expect(1).to.equal(1);
expect([0, 1]).to.not.include(2);
// ...
```


## Tips

### Limit tests to run while working on the implementation
For development it can be nice to only run the tests of one `describe()`. For that [`describe.only()`](https://mochajs.org/#exclusive-tests) can be used in place of if.

When there are several troublesome tests in one call to `describe()` using  [`it.skip()`](https://mochajs.org/#inclusive-tests) in place of `it()` can be useful. When protractor is run, it is displayed as "pending".

### Use page objects
[Page objects](https://www.protractortest.org/#/page-objects) encapsulate elements of interest on a tested page.  [Here](https://github.com/angular/protractor/blob/5.4.1/exampleTypescript/angularPage.ts) is a basic example. Unlike most examples on the web ours don't have a method `get()` since so far our tests all get the root page and navigate from there (necessary where login is required).

### Use `before()` for setup
Setup usually starts by calling `await browser.get("/")`, followed by logging in and navigating to the tested page (using the page objects in `src/web/src/test/javascript/e2e/page-objects`. It is also possible to directly get the page (when no login is required).

### Never have anything use manual bootstrapping
When using automatic bootstrapping (so far we do) protractor has means to tell when the test can be run, i.e. `browser.get()` does work. Otherwise, `browser.driver.get()` needs to be used instead, which can cause all kinds of trouble.


## Troubleshooting

### Equality checks don't work as expected

Maybe it's the wrong one. The naming of some methods is weird:

```
expect(1).to.eql(1);        // recursively compare properties,
                            // only equal if a === b for all primitive a, b
expect(1).to.deep.equal(1); // same as above
expect(1).to.equal(1);      // strictly equal (===), without recursion
expect(1).to.eq(1);         // same as above (but undocumented)
```

### Runs are too slow
Calls to `describe()` or `it()` can be replaced by `describe.only()` and `ìt.only()` to limit the number of tests that are run ([doc](https://mochajs.org/#exclusive-tests)).


### I need to debug a test
The chrome inspector ca be used ([details](https://www.protractortest.org/#/debugging):

1. Add the keyword "debugger" in the questionable test case
2. Call `node --inspect-brk node_modules/protractor/bin/protractor src/test/javascript/protractor.conf.js` in src/web
3. Open "chrome://inspect/#devices" in Chromium/Chrome
4. Click "inspect"


### Command not found
If globally installed `protractor` and `webdriver-manager` commands cannot be found, that is probably because the npm directory  is not on the PATH.
