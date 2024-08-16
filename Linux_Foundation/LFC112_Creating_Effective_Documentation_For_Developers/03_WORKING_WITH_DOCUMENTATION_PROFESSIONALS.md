# WORKING WITH DOCUMENTATION PROFESSIONALS

## 1 Introduction

### 1.1 Chapter Overview
Asking your development team to document their own code has a real impact on your development effort. Coders are not typically or primarily natural-language writers; the skill of writing code is different from the skill of writing natural language. Even when engineers have good writing and communication skills, they are usually not familiar with the planning and organizational issues and problems of producing technical documentation. Also, writing tasks are generally at odds with coding and code design responsibilities, in the sense of both task allocation and the frame of mind required to do the tasks.

In short, it is more efficient, and yields better results, to assign the planning and production of your documentation to technical communication professionals. Your engineering resources can contribute to the quality of documentation by providing technical information to writers, and reviewing draft content.

### 1.2 Learning Objectives
By the end of this chapter, you should be able to:

* Identify the skills needed for effective information transfer.

* Plan for the documentation effort as part of the software development process.

* Understand how software engineers and professional writers and editors collaborate to improve existing documents and create new ones.

## 2 Transferring Knowledge from Experts to Users

### 2.1 Effective Knowledge Transfer Requires Specific Skills
The purpose of technical documentation is to transfer knowledge efficiently from the people who have it (such as the development team for an open source software application) to people who need it (such as developers who want to use an API).

The effectiveness of product documentation is measured by user success. A successful user is one who has been able to find and understand the information they need to accomplish their tasks. You can tell that your product documentation needs work when your support team is swamped helping new users get started, your engineering teams are doing a lot of hand-holding for current users, and your marketing team is having trouble getting evaluators to understand the product's benefits and strengths.

Creating effective documentation for a complex technical subject requires two specific skill sets.

- **Knowledge engineering**

    The art of eliciting information from one or more subject-matter experts (SMEs) and analyzing it with the specific goal of understanding and communicating that information to others.

- **Information architecture**

    The art of organizing, arranging, and presenting a body of knowledge so that it is accessible to different kinds of users and potential users.

Experienced technical writers develop these skills. The knowledge engineer understands and recognizes different kinds of knowledge, such as factual and procedural. The information architect understands how people can most easily absorb each kind of knowledge. For instance, when does a user need a look-up table, and when do they need a tutorial?

While some software architects and engineers have decent or even excellent writing and communication skills, this is not their primary area of expertise. They are also fully occupied with designing and building the software. For others, writing is a struggle, and expecting them to do very much of it is not making good use of their time. It is generally more constructive for a development team to work with professional writers and editors to produce the quality of documentation that will attract users and contributors, and enable people to learn and use their software successfully.

### 2.2 Knowledge Transfer in Open Source Communities

In an open source project, it's particularly important to identify and recruit community members with writing and editing skills to work with software coders and architects. Writers and editors need to be aware that their skills are needed and appreciated, and engineers with no interest in writing need to be aware that those resources are available to them.

In your community blogs or forums, encourage participants to think of documentation production or improvement as a collaborative activity that benefits both the writer and the coder. A writer or editor improves their product knowledge by focussing on a subject area, and a SME that works with a writer or editor learns about the user viewpoint and might even improve their design choices when they see which things are harder to explain.


## 3 Creating a Documentation Plan

### 3.1 Plan a Document Suite
To fully document your product, you need a set of documents that address different kinds of users and contributors, providing the different kinds of information they need to accomplish different goals. Creating a documentation plan is the first step in producing a documentation suite that meets your business and project needs and enables your users to be successful.

For an open source project, community engagement is a key element of planning. Writers and editors in the community should be encouraged to collaborate with technical experts in order to build a documentation plan that will open the door to continuing doc contributions.

A plan tells you what documents you will need, who they are addressed to, their relative priorities, and how they can be produced efficiently as part of your software development process. The first step is determining which documents to create.Think about what the documentation needs to accomplish.

For any software product, you want to attract users by explaining how your product can help them, and make them successful by providing the information they need to accomplish their tasks and goals. → Think about who your potential users are, their roles and workflows, and how they can use your tools to accomplish specific goals.

