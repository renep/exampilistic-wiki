# Backlog

## Non-Goals

The open source version of exampilistic will be really simple - comparable to FitNesse. We will leave the complicated stuff for a "professional version", should we ever implement it.

* Authentication / Authorization
* Different storage backends (Database, ...)
* Multi-Tenant application
* Multi-Project setups

## Goal: Dogfooding

Exampilistic can be used to test itself. For now, it can only display the files that are stored on disk. We will have to write those MD files (Pages, User Stories) and JSON files (tests) by hand for now.

* Test runner can run tests marked as "implemented" from the local cache (Red / Green)
* Test runner can run tests marked as "in development" from the local cache (Yellow / Green)
* Wiki server shows main MD files saved on disk
* Wiki server renders cucumber-style test included in a MD file
* Wiki server serves all tests ("implemented" and "in development") as a machine-readable API
* Command line tool can fetch all tests from server and save them to local cache

## Goal: Editing

Exampilistic can be used to edit the markdown files and the simple cucumber-style tests.

## Goal: Better Editors

The editors for markdown files and tests now have live preview and better tools to support writing tests.

## Goal: More Test Types

The user can define tests in different tabular styles.

## Goal: Workflow for User Stories

User stories are not simple MD files anymore, they now have a workflow (planned / in development / implemented). The examples / tests of a user story are automatically tagged based on this workflow.

## Goal: Workflow for Impact Mapping

## Goal: Guide the User when Writing Tests

## Goal: Code Generator for Tests
