# Learn Node.js by building a backend framework

> There’s going to be 0 dependencies for our backend framework, as well as our logging library. Everything will be done using vanilla Node.js, the hard-way (the best way to learn).

> This is still in a very early stage. It consists of almost an insignificant portion of the total content which it intends to cover. There will also be an pdf version of this to download, as well as a website for the documentation.

I've found that one of the best ways to get a handle on a new concept is to start from scratch. Begin with nothing, and build it up yourself. This approach lets you not only learn how it works, but also understand _why_ it works that way.

This isn't any normal Node.js tutorial or guide. It's a detailed walkthrough, and a code along experience that shows you how to create a backend framework from the ground up while getting a solid grasp of Node.js's inner workings and it’s standard library.

In this guide, we will not only build a web framework, but also focus on designing a powerful and optimized end product that is ready for use in production applications (somewhat). Our goal is to create a modular backend framework that can be easily extended with new features as needed.

We will cover topics like error handling, security, and testing to ensure that our framework is reliable and secure. We will explore different approaches to modularity and demonstrate how to create reusable components that can be shared across multiple projects. By the end of this guide, you will have a solid understanding of Node.js and it’s tough parts.

I highly recommend coding along with this guide rather than just reading it.

[![Read Next](/assets/imgs/next.png)](/chapters/ch01-what-is-a-web-server-anyway.md)

# Table of contents

