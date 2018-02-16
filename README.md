# `@flood/chrome`

> Flood Chrome brings the familiar power of traditional browser scripting tools with the proven performance of Flood to create an easy to use and maintainable performance testing tool.

> This project is currently in beta and APIs are subject to change.

# Quickstart

First, make sure you have installed the [latest version of NodeJS](https://nodejs.org) for your platform.

#### 1. Download Flood CLI

**On macOS:**

```bash
brew install flood-io/taps/flood
```

**On Linux:**

**On Windows:**

Coming soon.

#### 2. Initialize Project

The very first thing you should do is authenticate the `flood` tool with your Flood account. _If you don't have an account, you can sign up for free at [Flood](https://flood.io)._

```bash
# Login
flood login

# Initialize a new project
flood init my-flood-chrome-test

# Change to this directory and install dependencies
cd my-flood-chrome-test
yarn install
```

#### 3. Write and validate your script

Edit `test.ts` in your editor of choice, then validate it by running it on the Flood validation service:

```bash
flood verify test.ts
```

This will output a detailed list of steps and configuration options it has read from your script, then execute it within the Flood Chrome Environment.

#### 4. Run it on [Flood](https://flood.io)

# Why?

Over the years, countless customers have mentioned that getting started with Load Testing is a daunting task. That's why it's often left until the last minute before launch. At Flood, it's our mission to make Load Testing less daunting and accessible to everyone. We want to give developers and testers an easy way to ensure that whatever part of the system they're responsible for meets expectations for both functionality and performance.

# What can I do with it?

* Flood Chrome can be used to **put load on any web accessible application** and measure how it performs as load is ramped up,
* **Measure performance regressions** after deploys by integrating it with you CI/CD pipeline,
* Measure how your application's response time from different regions as experienced by your customers,
* Create **realistic load scenarios** which stress test your network infrastructure without developing a complex protocol level load test scripts.

# Documentation

* [Getting Started Guide]()
* [Flood Challenge Tutorial]()
* [Tooling Setup guide]()
* [API Documentation]()

# Reporting Issues
