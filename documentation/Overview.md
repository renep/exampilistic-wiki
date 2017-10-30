# Exampilistic

With exampilistic, testers, developers and business people can collaborate on specifications for software by creating concrete examples. Exampilistic manages these examples in a Wiki-structure and allows you to create automated tests based on the examples.

You can refer to the same example from different documents (feature, user stories) and different documents can also refer to different versions of the example. This allows you to evolve you examples, and also to have your old user stories still link to the version of the example that was recent when the user story was finished.

## Design Goals

* "A better FitNesse"
* Versioned examples and test results
* Editors that help users to write examples (Live-Preview or even WYSIWIG)
* Different formats for writing examples (Tables, cucumber-style, ...)
* Separation of wiki, test case generator and test runner

## Example Workflow: New Feature

* Tester and PO write a new user story, with a completely new examples in tabular form. The examples are automatically marked as "upcoming"
* Developers pull all test data from the exampilistic server and run all tests. The new examples will be ignored, since it is "upcoming".
* Team pulls the story into the sprint, they refined the examples together. They mark the examples as "in development".
* Developers pull all test data from the server and run all tests. The examples will run, since they are "in development", but when they fail, they will be marked as "yellow" (ignored / skipped).
* Developers implement the feature. Tests are green.
* Team / PO marks the examples as "implemented". From now on, when the test fails, it will be marked as red.
* Developers upload the test results to the server, where they will be stored with the current version. They link the test results in the user story, where the test is shown as "green".
* PO / Team add a new page to the wiki, documenting the current feature. They link the examples in their "latest stable" version.

## Example Workflow: Update Existing Feature

* Tester and PO write a new user story, and they add existing examples in tabular form. They edit the example, the new version is automatically marked as "upcoming".
* Developers pull all test data from the exampilistic server and run all tests. The updated examples will be ignored, since it is "upcoming", automated tests still run the old version.
* Team pulls the story into the sprint, they refined the examples together. They mark the examples as "in development".
* Developers pull all test data from the server and run all tests. The examples will run (new version), since they are "in development", but when they fail, they will be marked as "yellow" (ignored / skipped). The current stable version of the examples will **also** run!
* Developers implement the feature. Tests are green.
* Team / PO marks the examples as "implemented". From now on, when the test fails, it will be marked as red.
* Developers upload the test results to the server, where they will be stored with the current version. They link the test results in the user story, where the test is shown as "green".
* PO / Team review the documentation of all changed features. They do not have to edit any examples, because they already show the "latest-stable" version.
