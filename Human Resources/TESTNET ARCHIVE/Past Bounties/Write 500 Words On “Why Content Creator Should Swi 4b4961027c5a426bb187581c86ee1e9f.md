# Write 500 Words On “Why Content Creator Should Switch To Atlas?” from gameover

### **From** [https://dao.joystream.org/#/bounty/preview/284](https://dao.joystream.org/#/bounty/preview/284)

**gameover**

[Joystream Governance App](https://dao.joystream.org/#/forum/thread/953)

[Why Content Creator Should Switch To Atlas](https://cugutalexei.medium.com/why-content-creator-should-switch-to-atlas-50c6650c2958)

# **Why Content Creator Should Switch To Atlas**

![](https://miro.medium.com/max/1400/1*N8izoEypEFploIapo1ACpQ.png)

[https://play.joystream.org/](https://play.joystream.org/)

The **Atlas** web app itself has a relatively conventional **web stack** for purpose, perhaps with the exception of relying on an external extension for key management, as is customary for web applications in **Web3.**

# **The mision of Joystream Atlas**

**Joystream** is a substrate-based protocol that aims to formalize a shared content platform. It is operated and governed by its users.

Today’s **web 2.0** is broken and corrupted. Content-creating platforms serve their owners and not their users.

We call for an arrangement where media platforms are accountable to the people they impact, which are primarily their users, be it as consumers, creatives, third-party developers, or workers.

It is the absence of such accountability which is the fundamental source of any particular problem at any particular time.

The **Joystream** it serve as a base template for others to build their own product offerings on top of Joystream. This innovation is uniquely unlocked by the open permissionless infrastructure of a blockchain system, and a forthcoming subsystem called the gateway system which provides a built in business-model for developers and entrepreneurs to build their offerings on top of the Joystream system.

Atlas is a content consumption and publication app for the Joystream platform. This document outlines conventions, tools and services make **Atlas** work.

# **Information for builders on WEB 3.0**

**Conventions**

**Some of the tools/ tech has been used**

- React
- Typescript
- GraphQL (+Relay-style pagination)
- ESLint, Prettier — for enforcing common code style
- Mirage JS — for client side mocking
- Emotion — for all the styling
- Apollo Client — for communications with GraphQL — based external services

**Repo structure**

- .github/ — GitHub stuff — currently PR checks actions
- docs/ — developer documentation
- public/ — static assets used to build the app
- scripts/ — some helper scripts for common tasks
- config-overrides.js — rules to modify CRA config with customize-cra
- src/ — the source code
- api/ — everything related to integrations with external services
- assets/ — assets to be used from withing source code — images/fonts/etc.
- components/ — components specific to Atlas
- config/ — everything related to config — route URLs, env variables, etc.
- mocking/ — client — side mocking
- shared/ — reusable code
- components — reusable components
- theme — all the theme stuff used by Atlas
- styles/ — app wide styles
- types/ — global Typescript related code
- utils/ — common utilities — e.g. for formatting dates etc.
- views/ — all the top-level views displayed by the router
- index.tsx — app entry-point
- App.tsx — React entry-point

**Shared folder**

Historically Atlas codebase was split between two packages — app and @joystream/components. Due to build process and developer experience issues it was decided to merge those packages into one until the separation is actually needed. Hence the shared/ directory in src/. This folder is what used to be @joystream/components and its intended to be application-agnostic. That means no Atlas-specific logic (like routing) should be put there, only atomic UI components.

**DevOps**

Currently GitHub actions and Netlify is used for all the DevOps needs. On every PR GitHub actions will be run to ensure the code follows the linting rules. Also for every PR, Netlify previews are generated so that it is easy to explore the updated app.

The deployed version of Atlas (at [https://play.joystream.org](https://play.joystream.org/)) is also hosted by Netlify. This one gets redeployed on every push/merge to master.

**Data sources**

Joystream is a decentralized platform so there cannot be a permissioned backend for all the Atlas querying/persistence needs. Instead, Atlas uses the following sources for its data.

Note that URLs for accessing all of the following services are provided to Atlas via build-time env variables (set in Netlify, accessed in src/config/urls.ts).

## **Main things of Atlas Joystream**

**Flexibility:** Flexible monetization of video content**Censorship resistance:** Censorship resistance and immunity to interventions by global entities**Equitable:** Equitable sharing of gains with creators and audience**Innovation:** Adequate platform innovation**Credibility:** Credibility with third-party developers