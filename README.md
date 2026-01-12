# document-form

## Summary

Short summary on functionality and used technologies.

[picture of the solution in action, if possible]

## Used SharePoint Framework Version

![version](https://img.shields.io/badge/version-1.21.1-green.svg)

## Applies to

- [SharePoint Framework](https://aka.ms/spfx)
- [Microsoft 365 tenant](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/set-up-your-developer-tenant)

> Get your own free development tenant by subscribing to [Microsoft 365 developer program](http://aka.ms/o365devprogram)

## Prerequisites

> Any special pre-requisites?

## Solution

| Solution    | Author(s)                                               |
| ----------- | ------------------------------------------------------- |
| folder name | Author details (name, company, twitter alias with link) |

## Version history

| Version | Date             | Comments        |
| ------- | ---------------- | --------------- |
| 1.1     | March 10, 2021   | Update comment  |
| 1.0     | January 29, 2021 | Initial release |

## Disclaimer

**THIS CODE IS PROVIDED _AS IS_ WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

---

## Minimal Path to Awesome

- Clone this repository
- Ensure that you are at the solution folder
- in the command-line run:
  - **npm install**
  - **gulp serve**

> Include any additional steps as needed.

## Features

Description of the extension that expands upon high-level summary above.

This extension illustrates the following concepts:

- topic 1
- topic 2
- topic 3

> Notice that better pictures and documentation will increase the sample usage and the value you are providing for others. Thanks for your submissions advance.

> Share your web part with others through Microsoft 365 Patterns and Practices program to get visibility and exposure. More details on the community, open-source projects and other activities from http://aka.ms/m365pnp.

## Commands
**run the sharepoint page**
gulp serve
gulp serve --nobrowser

**to clean**
gulp clean

**open edge to debug**

& "C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe" --remote-debugging-port=9222 --user-data-dir=C:\edge-debug


**link to site-local**
https://yfm71.sharepoint.com/sites/SharePointTutorial/_layouts/15/workbench.aspx


## 1.Creating the Document Libraries

The following three document libraries were created:

**Invoices**

**Purchase Orders**

**Quotes**

Steps to Create Each Library

Go to your SharePoint Site.

Click Site Contents (left navigation).

Click New → Document Library.

Enter the name:

Invoices

Purchase Orders

Quotes

Click Create.

Repeat the steps for each required library.

## 2. Adding Metadata Fields (Columns)

Each library requires custom metadata fields to store document information.
The fields were created inside Library Settings → Create Column.

Below are the fields created for each library, including their internal names (SharePoint auto-generates them based on spaces).

## 3. Folder Structure

No folders were created in the libraries.
Documents upload directly into the library root:

/sites/{your-sharpoint-sitename}/Invoices
/sites/{your-sharpoint-sitename}/Purchase Orders
/sites/{your-sharpoint-sitename}/Quotes

These URLs must match exactly in your SPFx component (e.g., sp.web.getFolderByServerRelativeUrl()).

**save webpart**
gulp bundle --ship
gulp package-solution --ship