---
title: Getting Started with DeveelDB 2.0
---

{% include toc %}

Because the resources behind the project are very limited, we will not spend time making any preamble about the relational model and the SQL model in this context, assuming that those who are reading these pages are familiar with the concepts.

In these pages you will find the bare minimum descriptions on how to use **DeveelDB** in your applications and the differences and derivations from the known SQL standard and the behavior of the system in determined conditions.

## Installing The Library

Because at the moment **DeveelDB** comes simply as a library for .NET applications, to get started the user must reference the library from the typical distribution sources, such as _NuGet_ or compressed archives.

### Technical Requirements

**DeveelDB 2.0** is built on top of the .NET Framework v3.5 and is currently oriented only to Windows (a new version based on .NET Standard is currently under development, to target any Operating System).

[.NET Framework 3.5](https://www.microsoft.com/en-us/download/details.aspx?id=21)

### NuGet Installation

The most likely alternative to use the functionalities of **DeveelDB** is to reference the package deployed to the different sources we use for _Development_, _Stage_ and _Production_, and divided by intended architecture (x86, x64 and Any CPU)


  * A development process based on Continuous Integration builds the sources of the project every time a change is made and deploys the latest builds to the _Development_ source: use the packages from there with care, because could be unstable
  * If a build version reaches a sufficient level of code coverage and implements one (or more) of the features defined in the project milestones, the package is promoted to the _Stage_ source, marked as a pre-release: using this versions of the library is safer, but could include untested bugs
  * Once a pre-release version is tested sufficiently and reports no major bugs and implements the features planned by the project milestones, this is promoted to the _Production_ source and it is possible to be used in production applications


|     Phase     |  Source | Package Feed URL |
|---------------|---------|------------------|
| _Development_ | MyGet   | https://www.myget.org/F/deveeldb/api/v2  |
| _Stage_       | NuGet   | https://www.nuget.org/api/v2 |
| _Production_  | NuGet   | https://www.nuget.org/api/v2 |

Once referenced the sources in the NuGet.config ([read this guide hoow to make it](https://docs.microsoft.com/en-us/nuget/consume-packages/configuring-nuget-behavior)), it is possible to install one of the following packages

|   Package Name |  Architecture   |
|----------------|-----------------|
| deveeldb       | Any CPU         |
| deveeldb-x86   | Windows 32 Bit  |
| deveeldb-x64   | Windows 64 Bit  |


### Download Compressed Archives

The Continuous Deployment process used to develop **DeveelDB** creates a new set of archives of the library for each successful build and publish them together with the tag of the version on [GitHub](https://github.com/deveel/deveeldb).

It is possible to download the archives of the [latest](https://github.com/deveel/deveeldb/releases/latest) release or any previous release, and reference the library directly from the application.
These libraries are _absolutely_ equivalent to the ones deployed to other sources.

## Creating A Simple Database


### Store Data into the Database


### Querying the Database
