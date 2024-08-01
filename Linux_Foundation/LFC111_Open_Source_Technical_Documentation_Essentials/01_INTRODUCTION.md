# INTRODUCTION

## 1 Introduction

### 1.1 Chapter Overview

An open source product or service needs to attract users, enable their successful use of the tools or API, and encourage community involvement. Technical documentation is a key ingredient in accomplishing these goals. Good documentation can make the difference between success and failure for your project or product.

> The effectiveness of documentation is measured by the success of users.

### 1.2 Learning Objectives

By the end of this chapter, you should be able to:
* Explain how effective documentation makes a difference to you and your user community.
* Understand how the user viewpoint differs from the developer viewpoint (even when your users are developers).
* Discuss how user-oriented design improves your API.
* Identify the potential audiences for your documentation to determine whether your existing documentation serves the needs of different types of users.
* Identify a set of documents that can help different types of users be successful with your software and API.

## 2 Importance of API documentation

### 2.1 How API Documentation Helps Open Source Products and Services

A good idea for a useful or original open source product or service, especially in the fast-growing cloud-native computing world, is not enough to turn this concept into a reality.

Of course your product needs great design and implementation, but if your prototype is ever to grow into a fully-realized product, you need to attract users and make them understand what you have to offer. You need to know who your target audience is, attract their attention, and communicate your idea to them quickly and clearly.

Once you have attracted their attention, you need to make sure they can learn how to use your API and tools correctly and effectively to achieve their goals. Your reputation rests on their successful use of your product. Wide adoption depends on demonstrated ease-of-use and effective application.

An open source project in particular needs to build a user community, whose involvement extends beyond simple adoption. Success depends on attracting the attention and enthusiasm of potential contributors, and enabling their contributions.

Poor or missing documentation is among the most frequent complaints of API users. Ineffective documentation has real costs to users in time and productivity losses, and to product developers in support costs and reputation. Effective documentation, on the other hand, significantly reduces support costs and increases adoption.

The existence and quality of your documentation can make or break the success of your developer-oriented product or service. Understanding how to evaluate and address your documentation needs is just as important as getting the code right.

### 2.2 It Is Open Source—Why Can't They Just Read the Code?

Maybe potential users can figure out how to use your API by just reading the code - but will they understand how you mean it to be used, and how to use it effectively and efficiently? Even an experienced developer might not have exactly the right background or might not want to go through that long, painful, and frustrating process to get started. If the barrier to adoption is high, they are going to be looking for another option.

No matter how well you understand your product, you have to be able to make others understand it, or they will never be able to use it successfully. Even new members of your own team have to learn what your API or tool is for, what it does, and how it does it before they can contribute to its development.

Even after adoption, successful use of your API or tool depends on complete, accurate syntax information that is easily discoverable, and on clear communication of the intended usage of every element. Inconsistent use of terms and descriptions that are difficult to parse can render even a well-designed API unusable.

You can jump-start the learning curve for new users by providing documentation. The better the documentation, the more quickly they can get up to speed, and the more likely they are to become productive. Achieving good technical communication, however, is not trivial. It takes a variety of techniques and skills. A technical writer needs to:
* Focus on the user viewpoint.
* Present the information that specific types of users need to perform specific tasks.
* Balance the factual information that users need to perform tasks with the conceptual information they need to understand when and how to perform those tasks.

## 3 Taking the User Viewpoint

### 3.1 Understanding the User Viewpoint

On your development team, you are used to talking to people who already know the context - other developers on your team, your managers, your testers, and maybe some partners. This means the context is largely invisible to you. When presenting your product or technology to someone outside that circle, you need to start with a clear description of the context within which you operate.

When the designers and engineers first attempt to create documentation for their code, they typically take what we call the provider-push perspective. If you ask a software designer or developer to describe their application, they naturally talk about what it is capable of; that is, what features it has. When the team is talking about it among themselves and in design documents and specs, they mostly describe what problems need to be solved, and the pros and cons of different possible solutions. When thinking about usage, the team tends to focus on design goals like security and performance.

To make users successful, however, documentation needs to reflect the users' viewpoint. User documents need to take what we call the user-pull perspective. Before you can plan what information to include and think about how to present and organize it, you have to consider who your users are and what they need to do. Are there different kinds of users with different goals? What will they want to do with your application and API? What workflows is the tool or API a part of? What tasks will your users need to do in what circumstances?

### 3.2 User-Oriented Design

To make sure your documentation reflects the user-pull perspective, you must carefully consider who will use your product, what tasks they will need to do, and exactly how they will accomplish those tasks. The benefits for documentation are obvious - you can aim explanations at a particular audience, and provide the specific information needed in a specific circumstance. There are additional benefits, however, that you might not have considered.

Taking the user perspective (as part of the documentation effort) leads to exposing pain points and gives the team an opportunity to clean up the API design in order to improve the user experience.

