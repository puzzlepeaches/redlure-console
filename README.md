# The redlure Distributed Phishing Framework
redlure is a phishing framework designed to advance pentest and red team phishing. It could also be utilized by blue teams looking to train employees through running realistic phishing scenarios. 

redlure's distributed architecture allows for multiple campaigns to be run on different ports and/or servers, while results are aggregated in a singular interface. This allows you to generate phishing templates, target lists, start/stop campaigns, change domains, change ports and generate LetsEncrypt certs on multiple workers all from one interface. 

## redlure-console
Use the [Wiki](https://github.com/redlure/redlure-console/wiki) to get started with the redlure-console.

## Sponsors
[![Schneider Downs](assets/schneiderdowns.png)](https://schneiderdowns.com)

## Core features
* Manage phishing campaigns running in parallel across multiple servers, ports and domains
* Chain webpage templates together for multi-step phishing (e.g. Office365, Gmail)
* Workspaces to manage results and templates for each engagement
* Partial database encryption (sensitive database columns only)
* Generate LetsEncrypt certs remotely (other certificates can be manually specified)
* Manage payload delivery via automatic downloads or links and buttons
* Role-based authentication

## redlure Ecosystem
redlure is comprised of three components:
1. redlure-console - Centralized API the operator interacts with. Stores templates/results and tracks campaigns. Manages your redlure-workers. Written in Python using Flask.
2. [redlure-worker](https://github.com/redlure/redlure-worker) - Skeletal API that manages the webserver for phishing campaigns. Multiple of these can and should be managed from a single console. Written in Python using Flask.
3. [redlure-client](https://github.com/redlure/redlure-client) - Web interface for interacting with the console API. Written with the Angular 7 framework (Typescript and HTML)

**Basic diagram:**
![](assets/diagram.png)






