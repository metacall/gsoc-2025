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

At the moment of writing, MetaCall has reached a stable point where showing the usage of the tooling itself is the most important. In this project we want to create a tutorial showing the full lifecycle of developing a complete application with MetaCall. The project has complete freedom for selecting language or framework for developing it, it will be interesting to use new technologies and also well known if possible. For achieving this, we will need to cover:

 1) Explain how to install MetaCall in Windows, Linux and MacOs.
 2) Develop a polyglot app with MetaCall, including Frontend, Backend and some services, for example using Python for doing something related to AI or math which cannot be done with NodeJS.
 3) Show how to develop the whole service locally with Deploy and FaaS tools.
 4) Deploy to both FaaS and show the final app in production.

All this process should be documented with markdown, also we will highly value if there are videos that we can upload to MetaCall's YouTube Channel. This should show the whole lifecycle of development and should be basic enough for people that does not know anything about MetaCall beforehand.

**Expected outcomes**: A complete tutorial written in markdown, with the code of the sample application developed, images and videos (or any other resource that can help to explain better the tutorial).

**Possible mentors**: Vicente Eduardo Ferrer Garcia, Jose Antonio Dominguez, Thomas Rory Gummerson, Alexandre Gimenez Fernandez, Raj Aryan

**Resources**:
 - MetaCall Install: https://github.com/metacall/install
 - MetaCall Deploy: https://github.com/metacall/deploy
 - MetaCall FaaS: https://github.com/metacall/faas
 - MetaCall Commercial FaaS: https://dashboard.metacall.io
 - MetaCall YouTube Channel: https://www.youtube.com/c/MetaCall

---

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

**Possible mentors**: Vicente Eduardo Ferrer Garcia, Fernando Vaño Garcia, Gil Arasa Verge, Param Siddharth

**Resources**:
 - MetaCall Rust Port Code: https://github.com/metacall/core/tree/5b592ac0e9a8e498e3e706623d0a788276f566e0/source/ports/rs_port
 - MetaSSR: https://github.com/metacall/metassr
 - Previous Work: https://github.com/metacall/core/pull/538
 - Previous Issues: https://github.com/metacall/core/pull/527
 - HList Pattern: https://github.com/plausiblelabs/hlist-rs

---

### Implement Core CI Support for C & Distributables

**Skills**: GitHub Actions, C/C++, CMake Build System, Homebrew, Guix, Windows Package Managers

**Expected size of the project**: Large (350 hours)

**Difficulty rating**: Hard

**Description**:

