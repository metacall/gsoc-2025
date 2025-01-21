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

You can send the proposal link to any readable format you wish: Google Docs, plain text, in markdown... and preferably hosted online, accessible with a common browser **without downloading anything**.

We highly recommend you to ask for a review anytime to the community or mentor candidates before the contributor application deadline. It's much easier if you get feedback early than to wait for the last moment.
  

## Project Ideas

You can also propose your own.


### Linux Distributable

**Skills**: C/C++ Depependency Management, CMake, Guix, Guile, Bash, Docker, BuildKit, DevOps

**Expected size of the project**: Medium (175 hours)

**Difficulty rating**: Hard

**Description**:

At the moment of writing, Linux distributable is one of the best suited distributions that we have right now. But it is not completed and it has [some issues](https://github.com/metacall/distributable-linux/issues). The main objective of this project will be to solve those issues, either focused on the user experience or the development of other applications by means of using MetaCall Core embedded into them. Here's the list of the objectives:

 - Solve issues related to environment variables[[1]](https://github.com/metacall/distributable-linux/issues/5)[[2]](https://github.com/metacall/distributable-linux/issues/14), this will require generate an environment variable file based on `guix shell` and it will let us remove [the current approach used in the install script](https://github.com/metacall/install/blob/0f145d4ee5a60b58f7c48f043ed7d0b7d6268609/install.sh#L376).
 - Solve problems with [existing languages not working](https://github.com/metacall/distributable-linux/issues/1), and extend it in order to support more languages, including extending support for [additional features](https://github.com/metacall/distributable-linux/issues/11).
 - Improve support for embedders in order to have portable binaries that can be embedded easily into other languages like C/C++/Zig/Rust[[1]](https://github.com/metacall/distributable-linux/issues/15)[[2]](https://github.com/metacall/zig-example).
 - Adding [new architectures](https://www.gnu.org/savannah-checkouts/gnu/autoconf/manual/autoconf-2.70/html_node/Specifying-Target-Triplets.html#Specifying-Target-Triplets) to Linux with their respective tests (for this it is possible to use Docker multi-architecture for supporting those tests) and the install script support for those architectures.

**Expected outcomes**: A better and more stable version of MetaCall Linux Distributable which addresses the current errors and user experience problems.

**Possible mentors**: Vicente Eduardo Ferrer Garcia, Gil Arasa Verge

**Resources**:
 - Guix Shell: https://guix.gnu.org/manual/devel/en/html_node/Invoking-guix-shell.html
 - Guix Build System options: https://guix.gnu.org/manual/en/html_node/Additional-Build-Options.html
 - Docker Multi-Arch support: https://docs.docker.com/desktop/multi-arch/

### MetaCall Deploy Integrations

**Skills**: TypeScript, JavaScript

**Expected size of the project**: Medium (175 hours)

**Difficulty rating**: Medium

**Description**:

We have implemented support for [deployments through CLI](https://github.com/metacall/deploy) and now we require to integrate this CLI/Library into more environments in order to improve the development and adoption of MetaCall FaaS. For this there is a list of required tasks to do:
- Visual Studio Extension
- Github CI action
- OpenAPI integration

**Expected outcomes**: 

 - Create a Visual Studio Extension for one click deployment so you don't even need to use the command line for deploying MetaCall projects.
 - Create a GitHub action for integrating MetaCall deployments with your own CI if required.
 - Create a library for exporting the current MetaCall Inspect format into OpenAPI format, so it can be used easily on other projects.

**Possible mentors**: Jose Antonio Dominguez, Alexandre Gimenez Fernandez

**Resources**:
  - Visual Code Extension: https://code.visualstudio.com/api/get-started/your-first-extension
  - GitHub Action: https://docs.github.com/en/actions/creating-actions/publishing-actions-in-github-marketplace


## Find Us

The three chats are bridged by Matrix (messages sent from one, on the main room/channel, can be seen from all).

 - Telegram:
  <a href="https://t.me/joinchat/BMSVbBatp0Vi4s5l4VgUgg" alt="Telegram"><img src="https://img.shields.io/static/v1?label=metacall&message=join&color=blue&logo=telegram&style=flat" /></a>

 - Discord:
  <a href="https://discord.gg/upwP4mwJWa" alt="Discord"><img src="https://img.shields.io/discord/781987805974757426?label=discord&style=flat" /></a>

 - Matrix:
  <a href="https://matrix.to/#/#metacall:matrix.org" alt="Matrix"><img src="https://img.shields.io/matrix/metacall:matrix.org?label=matrix&style=flat" /></a>
