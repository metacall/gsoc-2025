# Google Summer of Code 2025
List of project ideas for contributors applying to the Google Summer of Code program in 2025 (GSoC 2025).

## Timeline/milestones

Please always refer to the [official timeline](https://developers.google.com/open-source/gsoc/timeline).  
  
## Application Process

#### 0. Get familiar with GSoC

First of all, and if you have not done that yet, read [the contributor guide](https://google.github.io/gsocguides/student/) which will allow you to understand all this process and how the program works overall. Refer to its left side menu to quick access sections that may interest you the most, although we recommend you to read everything.  
  
#### 1. Discuss the project idea with the mentor(s)

This is a required step unless you have dived in into the existing codebase and understood everything perfectly (very hard) and the idea you prefer is on the list below.

If your idea is not listed, please discuss it with the mentors in the available [contact channels](https://github.com/metacall/gsoc-2025#find-us). We're always open to new ideas and won't hesitate on choosing them if you demonstrate to be a good candidate!  
  
#### 2. Understand that

- You're committing to a project and we may ask you to publicly publish your weekly progress on it.
- We will repeatedly ask you to give feedback on our mentorship and management.
- You wholeheartedly agree with the [code of conduct](https://github.com/metacall/core/blob/develop/.github/CODE_OF_CONDUCT.md).
- You must tell us if there's any proposed idea that you don't think would fit the timeline or could be boring (yes, we're asking for feedback).
  
#### 3. Fill out the application form

We recommend you to follow [Google's guide to Writing a Proposal](https://google.github.io/gsocguides/student/writing-a-proposal) as we won't be too harsh on the format and we won't provide any template. But hey, we're giving you a starting point!

You can send the proposal link to any readable format you wish: Google Docs, plain text, in markdown... and preferably hosted online, accessible with a common browser without downloading anything.

We **highly recommend you to ask for a review** anytime to the community or mentor candidates before the contributor application deadline. It's much easier if you get feedback early than to wait for the last moment.
  

## Project Ideas

You can also propose your own.

### Full Tutorial: Frontend & Backend & DB or Services

**Skills**: NodeJS / TypeScript, Python, React / Angular, Others, Markdown

**Expected size of the project**: Large (350 hours)

**Difficulty rating**: Medium

**Description**:

At the moment of writing, MetaCall has reached a stable point where adding new features to the tooling is not as necessary as showing the usage of the tooling itself. In this project we want to create a tutorial showing the full lifecycle of developing a complete application with MetaCall. The project has complete freedom for selecting language or framework for developing it, it will be interesting to use new technologies and also well known if possible. For achieving this, we will need to cover:

 1) Explain how to install MetaCall in Windows, Linux and MacOs.
 2) Develop a polyglot app with MetaCall, including Frontend, Backend and some services, for example using Python for doing something related to AI or math which cannot be done with NodeJS.
 3) Show how to develop the whole service locally with Deploy and FaaS tools.
 4) Deploy to the commercial FaaS and show the final app in production.

All this process should be documented with markdown, also we will highly value if there are videos that we can upload to MetaCall's YouTube Channel. This should show the whole lifecycle of development and should be basic enough for people that does not know anything about MetaCall beforehand.

**Expected outcomes**: A complete tutorial written in markdown, with the code of the sample application developed, images and videos (or any other resource that can help to explain better the tutorial).

**Possible mentors**: Vicente Eduardo Ferrer Garcia, Gil Arasa Verge

**Resources**:
 - MetaCall Install: https://github.com/metacall/install
 - MetaCall Deploy: https://github.com/metacall/deploy
 - MetaCall FaaS: https://github.com/metacall/faas
 - MetaCall Commercial FaaS: https://dashboard.metacall.io
 - MetaCall YouTube Channel: https://www.youtube.com/c/MetaCall

### Rust Port Update

**Skills**: Rust

**Expected size of the project**: Small (90 hours)

**Difficulty rating**: Medium

**Description**:

[Rust Port](https://crates.io/crates/metacall) is the wrapper of MetaCall for using multiple languages from Rust. We support Rust already but recently we have been using it in a more advanced environment, for example in our [MetaSSR](https://github.com/metacall/metassr) project from last GSoC year. We have noticed that there is some limitations with the current port implementation that must be addressed:

  1) from improvements in the usage of the API,
  2) sugar macros for easy usage (HList),
  3) bugs in the design of the async API
  4) bugs in the implementation of the pointer API
  5) or memory leaks, specially with async,
  6) in the build system, allow to use an already installed version of MetaCall instead of compiling it from scratch.

Those problems should be addressed and it will be also interesting to improve the documentation, tests and examples.

**Expected outcomes**: Address all the current requirements for MetaSSR project and the bugs related to the current version. Add more tests, documentation and examples to the project. Writing an article or tutorial showing the usage of the Rust project would be also interesting.

