# CONTENT OF AN API DOCUMENTATION SUITE

## 1 Introduction

### 1.1 Chapter Overview

An API-based product or service needs different kinds of documentation. We can classify the information users need to be successful into typical document types. Although that information can be packaged and divided up in various ways, some document types are absolutely essential to enable usage, and others are highly recommended to increase the probability of success.

### 1.2 Learning Objectives

By the end of this chapter, you should be able to:
* Understand what constitutes adequate documentation for effective API usage.
* Discuss what types of documents are essential to user success.
* Consider what set of documents you need to capture interest and bring users up to speed quickly.

## 2 Essential API Documentation

### 2.1 Industry Standard Document Types

Coming up with a single recommendation for an ideal API documentation suite is complicated because the specific situation varies for different kinds of products and software technologies. There is, however, an industry-standard set of common or expected deliverables, where each one addresses a different set of user needs and assumptions about the reader. The reader experience for each type of document differs, because each one addresses a particular type of information for a particular audience and stage of development.

Some types of documents are absolutely essential to make an API-based product usable at all. The specific names of the documents don't matter so much, but users must be able to find:
* A detailed element reference;
* A high-level technical overview;
* Instructions for installation or access;
* Requirements for authorization and authentication;
* A “Hello World” or "Getting Started" example.

Additional documentation (within the same documents or in separate documents) must provide context for the technical detail - the "why" and "when" in addition to the "what".

What type of information goes where in the documentation suite should reflect who the intended audience is, and how you expect them to use the document.

### 2.2 Required Document Types

To make an API-based product usable at all, it is absolutely essential to provide a technical overview of the API, a detailed element reference, instructions for installation or access, authorization requirements, and a “Hello World” or "Getting Started" example.

#### API reference manual

The most critical API documentation suite component is a complete, accurate, and accessible API reference.

The primary task of an API reference is to provide the precise syntax of the language and to explain the intended use of each element, with just enough conceptual context for readers to understand the basic usage, and to clarify the relationships between the elements of the language and among functional areas or subsystems.

The language details don't exist in a vacuum. To use an API, a programmer needs to gain access to it and understand the environment in which it is used. Semantic information in the reference provides context for the specific syntax information. This applies to both the API as a whole, and to each element.
* An API reference should provide an overview of what the API does and is used for overall, as well as introductory descriptions that describe what each major element does and is used for.
* An API reference should include code examples in the form of snippets that illustrate the correct usage of particular elements and special parameter values.
* An API reference is not the place for tutorials, extended examples, or in-depth conceptual discussions. These things are important, and should be provided somewhere in the product documentation - just not in the API reference. If conceptual and usage doc is available, the reference should contain links or pointers into it.

#### Technical overview

The technical overview explains what the technology is, what it does, who should use it, what differentiates it, and most importantly, the unique benefits it can deliver. People will only pay attention to your technology if they can see compelling benefits.

A good technical overview can provide a high-level description of how the underlying system works, how the software compares to alternatives, and why the unique benefits of this technology make it superior.

A technical overview, whether it is a standalone piece or an introduction to an API reference, should answer these questions:
* What does the product or service do?
    - Placement within the domain
    - Expected background of typical users
* How does the API fit in?
    - Placement within the product
    - Placement within workflows
* What can you do with the API?
    - Main features
    - Typical use cases

#### Installation or access guide

While most API provider teams know that they need a reference, this next deliverable is often overlooked. The installation guide tells a new API user how to set up their development workstation with the necessary software environment. Setup details can include how and where to get credentials for the VPN, access to wiki pages and bug tracking systems, GitHub repos, Slack channels, and information about other key developer tools.

This guide should include everything needed for setup and configuration, things that you think are obvious, but often are a complete mystery to newcomers. You might even have different versions of this, one for internal developers, one for external developers, one for partners, and so on.

#### "Getting Started"/"Hello World"

This deliverable can jumpstart the real work. The getting started guide provides an introduction to using the API with some simple practical examples. The getting started section is often overlooked in an API documentation suite.

A getting-started guide usually includes a “Hello World” recipe (more information about recipes will follow shortly). If you aren’t familiar with “Hello World”, it’s the shortest functional program that you can write using an API. The program is a complete coding example that a developer can compile, execute, run, and see simple results. Originally, these programs ran just enough code to produce the message “Hello World” on a screen or printer.

### 2.3 Strongly Recommended Document Types

Although the previous document types are essential to ensure that developers can use your API, there are some additional documents that greatly enhance your product's chances of adoption and successful usage.

#### Glossary of terms

You should have a glossary that will help ensure the consistent use of terminology. This deliverable should be at least internal, but we strongly recommend that you make it available to your readers.

#### Usage recommendations and example code

These include recipes and cookbooks with solutions for common use cases. They should be copy/paste ready, well-commented, and provide instructions for how to modify.

#### Conceptual and procedural documents

These documents are critical if your software technology is complex and has a broad set of potential applications. They enable developers to achieve true mastery of the API by providing another level of information. In a design guide, you can teach API users about the elegant features of the API design and how to apply that elegance in the context of software development. These documents can also identify, explain, and justify recommendations for best practices.
* Usage guides (Programmers Guide, Design Guide, Developers Guide) explain important concepts and advise on recommended usage.
* Tutorials help users learn the product and implement common use cases.

#### Release notes

Provide essential support information. For an initial release, the release notes should include a list of features, overview of documentation, known problems, and how to get support. For following releases, release notes should include new features, changes, deprecations, deprecation policy, and upgrade/migration instructions

#### Migration/Integration guides

Not every API needs a Migration or Integration guide, but if your API integrates with other systems, this document can be essential for success. Don’t assume that your user will be able to figure it out on their own. Even if it is easy to do, create the short guide that saves them the time it will take to determine that it is easy.