-   [What the hell is a web server any way?](/chapters/ch01-what-is-a-web-server-anyway.md)
    -   [Parts of a Web Server](/chapters/ch01-what-is-a-web-server-anyway.md#parts-of-a-web-server)
    -   [Navigating the World of Protocols: A Quick Overview](/chapters/ch01-what-is-a-web-server-anyway.md#navigating-the-world-of-protocols-a-quick-overview)
    -   [The Relationship Between HTTP and TCP](/chapters/ch01-what-is-a-web-server-anyway.md#the-relationship-between-http-and-tcp-ensuring-reliable-web-communication)
        -   [Data Integrity and Order](/chapters/ch01-what-is-a-web-server-anyway.md#1-data-integrity-and-order)
        -   [Acknowledgment Mechanism](/chapters/ch01-what-is-a-web-server-anyway.md#2-acknowledgment-mechanism)
        -   [Complex Interactions](/chapters/ch01-what-is-a-web-server-anyway.md#3-complex-interactions)
        -   [Transmission Overhead](/chapters/ch01-what-is-a-web-server-anyway.md#4-transmission-overhead)
    -   [How Web Servers Respond to Your Requests](/chapters/ch01-what-is-a-web-server-anyway.md#asking-and-getting-how-web-servers-respond-to-your-requests)
        -   [The Request](/chapters/ch01-what-is-a-web-server-anyway.md#the-request)
            -   [Your Request](/chapters/ch01-what-is-a-web-server-anyway.md#1-your-request)
            -   [Finding the Address](/chapters/ch01-what-is-a-web-server-anyway.md#2-finding-the-address)
            -   [Resolving the Address](/chapters/ch01-what-is-a-web-server-anyway.md#3-resolving-the-address)
        -   [The Response](/chapters/ch01-what-is-a-web-server-anyway.md#the-response)
            -   [Return Address](/chapters/ch01-what-is-a-web-server-anyway.md#1-return-address)
            -   [Sending the Request](/chapters/ch01-what-is-a-web-server-anyway.md#2-sending-the-request)
            -   [Preparing the Content](/chapters/ch01-what-is-a-web-server-anyway.md#3-preparing-the-content)
            -   [Sending the Response](/chapters/ch01-what-is-a-web-server-anyway.md#4-sending-the-response)
            -   [Enjoying the Content](/chapters/ch01-what-is-a-web-server-anyway.md#5-enjoying-the-content)
-   [Your first web server with node.js](/chapters/ch02-your-first-nodejs-server.md)
    -   [What exactly is node or nodejs?](/chapters/ch02-your-first-nodejs-server.md#what-exactly-is-node-or-nodejs)
    -   [Your first node.js program](/chapters/ch02-your-first-nodejs-server.md#your-first-nodejs-program)
    -   [How does console.log() work in Node.js?](/chapters/ch02-your-first-nodejs-server.md#how-does-consolelog-work-in-nodejs)
    -   [The process Object](/chapters/ch02-your-first-nodejs-server.md#the-process-object)
    -   [The stdout property of the process object](/chapters/ch02-your-first-nodejs-server.md#the-stdout-property-of-the-process-object)
-   [Working with files](/chapters/ch03-working-with-files.md)
    -   [What will the logging library do](/chapters/ch03-working-with-files.md#what-will-the-logging-library-do)
    -   [How do you work with files anyway?](/chapters/ch03-working-with-files.md#how-do-you-work-with-files-anyway)
    -   [Let's get back to files](/chapters/ch03-working-with-files.md#lets-get-back-to-files)
    -   [A little more about file descriptors](/chapters/ch03-working-with-files.md#a-little-more-about-file-descriptors)
    -   [Creating our first file](/chapters/ch03-working-with-files.md#creating-our-first-file)
        -   [`path` argument](/chapters/ch03-working-with-files.md#path-argument)
        -   [`flag` argument](/chapters/ch03-working-with-files.md#flag-argument)
        -   [`mode` argument](/chapters/ch03-working-with-files.md#mode-argument)
    -   [Reading from a file](/chapters/ch03-working-with-files.md#reading-from-a-file)
    -   [Reading the json file](/chapters/ch03-working-with-files.md#reading-the-json-file)
    -   [Buffers](/chapters/ch03-working-with-files.md#buffers)
    -   [Parsing the json file](/chapters/ch03-working-with-files.md#parsing-the-json-file)
-   [`logtar` - Our Own logging library](/chapters/ch04-logtar-our-logging-library.md)
    -   [Initializing a new project](/chapters/ch04-logtar-our-logging-library.md#initialising-a-new-project)
    -   [A little about `SemVer`](/chapters/ch04-logtar-our-logging-library.md#a-little-about-semver)
    -   [Creating a LogLevel class](/chapters/ch04-logtar-our-logging-library.md#creating-a-loglevel-class)
    -   [The Logger class](/chapters/ch04-logtar-our-logging-library.md#the-logger-class)
    -   [Encapsulation with private fields](/chapters/ch04-logtar-our-logging-library.md#encapsulation-with-private-fields)
    -   [The `LogConfig` class](/chapters/ch04-logtar-our-logging-library.md#the-logconfig-class)
    -   [Design Patterns](/chapters/ch04-logtar-our-logging-library.md#design-patterns)
        -   [The `Builder` pattern](/chapters/ch04-logtar-our-logging-library.md#the-builder-pattern)
        -   [Using the `Builder` pattern with the `LogConfig` class](/chapters/ch04-logtar-our-logging-library.md#using-builder-pattern-with-the-logconfig-class)
    -   [`jsdoc` comments](/chapters/ch04-logtar-our-logging-library.md#jsdoc-comments)
    -  [The `RollingConfig` class](/chapters/ch04-logtar-our-logging-library.md#the-rollingconfig-class)
        - [The `RollingSizeOptions` class](/chapters/ch04-logtar-our-logging-library.md#the-rollingsizeoptions-class)
        - [The `RollingTimeOptions` class](/chapters/ch04-logtar-our-logging-library.md#the-rollingtimeoptions-class)
    -  [Finishing up the `RollingConfig` class](/chapters/ch04-logtar-our-logging-library.md#finishing-up-the-rollingconfig-class)
    - [Let's recap](/chapters/ch04-logtar-our-logging-library.md#lets-recap) 
    - [Adding more useful methods in the `LogConfig` class](/chapters/ch04-logtar-our-logging-library.md#adding-more-useful-methods-in-the-logconfig-class)
    - [Why `readFileSync`?](/chapters/ch04-logtar-our-logging-library.md#why-readfilesync)
-   [Refactoring the code](/chapters/ch04.1-refactoring-the-code.md)
    - [The need for refactoring](/chapters/ch04.1-refactoring-the-code.md#the-need-for-refactoring)
    - [Creating Separate Files](/chapters/ch04.1-refactoring-the-code.md#creating-separate-files)
        - [Explanation](/chapters/ch04.1-refactoring-the-code.md#explanation)
        - [The `index.js` file](/chapters/ch04.1-refactoring-the-code.md#the-indexjs-file)
        - [The `lib/logtar.js` file](/chapters/ch04.1-refactoring-the-code.md#the-liblogtarjs-file)
        - [The `lib/logger.js` file](/chapters/ch04.1-refactoring-the-code.md#the-libloggerjs-file)
        - [The `lib/config/log-config.js` file](/chapters/ch04.1-refactoring-the-code.md#the-libconfiglog-configjs-file)
        - [The `lib/config/rolling-config.js` file](/chapters/ch04.1-refactoring-the-code.md#the-libconfigrolling-configjs-file)
        - [The `lib/utils/log-level.js` file](/chapters/ch04.1-refactoring-the-code.md#the-libutilslog-leveljs-file)
        - [The `lib/utils/rolling-options.js` class](/chapters/ch04.1-refactoring-the-code.md#the-libutilsrolling-optionsjs-class)
- [Writing Logs](/chapters/ch04.2-writing-logs.md)
    - [Re-using the file handle](/chapters/ch04.2-writing-logs.md#re-using-the-file-handle)
    - [Log rotation](/chapters/ch04.2-writing-logs.md#2-log-rotation)
    - [Asynchronous logging](/chapters/ch04.2-writing-logs.md#3-asynchronous-logging)
    - [Getting caller information](/chapters/ch04.2-writing-logs.md#4-getting-caller-information-module-and-line-number)
    - [Testing our current API](/chapters/ch04.2-writing-logs.md#testing-our-current-api)
    - [Implementing logging methods](/chapters/ch04.2-writing-logs.md#implementing-logging-methods)
        - [DRY (Don't Repeat Yourself)](/chapters/ch04.2-writing-logs.md#dry-dont-repeat-yourself)
        - [The `log` method](/chapters/ch04.2-writing-logs.md#the-log-method)
        - [Considering the `log_level` member variable](/chapters/ch04.2-writing-logs.md#considering-the-log_level-member-variable)
    - [Writing to a file](/chapters/ch04.2-writing-logs.md#writing-to-a-file)
        - [A small primer on Regular Expressions](/chapters/ch04.2-writing-logs.md#a-small-primer-on-regular-expressions)
        - [Testing the log file creation](/chapters/ch04.2-writing-logs.md#testing-the-log-file-creation)
        - [Another gotcha](/chapters/ch04.2-writing-logs.md#another-gotcha)
        - [Logs directory configuration](/chapters/ch04.2-writing-logs.md#logs-directory-configuration)
        - [Our first script](/chapters/ch04.2-writing-logs.md#our-first-script)
    - [The `require` object](/chapters/ch04.2-writing-logs.md#the-require-object)
    - [Adding a new helper to create log directory](/chapters/ch04.2-writing-logs.md#adding-a-new-helper-to-create-log-directory)
    - [Updating the `init` method](/chapters/ch04.2-writing-logs.md#updating-the-init-method)
    - [Completing the `log` method](/chapters/ch04.2-writing-logs.md#completing-the-log-method)

![](https://uddrapi.com/api/img?page=readme)