**Possible mentors**: Vicente Eduardo Ferrer Garcia, Gil Arasa Verge

**Resources**:
 - MetaCall Rust Port Code: https://github.com/metacall/core/tree/5b592ac0e9a8e498e3e706623d0a788276f566e0/source/ports/rs_port
 - MetaSSR: https://github.com/metacall/metassr
 - Previous Work: https://github.com/metacall/core/pull/538
 - Previous Issues: https://github.com/metacall/core/pull/527
 - HList Pattern: https://github.com/plausiblelabs/hlist-rs 

### Medium Sized Tutorial: Mini Polyglot Blog Application

**Skills**: NodeJS / TypeScript, Python, React / Angular, Markdown

**Expected size of the project**: Medium (175 hours)

**Difficulty rating**: Medium

**Description**:

As shown in [the first idea](https://github.com/metacall/gsoc-2025/tree/main?tab=readme-ov-file#full-tutorial-with-frontend--backend--db-or-services), this project involves creating a small, polyglot blog application that showcases MetaCall's ability to integrate different languages seamlessly. The blog will have basic features like creating, editing, and displaying posts, but different parts of the app will be implemented in different languages.

Key deliverables:

 - Frontend: Build a simple blog UI using React or Angular.
 - Backend: Implement REST or GraphQL APIs using NodeJS for blog post management.
 - Additional Service: Use Python to generate automated blog summaries using an AI library like HuggingFace or OpenAI's API.
 - Cloud Deployment: Demonstrate local development and deploy the app using MetaCall's FaaS and deployment tools.

Documentation will explain how to:

 - Set up MetaCall.
 - Develop and test the app locally.
 - Deploy to the cloud using MetaCall's tools.

**Expected outcomes**: A mini blog application with frontend, backend, and a Python-based AI service. The project should include markdown documentation and sample code.

**Possible mentors**: Vicente Eduardo Ferrer Garcia, Gil Arasa Verge

**Resources**:
 - MetaCall Install: https://github.com/metacall/install
 - MetaCall Deploy: https://github.com/metacall/deploy
 - MetaCall FaaS: https://github.com/metacall/faas

### Medium Sized Tutorial: Weather Dashboard with Polyglot Microservices

**Skills**: NodeJS, Python, VueJS / Svelte, Markdown

**Expected size of the project**: Medium (175 hours)

**Difficulty rating**: Medium

**Description**:

As shown in [the first idea](https://github.com/metacall/gsoc-2025/tree/main?tab=readme-ov-file#full-tutorial-with-frontend--backend--db-or-services), the aim of this project is to create a weather dashboard using MetaCall to mix services implemented in different languages. The dashboard will provide weather data, forecasts, and analytics.

Key deliverables:

 - Frontend: A weather dashboard UI built with VueJS or Svelte.
 - Backend: Use NodeJS to fetch live weather data from a public API (e.g., OpenWeatherMap).
 - Additional Service: Use Python to calculate weather statistics, such as average temperature or trend analysis over time.
 - Cloud Deployment: Deploy the weather app on MetaCall's FaaS platform and showcase it running online.

Documentation will include:

 - Step-by-step guide to building and integrating each component.
 - Instructions for deploying the app to MetaCall's cloud.

**Expected outcomes**: A weather dashboard app with a clean UI, backend data fetching, and Python-powered analytics, all integrated and deployed using MetaCall.

**Possible mentors**: Vicente Eduardo Ferrer Garcia, Gil Arasa Verge

**Resources**:
 - MetaCall Install: https://github.com/metacall/install
 - MetaCall Deploy: https://github.com/metacall/deploy
 - MetaCall FaaS: https://github.com/metacall/faas


TODO:
Update rust loader - Medium
Release Distributables CI (Extending existing CI) - Small
Implement C support on Windows, MacOS Core & Distributables - Large
Connect examples, faas, deploy and install with test center - Medium

## Find Us

The three chats are bridged by Matrix (messages sent from one, on the main room/channel, can be seen from all).

 - Telegram:
  <a href="https://t.me/joinchat/BMSVbBatp0Vi4s5l4VgUgg" alt="Telegram"><img src="https://img.shields.io/static/v1?label=metacall&message=join&color=blue&logo=telegram&style=flat" /></a>

 - Discord:
  <a href="https://discord.gg/upwP4mwJWa" alt="Discord"><img src="https://img.shields.io/discord/781987805974757426?label=discord&style=flat" /></a>

 - Matrix:
  <a href="https://matrix.to/#/#metacall:matrix.org" alt="Matrix"><img src="https://img.shields.io/matrix/metacall:matrix.org?label=matrix&style=flat" /></a>
