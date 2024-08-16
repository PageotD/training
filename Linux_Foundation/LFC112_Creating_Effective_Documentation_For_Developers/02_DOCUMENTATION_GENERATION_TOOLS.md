# DOCUMENTATION GENERATION TOOLS

## 1 Introduction

### 1.1 Chapter Overview

Tools are available that translate the API definition and specially formatted comments in source code into documentation for an API. The quality of such generated documentation depends on how you configure the tool, and on how much descriptive text you provide in those comments.

### 1.2 Learning Objectives

By the end of this chapter, you should be able to:

* Understand how API documentation can be generated from source code.
* Discuss how basic generated documentation can be improved.
* Identify some common generation tools.

## 2 Generating API Documentation

### 2.1 Annotating Source Code

Documentation generation tools typically produce API documentation from source code or specifications by extracting structural information from function and data type definitions, and looking for specially formatted comments and tags that identify and describe public elements.

To make your API source code "self-documenting" with these tools, you have to add the comments and tags to the source code. Your coding standard should include the task of checking for and adding the documentation framework as part of your code review process.

Source files that define classes and functions, like myClass.java, provide structural information for native-code APIs. For languages like C/C++, header files (*.h) define the data structures and the function and class signatures, but do not contain the implementation code.

Tools like [Doxygen](https://www.doxygen.nl/), [JavaDoc](https://javadoc.io/), and [GitBook](https://www.gitbook.com/) require a specially-formatted comment on public elements in the source or header files from which to generate documentation.

* For interpreted languages like JavaScript, the source for structural information is the actual implementation file (*.js). Tools like [JSDoc](https://jsdoc.app/) look for the same kind of documentation-specific comment on the definitions of public elements.
* [Sphinx](https://www.sphinx-doc.org/en/master/) is a Python tool that can generate documentation from comments in any kind of text file, including CLI source code.

For REST APIs, tools such as [Swagger](https://swagger.io/) and [Redoc](https://redoc.co/) generate documentation from YAML or JSON API description files that conform to the OpenAPI spec.

### 2.2 Supporting Documentation for Open Source Code

For an open source project, it is particularly important to document exactly how the generated documentation is produced. Contributors need to know what tools are being used, and how those tools are configured.

* Code contributors need to know whether and how to add the comment infrastructure to new definitions, and whether and how to add new files to the document-generation infrastructure.
* Community members who want to edit or add to documentation need to know how and where to make changes. A contributor can easily make the mistake of editing a generated documentation file directly, only to find their contributions overwritten the next time the automatic doc-generation job runs.

Encourage both kinds of contribution and multiply the value of your doc-generation tools by including documentation requirements in your contribution policies and instructions.

## 3 Adding Value to Generated Documentation

### 3.1 Ways to Improve Generated Documentation
Typically, tools generate one HTML page per major element with all syntax represented. The output is configurable—usually with a makefile or configuration file—with options that control the look and feel and heuristics that control what information is included.

All of these tools are optimized for syntax representation, not for semantic description. Basic listing of things like parameter names and types is built into the format, but you can and should add useful descriptions. Tools generally include a "description" property or tag where you can add a descriptive string that explains the meaning and intended usage of each element.

Description fields are not given default values. Even if your comment template includes the placeholders for descriptive strings, the semantic content still has to be added. If you don't add it, you get a bare-bones listing of syntax details, like property names, types, and allowed values—but users have to figure out for themselves what those values mean, and what the intended usage might be.

Even when the engineers do add descriptive doc comments in the source, they can almost always be improved. The API developers are a) not usually professional writers, b) not looking at the entire public API, and c) usually focused on implementation, rather than the user experience.

* If you want a professional writer to help you add and edit semantic descriptions, that person needs access to the source code. Choose a technical writer who understands software development and can be trusted to maintain the integrity of non-comment code. They don't have to be an expert developer or be able to program in the language you are using, they just have to learn the syntax and be able to read the code.

* For an open source project, encourage documentation contributions from community members with editing and writing skills by specifying the project's documentation requirements and standards. 

* Make sure your project has a way to label documentation issues, and a policy for doc contributions. If your generated documentation has an "Edit this page" option, make sure it points to the doc-contribution policy. The policy should describe how and where to make changes that are compatible with the automatic generation process, and also list specific subject-matter experts who can review and approve documentation contributions in their areas.

### 3.2 Adding Overviews and Introductions to Generated Docs

Conceptual information that explains what an API is used for and how it is intended to be used cannot be generated directly from annotation on the source code. Instead, you must explicitly add text-only pages such as overviews and introductions to the set of files your tool is parsing and formatting.

Typically, an overview page for each class or resource should include a description of how, why, and when to use that class or resource, along with an index of what methods or operations are supported. The index can link directly to the generated syntax page for each element, so that it serves as a navigation aid for users.

You can also create entire additional API documents, such as conceptual guides and tutorials, directly in markup and HTML (or whatever format your tool uses), and configure the tool to add them to the generated syntax pages.

### 3.3 Exploring API Documentation Tools

There are many API documentation tools, frameworks, and platforms to choose from. The choice of tool often depends on the programming language, project requirements, and personal preferences. You should explore and evaluate different tools based on your specific needs before deciding on the most suitable tool set for your project.

The following table lists a few common tools that can either generate API documentation from source code or specifications, or integrate with generation tools to produce comprehensive documentation sites that include the generated content. There are, of course, many more such tools becoming available every day in this evolving and fast-growing field.

| TOOL | DESCRIPTION | API TYPE |
|------|------|------|
| [DapperDox](http://dapperdox.io/) |Open source API documentation generator and server for OpenAPI Swagger specifications. Combines specifications with documentation, guides and diagrams, all of which can be authored in GitHub flavored Markdown. | REST |
| [Doxygen](https://www.doxygen.nl/index.html) | A widely-used documentation tool for C++, C, Objective-C, and several other programming languages. It generates documentation from source code comments and supports multiple output formats, including HTML, PDF, and LaTeX. | Native code |
| [Javadoc](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html) | A documentation tool specifically designed for generating API documentation for Java projects. It extracts comments from the source code and produces HTML-based documentation. | Native code |
| [JSDoc](https://jsdoc.app/) | A markup language used to annotate JavaScript source code files. Similar to Javadoc, but specialized to handle JavaScript's dynamic behavior. | Native code |
| [RapiDoc](https://github.com/rapi-doc/RapiDoc) | An interactive tool that lets you create visually appealing documents using the OpenAPI specification, with a console for making API calls and testing APIs. | REST |
| [ReadMe](https://readme.com/) | A platform that helps you create, manage, and maintain an online developer hub with different kinds of documents. Can automatically generate interactive API reference documentation from OpenAPI, RAML, or GraphQL specifications. Integrates with various development tools and services, such as GitHub, GitLab, and Slack. | REST </br> Native Code |
| [Read the Docs](https://about.readthedocs.com/) | A documentation hosting platform that integrates with popular documentation generators like Sphinx and MkDocs. Automatically builds and deploys documentation from your source code repository, using the "docs as code" pattern. | REST</br>Native Code |
| [Redoc](https://redocly.com/docs/redoc/) | Produces web-ready documentation from an OpenAPI description or Swagger. | REST |
| [Redocly CLI](https://redocly.com/docs/cli/) | Open source command-line tool for working with OpenAPI descriptions, developer portals, and other API lifecycle operations including API linting, enhancement, and bundling. | REST |
| [Sphinx](https://www.sphinx-doc.org/en/master/) | A documentation generator commonly used in the Python ecosystem. Supports multiple markup languages, including reStructuredText (RST) and Markdown. Sphinx can generate various output formats, such as HTML, PDF, and ePub.	| REST </br>Native Code |
| [Stoplight](https://stoplight.io/) | Platform that includes tools to generate API documentation from an OpenAPI specification. Includes templates for API Overview pages, Quick Start Guides, and How-to Tutorials. | REST |
| [Swagger Codegen](https://swagger.io/tools/swagger-codegen/) | Generates an interactive HTML interface that allows users to explore the API endpoints, parameters, request/response examples, and more. | REST |