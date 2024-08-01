# SUPPORTING THE DOCUMENTATION EFFORT

## 1 Introduction

### 1.1 Chapter Overview

The effectiveness of documentation is measured by the success of users. To achieve quality documentation, your software development process must incorporate planning and preparing for the documentation effort, as well as allowing for adequate technical and editorial review to ensure the quality of the content.

### 1.2 Learning Objectives

By the end of this chapter, you should be able to:
* Identify the essential attributes that define quality software documentation.
* Understand the stages and processes for creating quality software documentation for an open source product or service.
* Understand how your software development process can support the documentation effort.
* Identify areas of consideration for evaluating the quality of your documentation.

## 2 Best Practices for Producing Quality Software Documentation

API developers and writers are lucky to be able to use the experience gained over the last 30-40 years on how to create effective documentation for programmers. There is a lot of knowledge available about what does and does not work. Although there isn’t any book published with this title, there is a set of best practices that have been developed over the years. Those best practices are associated with knowing how to:
* Collect information from non-human sources
* Effectively interview API developers to collect information efficiently
* Develop an architecture or design for the document suite
* Use tools to enhance productivity
* Create maintainable documents
* Create high-quality content

Developing deep technical writing skills enhances the quality of the documentation and speeds up the development process. If you want to understand these skills better, we suggest that you take the follow-on course, Creating [Effective Documentation for Programmers (LFC112)](https://training.linuxfoundation.org/training/open-source-technical-documentation-essentials-lfc111/?_gl=1*1r0fycm*_gcl_au*MTIzMTEzODg0NC4xNzIyNTE0Njc5*_ga*MTI1ODkwNjU2MS4xNzIyNTE0Njc5*_ga_EMX7DDZMX4*MTcyMjUxNDY3OC4xLjEuMTcyMjUxODUxMi4xMi4wLjA.*_ga_VWZ4V8CGRF*MTcyMjUxNDY3OC4xLjEuMTcyMjUxODUxMi4wLjAuMA..).

## 3 Steps to Ensure High Quality Documentation

### 3.1 Supporting the Documentation Effort

The following supporting tasks and activities (before, during, and after the actual writing phase) go a long way toward ensuring documentation that actively contributes to user success.

#### Define a user layer to ensure complete coverage

To determine whether your documentation covers all of the information users need, you must define a user layer. This is the set of features and clearly identified public API elements that are available to users, which you are prepared to support across versions. Good API documentation covers all parts of the user layer completely. There cannot be any question about the syntax or usage of an API element.

Internal utilities and implementations should not be documented publicly. You can update and improve the internal code without a lot of extra support costs, as long as it doesn't change the documented user layer. For open source projects, however, this kind of internal information is available to contributors, so it's a good idea to provide specific warnings about ways in which changes can affect the user layer.

#### Review and test to ensure accurate content

Technical errors in the documentation undermine a reader's confidence in your product and in themselves, and make it much less likely that they will adopt and use your API successfully.

To ensure that content is correct, you must make sure that every piece of public documentation is carefully reviewed and that all examples are fully tested. Of course the API experts are responsible for making sure that the technical details are correct, but it is also important to ensure that the information can be understood and used correctly by non-experts who can model potential users. You can use your own QA and support engineers, beta testers, or partners.

#### Maintain a glossary of terms to ensure adequate description

For someone to learn your system, you must ensure that the specific technical details are supported by high-level description that places those details in context. When you tell people how to use an element, you must also tell them why and when to use it.

To make sure that descriptions are correct and unambiguous, you must first make sure that terms are clearly and explicitly defined, then use those terms consistently. The language you use should be consistent, clear, concise, and direct.

#### Follow a style guide to ensure discoverability

If a user can't find what they need in the documentation, it might as well not be there. To make the information available, you must make sure that it is presented using a consistent style or template, so readers can immediately tell what they are looking at and whether they are in the right place. Your documents must include indexes, tables of contents, and cross-references that help the reader get to the right place from wherever they happen to land.

### 3.2 Documentation as a Contribution Area

An open source project, like any other software product or tool, needs to encourage adoption and attract new users. For the product to succeed as open source, however, it also needs to attract, encourage, and support an active contributor community.

The documentation effort itself offers potential contributors an entry point. Contributing to the documentation helps developers gain a deeper understanding of the design and architecture, and an appreciation of how the product can and should be used.

Supporting documentation contribution is part of preparing for and supporting the documentation effort in general. To solicit documentation contributions, you need to:
* Create a documentation label or tag for doc issues.
* Identify and prioritize your project's specific documentation needs.
* Provide policies and support services for documentation contributors.
* Identify subject-matter experts who can answer questions from writers and review documentation proposals in different areas.

## 4 Evaluating the State of Your Documentation

### 4.1 Quick Evaluation Checklist

Quality documentation is defined by how effective it is in making users successful. The content of documentation must meet certain basic requirements for it to be effective:
* Complete coverage
* All user-level elements and features included.
* Accurate content
* All details are correct.
* Adequate description
* Details are unambiguous and placed in context.
* Discoverability
* Readers can find the information they need.

When a professional technical writer checks the quality of existing documentation to see how it can be improved, they look for the following essential characteristics:
* A clearly-defined user layer (public API elements).
* Complete coverage and accurate syntax details of all public elements and features.
* Useful semantic description of every element and feature.
* Introductory description at every level that places information in the appropriate context.
* Consistent use of terminology, conforming to an explicit glossary.
* Consistent presentation and use of language.
* Navigational aids that keep readers oriented and make it easy for users to find the information they need when they need it.
* Clear indications of intended audience, prerequisites, and assumptions.

### 4.2 CNCF Documentation Evaluation Criteria

The [Cloud Native Computing Foundation (CNCF)](https://www.cncf.io/?_gl=1*dzz4h7*_gcl_au*MTIzMTEzODg0NC4xNzIyNTE0Njc5*_ga*MTI1ODkwNjU2MS4xNzIyNTE0Njc5*_ga_VWZ4V8CGRF*MTcyMjUxNDY3OC4xLjEuMTcyMjUxOTAyOC4wLjAuMA..) has established comprehensive guidelines and standards for how much and what kind of documentation is needed for a fully-realized cloud-native open source product. If you are a maintainer for a CNCF project, you can submit your documentation to CNCF for evaluation by technical writing professionals and get suggestions and recommendations for improvement or further development.

Even before you start writing your documentation, it can help to understand the evaluation guidelines and [criteria](https://github.com/cncf/techdocs/blob/main/assessments/criteria.md) that affect the writing process.

#### Information architecture structure

Is there a technical overview? Do the navigation options support the user? Is there a learning path for new users? Are different types of users identified and supported? Is the domain context clear? Is there any task-based content, such as tutorials or recipes? Is conceptual content covered?

#### Documentation creation process

Is there a style guide and does the documentation adhere to it? Is it clear that there are page templates/designs and does the documentation adhere to them? Is there a well-defined review and approval process? Is there a documentation development plan?

#### Maintainability of the documents

Is there versioning? Is there appropriate internationalization and localization? Is there a documentation maintenance plan? Does their documentation support policies and procedures?

#### Contributor support

Are there code contribution policies? Do you have documentation contribution policies? Are there clearly defined issue/PR triage procedures?