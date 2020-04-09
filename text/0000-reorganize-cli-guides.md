- Start Date: (fill me in with today's date, YYYY-MM-DD)
- Relevant Team(s): (fill this in with the [team(s)](README.md#relevant-teams) to which this RFC applies)
- RFC PR: (after opening the RFC PR, update this with a link to it and update the file name)
- Tracking: (leave this empty)

# CLI Guides Reorganization

## Summary

The current Ember CLI Guides are broken into 3 sections, Basic Use, Advanced Use, and Writing Addons. The issue is that there is no infrastructure to allow nesting categories in the guidemaker. Because of this, we cannot create subcategories within these 3 large categories. Therefore we will keep Basic Use items on top, and Advanced Use items in the middle, but remove those categories and break each into several subcategories. Basic Usage will be split into CLI Commands and Usage. Advanced Usage will be split into Project Layout, Build Pipeline, Maintenance, Configuration, and Troubleshooting.

## Motivation

When new authors are looking to add items into the guides, it is not clear where to put content. The current infrastructure, guidemaker, doesn't allow nesting of categories. Therefore, all of CLI commands cannot be easily broken into subpages under a category of CLI commands because it could no longer be under Basic Use. Authors want to allow content to be grouped by category and for categories to be able to grow in the future. CLI Commands for example, are most often the first things beginners need to learn, so they should remain first in order above other basic content.

Most of the content in the guides fall under Advanced Use. Advanced users do not know which page to look for their information. Very often what they are looking for does not fit in the short list of pages. Those pages are too long and cannot be easily digested. Also, a lot of advanced content is missing, and advanced users currently feel they need to skim all the pages to determine this.

## Table of Contents

### Intro
  - Ember CLI
### CLI Commands
  - /index (links to full API docs and references `--help`)
  - new
  - addon
  - install
  - serve
  - build
  - generate
  - test
### Usage
  - Folder Layout
  - Using Addons
  - Asset compilation
  - Stylesheet compilation
  - Dependencies
### Project Layout
  - Classic
  - Pods
  - Template Colocation
### Build Pipeline
  - Builds & Rebuilds
  - Addons (for merging behavior)
  - Plugins (Broccoli intro)
  - Looking Forward (Ember Auto Import & Embroider)
### Maintenance
  - Updating
  - Testing
  - Deploying
### Writing Addons
  - Structure
  - Tutorial (Writing your first addon)
  - Dependencies
  - Blueprints
  - In-Repo Addons
  - Documenting
  - Deprecating Addon Features
### Configuration
  - .ember-cli file
  - ember-cli-build.js
  - ember-cli-update.json
  - package.json
### Troubleshooting
  - Windows
  - Vagrant
  - Debugging
  - Performance

## Versioning

> Redirects

## Drawbacks

> It is no longer clear what we consider Basic and Advanced.

## Alternatives

> Build infrastructure that allows for the nesting of categories.

## Unresolved questions

> Do this in a branch until complete or land pages as we go