For an open source project, you also want to attract contributors by explaining how they can join the project and become part of the community. → Think about who your potential contributors are, their interests, and what contributions they could make.

Review the standard document types from [Open Source Technical Documentation Essentials (LFC111)](https://training.linuxfoundation.org/training/open-source-technical-documentation-essentials-lfc111/?_gl=1*vjwotx*_gcl_aw*R0NMLjE3MjM3OTkxMjMuQ2p3S0NBanc4ZnUxQmhCc0Vpd0F3RHJzakpSSndndjF5TWlxUDUxdEtWVk9lcE5jQVpOYkdmVEVhZl9nd1R6d0dTT2J5V2Q2ZTlTS01Cb0N6Rm9RQXZEX0J3RQ..*_gcl_au*ODE0NjI3NDAuMTcyMzc5OTEyMw..*_ga*MjY3MjA0MzA4LjE3MjM3OTkxNDU.*_ga_EMX7DDZMX4*MTcyMzgwOTA3My4zLjEuMTcyMzgxMjExMS4yMC4wLjA.*_ga_VWZ4V8CGRF*MTcyMzgwOTA3My4zLjEuMTcyMzgxMjExMS4wLjAuMA..) and decide which ones your expected users will need to use your product. Consider the relative priority of particular types of documents, according to the maturity and usage patterns of your product.

### 3.2 Create Document Specifications

For each document that you decide is needed, your documentation plan should include a document specification. A document specification doesn't have to be detailed and comprehensive, but should cover the following points.

- **Project Objectives**. How will this document support the needs of your business, community, and stakeholders?
- **Audience**. What type of user does this document address? What is their role?
- **Technical Objectives**. What goals and tasks will this document help the reader accomplish?

- **Pattern to Use**. How will the information in this document be used as part of a specific workflow?

- **Content**. What subject areas will be covered in this document?

- **Delivery Medium**. How will this document be made available to users?

User roles and personas have typical workflows and goals, which suggest patterns of use, and therefore content. For instance, an evaluator needs to know the tools benefits, limitations, and required environment to decide on adoption. The document they need is a high-level technical overview. A coder needs to look up the type of an input to make a call to the API, so they need a detailed API reference.

For more detailed information and examples of each of these points, see [Quick and Easy Document Specifications](https://expertsupport.com/library/quick-and-easy-document-specifications/).

## 4 Planning for the Documentation Effort

### 4.1 Working with Technical Writers

When a project manager for a commercial product works with a professional technical writer they should know what to expect and plan for. Similarly, the planners for an open source API-based application or service need to know how writers and editors in the community can collaborate with technical experts to produce quality documentation.

You can build documentation in the same way you build your software, and at the same time, using the same tools. The open source tool [Backstage](https://backstage.io/), for example, provides documentation templates as part of a comprehensive build-and-test infrastructure. You can plan for conceptual, reference, and support documents. All you need to do is add the content—and that's where a professional technical writer comes in.

It is the writer's responsibility to learn the subject matter, and it is the responsibility of the development team to teach it. Writing can and usually does run concurrently with software development. You cannot, however, decide in advance exactly when each phase of writing will begin and end, or predict exactly how long it will take. To plan for documentation that is excellent and finished in time to accompany the software, you must give documentation tasks enough priority to allow engineers to interrupt their other activities in order to answer questions from the writer.

A project manager (when there is one) must allow time for the development team to work with the writer. Some activities can be explicitly scheduled between participants, but others are, by nature, interrupt-driven. Because the team (and especially the architects and experts who have the bulk of the information) is fully occupied with producing the code and fixing bugs, it helps to create slack in the schedule, if possible. The best way to facilitate the documentation process is not with explicit scheduling, but by creating a culture in which developers make time for documentation tasks. The development team should feel free to spend some of their time answering questions and reviewing drafts.

Without willing cooperation of the development team, documentation doesn't get done or is done poorly. Developers need to know that, even if they don't want to do it, collaborating with the tech doc team is the least painful option with respect to optimizing their on-programming-task hours. Managers should make developers understand how taking unscheduled time out of their day to work with writers will save them time and aggravation overall—as compared with trying to write the documentation themselves or handhold frustrated users.

If there is no specific project manager for an open source project, subject-area specialists should be expected to document their own contributions as best they can, and then actively solicit help from writers and editors in the community to help them develop that material into publishable documentation.

### 4.2 Planning for Open Source Documentation

For an open source project, the community needs to be involved in documentation planning. Technical experts who recognize the need for better documentation in their areas should be able to solicit help from writers. Similarly, writers in the community should be able to find and collaborate with experts to produce new documentation or improve existing documents.

In open source, communicating what needs to be done, even when you may not be the one that will be doing the work, is a valuable technical writing skill. Creating a well-defined, actionable issue is a specific skill, whether or not the issue is specifically for documentation. Documentation issues must be clear about what needs to be done, and about what skills and collaborations will be needed to accomplish it.

It is important for the project's contribution policies to include explicit support for how to create documentation issues. A template for doc issues, for example, can guarantee that a writer who undertakes the issue can find an appropriate technical source to work with, or vice versa.

### 4.3 What to Expect from the Writing Process

#### Phase 1: Information transfert from experts

Subject-matter experts (SMEs) on the development team need to provide the information the writer—like other new users—needs to learn. They can do this in whatever way is most suited to their skills and preferences.

- Written brain-dump
    An engineer who is at all comfortable with writing can write up what they think users need to know about their subject area. They don't have to worry about how it is stated or make it pretty—it is just a starting point for the writer. It can be in any form or format, such as a shared document or email.

- Interviews/chalk talks
    Early in the schedule, you can schedule interviews between the writer and SMEs in each major area. The SME will explain what they think users need to know, and the writer will take notes and ask questions.

- Answering questions
    As someone new to the project, the writer will be missing the background information and context that the experts take for granted. Using the initial information as a starting place, they will go back to the expert to explain anything they have trouble with. This gives the expert an opportunity to provide a more complete picture that takes new users into account.

The writer will begin writing drafts, and work with each source to make sure they understand the information correctly. Communication style can be agreed according to the engineer's preferences.

#### Phase 2: Technical review cycles from SMEs

As the writer produces a draft of each section, they will send it to the appropriate SME for careful review to ensure accuracy and completeness. The writer will mark or highlight questions and guesses. The engineer will be expected to answer questions, and confirm or correct guesses.

This is an iterative process, as each change must be edited by the writer, and reconfirmed by the engineer. Some sections will be ready for review sooner than others, and the writer can collect more information on other subjects while an earlier section is undergoing review.

#### Phase 3: General review cycles from other team members

After the writer and SME are satisfied with the accuracy and completeness of a section, the section should get a general review from other team members. A general review ensures that the information is communicated clearly to non-experts.

- Reviewers can be development engineers with other specialties, support and QA engineers, product managers in both engineering and marketing, and even partners and beta testers.

- A shared review document allows all reviewers to see each other’s comments and suggestions, and even answer each other’s questions.

- The writer retains a master copy, edits and incorporates changes, and checks with the SME to ensure that the information is still accurate.

### 4.4 What the Writer Will Do

- Work with the team to create a doc plan
    - Determine what documents to produce.
    - Determine the relative priorities of different subject areas and documents.

- State the information they collect clearly, unambiguously, and consistently
    - Create and maintain a glossary of terms to ensure consistent usage.
    - Create or follow a style guide to ensure uniformity of language.
    - Create or follow page templates to ensure uniformity of presentation.

- Organize the information to present it effectively to different kinds of users
    - Sort out which users need which information.
    - Develop a learning journey for new users.
    - Tailor the breadth and depth of information in each section to particular audiences.
    - Evaluate and tweak the presentation templates and content distribution.

- Work with reviewers
    - To ensure completeness and accuracy of all technical details.
    - To ensure clear communication to intended audiences.

- Prepare the documentation for publication
    - Copy-edit and ensure consistent use of terms and styles.
    - Ensure use of language is suitable for localization.
    - Check example code.
    - Check accessibility on supported platforms.
    - Check navigational links.
