# CREATING AN IDEAL API REFERENCE DOCUMENT

## 1 Introduction

### 1.1 Overview

Ideally, an API reference is part of a complete documentation suite that includes more detailed conceptual information and usage recommendations. However, it is often the first documentation produced for a new API, because developers can’t use the API without it. In addition, the API reference can act as a language specification for the API development team.

Even when there is additional documentation, the API reference is particularly important because there are always some developers (often the early adopters) who will depend entirely on the reference to learn and understand the system, regardless of what other documentation you provide.

### 1.2 Learning Objectives

By the end of this chapter, you should be able to:
* Understand how an API reference differs from other types of documents.
* Discuss why you need both high-level conceptual documents and low-level detailed reference documents.
* Identify the different major types of APIs.
* Recognize what to document for different types of APIs.

## 2 Understanding API Documentation

#### What Needs to Be Documented for an API

An API is a coding language. Coding languages are similar to natural languages in that they follow rules of both structure and usage. They differ in that the rules are rigid and inflexible, and must be followed exactly for the code to work. To use an API successfully, a programmer needs to know the syntax and semantics of the language the API is written in, and also the specific rules that apply to the API elements within that language.

**Syntax** is the _structure_ of the elements:
* names of elements
* ordering and type requirements
* rules of construction for statements

**Semantics** is the _meaning_ of the elements:
* how elements are related
* what statements do

The primary function of an API reference is to describe the syntax and semantics of the APIs public elements, in enough detail that a programmer can use the language correctly to write working code.

This particular document is specifically meant to be used for reference. You can expect a programmer or developer to use it while coding to look up the exact syntax or language element they need to use, as they need it. To use the element correctly, however, they need to understand more than the syntax. They need to know, for instance, what each possible value of each input means, and how that value affects the result of the call.

Developers need to know nuances of meaning that might not be obvious from the code. Consider, for example, a property defined as name. Its meaning is probably obvious to the developer who named it, and if they provide a description at all, it might be:

**@param** **name** _The name of the widget._

This description is no more useful than the property name itself, because it does nothing to clarify the context and intention that the developer assumed was obvious.

An adequate description adds value and disambiguates. A description in reference material should be as explicit and specific as possible, while still being stated in terse and straightforward language. For example, this property might be used to mean any of the following (_table: Property name and Its Possible Meanings_).

| PROPERTY | DESCRIPTION |
|------|------|
| name | A localizable display string.|
| name | A descriptive display label.|
| name | An identifying string, unique within the scope of the request.|
| name | A generated opaque identifier, as returned by the creation function.|
| name | A developer-defined unique identifier used to associate a response with a specific request.|

This kind of description adds information about the source, expected usage, and constraints on the information being passed. It greatly increases the probability of the described element being understood immediately and used correctly by both new and experienced users.

## 3 Suitable API Reference Content

#### API Reference Content vs. Content for Other Document Types

To use an API, a programmer needs to gain access to it and understand the environment in which it is used. The use cases for your API, and the tasks your API enables within your domain and within a particular development environment are the context for the factual reference details of how to make calls.

It is important for an API reference to establish enough context to make the technical details useful to developers. Context establishes what the API is for, generally what features it has, and what a developer is supposed to do with it. For someone who is not already familiar with it, it can be very difficult to figure out the bigger picture from technical details alone.

High-level introductory and semantic information in the reference provides context for the low-level specific syntax information. This applies to both the API as a whole, and to each element.

* An API reference should provide an overview of what the API does and is used for overall, as well as introductory descriptions that describe what each major element does and is used for.

* An API reference should include code examples in the form of snippets that illustrate the correct usage of particular elements and special parameter values. Introductory text should clarify what each example demonstrates.

* An API reference is not the place for tutorials, extended examples, or in-depth conceptual discussions. These things are important, and should be provided somewhere in the product documentation—just not in the API reference. If a conceptual and usage document is available, the reference should contain links or pointers into it.


## 4 Reference Content for Different Types of API

### 4.1 API Documentation Requirements

An API reference document should provide basic information about how to access and use its associated API, and what background knowledge or preparation is assumed. To use a REST API, for example, developers are expected to know how to use the HTTP/HTTPS protocol and the data-transfer format (such as JSON). The reference needs to provide specific authentication and authorization details and the base URI for resources. Basic usage information also includes things like supported languages and platforms, error handling, how to get paged results, and so on.