MetaCall Core has support for C by using `libffi`, `libclang` and `tcc`. This is widely tested in Linux on the `metacall/core` CI but lacks the implementation for MacOs and Windows. The objective of this project is to provide testing support in the Core for [Windows](https://github.com/metacall/core/pull/458) and [MacOs](https://github.com/metacall/core/pull/445) platforms, and once this is done we should implement this in the Distributables repositories. For this requirement, we will need to implement it in Guix (Linux), Homebrew (MacOs) and manually installing with Batch (Windows). It is not easy because the task requires knowledge of CMake build system and knowledge about different architectures. It willl be difficult but the final result of this is that we will be to bootstrap metacall itself with this. All the platforms will contain metacall.h and the metacall library and we can generate the API of metacall itself for multiples languages by using the C Loader. The explanation of this idea itself can be difficult because we are assuming some previous basic knowledge on MetaCall Core, but if you are intereseted you can ask in our chat groups for further explanation.

**Expected outcomes**: MacOs and Windows C Loader support in the Core and the distribution of the C Loader for Windows, MacOs and Linux. We should able to run things like: `metacall test.c`, once this is implemented.

**Possible mentors**: Vicente Eduardo Ferrer Garcia, Fernando Vaño Garcia, Gil Arasa Verge, Param Siddharth

**Resources**:
 - Previous Work: https://github.com/metacall/core/pull/458 & https://github.com/metacall/core/pull/445
 - Known Issues: https://github.com/metacall/core/issues/442
 - Guix `libclang`: https://git.savannah.gnu.org/cgit/guix.git/tree/gnu/packages/llvm.scm#n2160
 - Guix `tcc`: https://packages.guix.gnu.org/packages/tcc/
 - Guix `libffi`: https://packages.guix.gnu.org/packages/libffi

---

### Scala Port with GraalVM Comparison

**Skills**: Scala, GraalVM, Java, Language Interoperability

**Expected size of the project**: Small (90 hours)

**Difficulty rating**: Medium

**Description**:

The aim of this project is to showcase the capabilities of the existing MetaCall Scala Port by comparing its usage with GraalVM for polyglot programming. The project will involve creating a small example application that demonstrates calling other languages (e.g., Python or JavaScript) from Scala using MetaCall and from Java using GraalVM. The goal is to highlight how MetaCall simplifies polyglot development compared to GraalVM in terms of setup, ease of use, and developer experience.

Key aspects to be addressed:
 - Using the Scala Port: Leverage the existing MetaCall Scala Port to execute Python or JavaScript code directly from Scala.
 - GraalVM Comparison: Build the same example using GraalVM with Java as the primary language, integrating either Python or JavaScript.
 - Example Application: Create a small, practical example, such as:
   - Calling a Python function to process a dataset (e.g., summing numbers or sorting).
   - Executing JavaScript code for simple calculations (e.g., a factorial function).

Comparison Criteria:
 - Simplicity: Highlight the difference in setup and usage for developers.
 - Developer Performance (optional): Compare time or cost to set up and develop the example with each technology.
 - Documentation: Provide clear instructions and a side-by-side comparison of the two approaches, including code examples for both.

This project will focus on demonstrating how MetaCall provides a more ergonomic and straightforward approach to integrating multiple languages into a single project compared to GraalVM.

**Expected outcomes**:
 - A practical example showcasing MetaCall's Scala Port and its ability to execute scripts from other languages.
 - A comparison with GraalVM in terms of setup, ease of use, and developer experience.
 - Comprehensive documentation detailing the comparison, including code snippets, setup instructions, and insights into the pros and cons of each approach.

**Possible mentors**: Alexandre Gimenez Fernandez, Param Siddharth

**Resources**:
 - MetaCall Scala Port: https://github.com/metacall/scala-port
 - GraalVM Documentation: https://www.graalvm.org/docs/
 - Example of GraalVM Polyglot Programming: https://www.graalvm.org/reference-manual/polyglot/

---

### Zig Port Implementation

**Skills**: Zig, Systems Programming, C

**Expected size of the project**: Medium (175 hours)

**Difficulty rating**: Medium

**Description**:

The goal of this project is to create a new Port for MetaCall in Zig, allowing Zig programs to call and integrate other languages like JavaScript, Python, Ruby, and more. This project will require designing and implementing the Zig port from scratch, leveraging Zig's unique features such as comptime to simplify and improve the API's ergonomics for end users. This project will need to implement all supported types of MetaCall, also async APIs and different loading methodologies. Key aspects to be addressed:

 - Language Interoperability: Develop the necessary bindings and functionality to enable Zig to call functions from other supported MetaCall languages.
 - API Design: Use comptime to build a concise, ergonomic, and type-safe API that makes it easy for developers to integrate MetaCall into their Zig projects.
 - Build System: Ensure the port supports using an already installed version of MetaCall without requiring a full recompilation.
 - Testing and Documentation: Include extensive tests, documentation, and usage examples.
 - Memory Safety: Pay special attention to avoiding memory leaks and ensuring safe integration with Zig's memory model.

Additionally, the project should produce a basic tutorial or article showcasing the Zig port, providing examples of how it can be used to create polyglot applications.

**Expected outcomes**: 
 - A fully functional Zig port for MetaCall that supports calling multiple languages.
 - Comprehensive documentation, tests, and usage examples.
 - A tutorial or article demonstrating how developers can use the Zig port to build polyglot applications.

**Possible mentors**: Vicente Eduardo Ferrer Garcia, Fernando Vaño Garcia, Gil Arasa Verge

**Resources**:
 - Prior Work: https://github.com/metacall/core/tree/5b592ac0e9a8e498e3e706623d0a788276f566e0/source/ports/zig_port
 - MetaCall Core: https://github.com/metacall/core
 - Zig Documentation: https://ziglang.org/documentation/master/

---

### Rust Loader Update

**Skills**: Rust

**Expected size of the project**: Medium (175 hours)

**Difficulty rating**: Hard

**Description**:

Few years ago [Rust Loader was implemented](https://github.com/metacall/gsoc-2022?tab=readme-ov-file#rust-loader-support) but the code has became outdated due to nature of Rust Compiler unstable API / ABI. The idea of this project is to update to the latest version and add more tests and examples with tutorials. It will be also interesting to find a portable version, or at least to prevent depending on unstable Rust Compiler API (although I am not sure this is possible). Showing examples of mixing Rust and C++ would or script languages using Rust directly without need of using macros in the original Rust code would be also interesting, also [updating existing examples](https://github.com/metacall/python-rust-melody-example). Adding support for more types will be also interesting.

**Expected outcomes**: Implement a fully functional version of the Rust Loader with the latest compiler API. Extend the functionalities that are not implemented and provide more tests and examples with some tutorials about how to use it. Update existing tutorials using Rust Loader.

**Possible mentors**: Vicente Eduardo Ferrer Garcia, Fernando Vaño Garcia, Gil Arasa Verge

**Resources**:
 - MetaCall Rust Loader Code: https://github.com/metacall/core/tree/5b592ac0e9a8e498e3e706623d0a788276f566e0/source/loaders/rs_loader
 - Previous Work: https://github.com/metacall/core/issues/443

---


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

**Possible mentors**: Jose Antonio Dominguez, Thomas Rory Gummerson, Alexandre Gimenez Fernandez, Raj Aryan

**Resources**:
 - MetaCall Install: https://github.com/metacall/install
 - MetaCall Deploy: https://github.com/metacall/deploy
 - MetaCall FaaS: https://github.com/metacall/faas


---


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

**Possible mentors**: Jose Antonio Dominguez, Thomas Rory Gummerson, Alexandre Gimenez Fernandez, Raj Aryan

**Resources**:
 - MetaCall Install: https://github.com/metacall/install
 - MetaCall Deploy: https://github.com/metacall/deploy
 - MetaCall FaaS: https://github.com/metacall/faas

---

### Release Distributables from Core

**Skills**: DevOps, GitHub Actions, C/C++, Build Systems, Bash, Batch

**Expected size of the project**: Medium (175 hours)

**Difficulty rating**: Medium

**Description**:

Last year we connected the [Distributables with the Core](https://github.com/metacall/gsoc-2024/?tab=readme-ov-file#connect-core-ci-with-distributables) but we plan to extend this further and allow to automatically test master and new versions for each platform. So every time we release a new version or we push to master, it gets tested in the latest version or in the tagged version, and it automatically generates a commit updating to the new version if everything worked. This will act as an extension to the previous project, providing the full automatic lifecycle of development and releases for all platforms. It is also expected to make it work with the install scripts CI, so we can test it from core to the install repository.

**Expected outcomes**: Full lifecycle working and validated for MacOS, Windows, Linux. Tested for master and tagging versions and also including the install.

**Possible mentors**: Raj Aryan, Harsh Bardhan Mishra, Vicente Eduardo Ferrer Garcia, Gil Arasa Verge, Ashish Kumar

**Resources**:
 - MetaCall Core Windows Dispatch: https://github.com/metacall/core/blob/5b592ac0e9a8e498e3e706623d0a788276f566e0/.github/workflows/windows-test.yml#L68
 - MetaCall Core MacOS Dispatch: https://github.com/metacall/core/blob/5b592ac0e9a8e498e3e706623d0a788276f566e0/.github/workflows/macos-test.yml#L100
 - MetaCall Core Linux Dispatch: https://github.com/metacall/core/blob/5b592ac0e9a8e498e3e706623d0a788276f566e0/.github/workflows/linux-test.yml#L70
 - MetaCall Distributable Windows: https://github.com/metacall/distributable-windows
 - MetaCall Distributable MacOS: https://github.com/metacall/distributable-macos
 - MetaCall Distributable Linux: https://github.com/metacall/distributable-linux

---

### Connect Examples with MetaCall Test Center

**Skills**: Python, DevOps, GitHub Actions, Yaml

**Expected size of the project**: Medium (175 hours)

**Difficulty rating**: Medium

**Description**:

Last year we implemented the [MetaCall Testing Center](https://github.com/metacall/testing-center) based on [this idea from GSoC](https://github.com/metacall/gsoc-2024?tab=readme-ov-file#metacall-examples-ci). This project aims to make this fully functional and work with existing examples and versions. The `metacall/install`, `metacall/deploy` and `metacall/faas` repositories should be connected with this one, and also the examples. On any modification of those repositories or the examples themselves, the CI of this repo should be triggered and it must test all the examples with the newer versions so we can verify all examples work and also we do integration testing for all the tools. By this way we can ensure that we keep up to date all the tools and if we break something, we can monitor that easily.

**Expected outcomes**: All the existing examples must work with the testing center, and this CI must be connected with the deploy, faas and install repos. The new examples must be added by using yaml and we must validate them. They also must work on Windows, Linux and MacOS. All the remaining features which are not implemented must be implemented to fullfill the requirements described.

**Possible mentors**: Raj Aryan, Harsh Bardhan Mishra, Vicente Eduardo Ferrer Garcia, Gil Arasa Verge, Ashish Kumar

**Resources**:
 - MetaCall Examples: https://github.com/metacall/examples
 - MetaCall Install: https://github.com/metacall/install
 - MetaCall Deploy: https://github.com/metacall/deploy
 - MetaCall FaaS: https://github.com/metacall/faas

---

## Find Us

The three chats are bridged by Matrix (messages sent from one, on the main room/channel, can be seen from all).

 - Telegram:
  <a href="https://t.me/joinchat/BMSVbBatp0Vi4s5l4VgUgg" alt="Telegram"><img src="https://img.shields.io/static/v1?label=metacall&message=join&color=blue&logo=telegram&style=flat" /></a>

 - Discord:
  <a href="https://discord.gg/upwP4mwJWa" alt="Discord"><img src="https://img.shields.io/discord/781987805974757426?label=discord&style=flat" /></a>

 - Matrix:
  <a href="https://matrix.to/#/#metacall:matrix.org" alt="Matrix"><img src="https://img.shields.io/matrix/metacall:matrix.org?label=matrix&style=flat" /></a>