When you start writing about an API or complex tool, you will find that some things are hard to explain. Some concepts might be difficult, but the process of explaining them (to a technical writer or new user) clarifies your thinking about how much really needs to be user level. Which elements really need to be public? You often find that some things can be provided through utilities or taken care of internally, easing the burden on the end user. In an open source project, what needs to be surfaced in documentation for end users, and how much implementation detail needs to be documented and supported for contributors?

When you start thinking about and writing about exactly how to use your API, for instance, you might find that the original design doesn't have the clarity and consistency that maximizes ease of use. Considering the user experience early in development provides a valuable opportunity to tweak and streamline the overall design.

> An API or tool that is easier to explain is also easier to learn and easier to use.

## 4 Know your Users

### 4.1 Identifying the Audience and Their Needs

The content of your documentation should reflect the user viewpoint, and every potential user needs to know if the information on a page is going to be useful to them. It is discouraging for a new or unfamiliar user to be plunged into detailed discussions that they have no hope of understanding. Similarly, an experienced user who is trying to find a specific technical detail doesn't want to hunt through an elementary tutorial or conceptual discussion to find it.

When you present information, think about who needs that information and what background they need to understand it. Each document and each section in each document should make clear:
* Who is the intended audience for the information;
* What background they are expected to have;
* Where they can go to get that background;
* How you expect them to use the documentation.

### 4.2 User Goals and Information Needs

Different types of readers can have very different needs and goals, and your doc plan has to take that into account. For example, the following common types of both external and internal API or tool users have specific goals, tasks, and information needs.

| Audience | Goal | Information needs |
| ------ | ------ | ------ |
| Evaluators | Determine if this service or tool or API is useful | High-level overview of functionality</br>List of features; Expected benefits</br>Known deficiencies |
| New users | Learn the usage framework and conventions | Getting started(authentication, authorization, and access)</br>Basic concepts</br>“Hello World” example</br>Recipes for common use cases |
| Users of specific features | Use feature to accomplish task | Feature/task breakdown</br>Task-based procedures</br>Syntax details</br>Usage recommendations and examples |
| Advanced users | Troubleshoot</br>Optimize</br>Apply to unusual use cases | Full API reference</br>Design information</br>Intended usage</br>Caveats |
|  QA & Tech support | Test</br>Troubleshoot</br>Advise | Full API/CLI reference</br>Update/upgrade/migration</br>Common problems</br>Intended usage |
| Administrators | Build engineering</br>System configuration | Architecture, dependencies</br>Full configuration reference</br>Full CLI reference |
| Contributors | Extend the system or documentation	| Full API/CLI reference</br>Architecture/design decisions and directions</br>Contributors guide (submission rules/coding conventions)</br>Doc style guide, including glossary of terms |

### 4.3 Documentation for Contributors

Open source projects have a specific need to attract, encourage, and enable contributions to both their code base and their documentation from members of the community.

Contributors in particular can benefit from in-depth documentation that goes beyond the user layer. Developers who want to contribute can do so most effectively when they understand design goals and implementation choices - the kind of information that would be considered internal in a traditional project. When you create a documentation plan for an open source project, it is particularly important to consider these needs.

In addition to in-depth documentation, potential contributors need information about the contribution process.

#### Contribution guidelines

Members of the community need to know how to contribute. Your project needs to document specific and clear contribution guidelines. This article goes into some of the issues folks run into and how to mitigate them: _["Do you want to start contributing to open source and need help figuring out where to begin?"](https://contribute.cncf.io/contributors/getting-started/?_gl=1*198tlek*_gcl_au*MTIzMTEzODg0NC4xNzIyNTE0Njc5*_ga*MTI1ODkwNjU2MS4xNzIyNTE0Njc5*_ga_VWZ4V8CGRF*MTcyMjUxNDY3OC4xLjEuMTcyMjUxNjk5Ni4wLjAuMA..)_.

#### Contributing to documentation

The documentation itself is an important area of contribution. Your project is most likely to get writers to contribute if you have specific policies and procedures for submitting and undertaking documentation issues. You can provide documentation process and style guidelines along with coding process and style guidelines. Your contribution policies should include information about subject matter experts in all areas that need documentation.

#### Skill & tool requirements

Open source writers often have to overcome technical hurdles to start contributing. These technical hurdles can include things like getting started on GitHub (or GitLab or other similar system), understanding what a Pull Request is, how to make one, and how to edit one after someone suggests feedback. Often, a documentation set is part of a website, and the technical writer could be expected to make sure that it runs on their system (or in something like Codespaces) so that they can see that the changes they've made don't break the site, or page styling.

#### Community interaction

Working in open source isn't like getting hired into a company; it's more like becoming a part of a community, and those community members are often volunteers - this can affect the experience of writing in open source. Even if an update is a welcomed and anticipated contribution, it can still take a while for someone to get to reviewing it. Working with the community also helps identify subject matter experts; it can be hard to tell by looking at a list of commits who is an expert, but attending community meetings (where offered) is an excellent way to meet folks who can help point you in the right direction.