Beyond that introductory material, the reference must provide complete syntactic details and semantic descriptions of every public element. The specific elements that need to be documented are different for the different kinds of API.

There are three basic types of API: native-code, REST, and command-line. The structures and use cases for these APIs are different. They use different terminology, and have different documentation requirements.

#### Native-code APIs

Native code is the language in which an application or system itself is (or can be) written. An API gives developers a way to extend the system or control it programmatically. For an open source application, a complete API reference is essential to enable community contributions.

This kind of API tends to be more complex than REST APIs and command languages. Native-code APIs can include tools for formulating REST requests and handling responses.

* An API can be in a compiled language like C/C++ or Java, or an interpreted (scripting) language like JavaScript/Typescript. Scripting APIs can be available in different languages for the same app, and typically talk to apps or systems that are built in a compiled language.

* Native-code APIs can use an object-oriented approach, or a function-oriented approach (technically called a DSL, or Domain-Specific Language). These are not mutually exclusive, but the two approaches have slightly different documentation needs. Most modern languages are optimized for the object-oriented programming style. The main elements to document are classes with methods and properties, top-level functions, and data structures.

#### REST APIs

REST (Representational State Transfer architecture) provides a protocol for communicating over HTTP. A RESTful API defines specific calls using that protocol.

The [OpenAPI specification (OAS)](https://www.openapis.org/) is a de facto standard for creating REST APIs, and is very popular in the OSS community. OpenAPI initiative (OAI) doesn't use the term REST, but the terminology and documentation requirements are otherwise the same.

REST APIs are currently the most common kind of API being produced that requires public documentation. The REST API communicates between systems that are written in native code—usually a client and server. API calls typically send data back and forth between apps, but can also issue instructions to initiate some action on either end.

To use a REST API, you must have native-code systems on both ends to formulate requests and handle responses, and to produce or use the data being transmitted. The language you use to formulate calls is irrelevant to the syntactic and semantic details of the requests, responses and data schemas. A programmer can formulate calls in any number of coding languages, including many modern languages that are optimized for this purpose. Documentation typically includes examples in a variety of common languages, such as Python, C++, Java, JavaScript, TypeScript, Ruby, Go, and so on.

The main elements to document for a REST API are resources with endpoints, operations supported for each endpoint, request and response syntax for each operation, and data schemas.

#### Command-line interface

A command line interface (CLI) is similar to a REST API in that it is used to issue parameterized commands to a system. The difference is that a REST API communicates with an application or server via a network connection, while a CLI communicates with a server directly via a script or a command shell.

CLIs are generally used by administrators for system configuration, or by developers during system development. They can be used to write automation scripts for an application.

A CLI is a set of commands. Commands take input (arguments, options, and flags), perform an action, and might or might not produce output. Arguments are parameters to the command. Options are optional arguments that govern the behavior of the command, and may or may not take parameters of their own. Options that do not take parameters are flags.

_**NOTE**: It is not at all unusual for the same product to provide APIs of different types. A product can have native-code APIs in different languages, along with a CLI for configuration or administration and a REST API for client-server communication—and perhaps a scripting API for generating REST requests and handling responses._

### 4.2 Elements that Require Reference Documentation

| API TYPE | ELEMENTS |
|------|------|
| REST API | For a REST API, the reference must document the following public elements:</br>**List available resources and endpoints**</br>- Describe access and authorization requirements</br>- List supported HTTP operations for each endpoint</br></br>**For each endpoint operation**</br>- Provide request details and parameters</br>- Provide successful and unsuccessful response details</br></br>**For data objects being transferred**</br>- List and describe all properties in each schema</br>- For each property, list and describe allowed values |
| Native-code API |For a native-code API, the reference must document the following public elements:</br>**List and describe all classes (or object types or interfaces)**</br>- Describe instantiation (object creation)</br>- List and describe all properties (data) and methods (actions)</br>**List and describe all top-level functions (meaning functions that are not object methods)**</br>**For methods and functions, show all inputs (parameters) and outputs (return values)**</br>**For properties, list and describe allowed values**</br>**List and describe all data structures (types and enumerations)**</br> |
| CLI | For a CLI, the reference must document the following public elements:</br>**List and describe all commands (actions)**</br>**For each command, list and describe arguments and options**</br>- Arguments are variables; list and describe allowed values</br>- For options, list and describe all required and optional parameters with allowed values |