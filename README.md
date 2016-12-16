![alt tag](http://www.martinerlic.com/parsebars/images/parsebars-banner.png)

# Parsebars.js
Parsebars.js provides a boilerplate MVC template for creating a web application using Handlebars.js and the Parse JavaScript SDK.

# Table of Contents  
* [0.0 Vision](#vision)
* [1.0 Team & Past Contributors](#team)
* [2.0 Installation & Documentation](#installation)
  * [2.1 Back4App Registration](#back4app)
  * [2.2 Application Configuration](#config)
* [3.0 Database Schema](#schema)
  * [3.1 Classes](#classes)
    * [3.1.3 User](#user)
* [4.0 Third-Party Libraries](#libs)
* [5.0 License](#license)

<hr>

<a name="vision"/>
## 0.0 Vision

I created Parsebars.js to save time for developers and entrepreneurs that don't want to spend hundreds of hours building a server before attaining product-market fit for their new web applications. Parsebars.js runs exclusively in the Cloud, making your back-end extremely easy to launch.

<hr>

<a name="team"/>
## 1.0 Team & Past Contributors

* <a href="https://github.com/santafebound/">Martin Erlic</a>

<hr>

<a name="installation"/>
## 2.0 Installation & Documentation

<a name="back4app"/>
### 2.1 Back4App Registration

In order to host your own version of Parsebars.js, you will most likely want to create an account at www.back4app.com. Given that Parsebars.js was originally developed with Parse, this means that Back4App is currently one of the few viable free hosting options out-of-box. Back4App is a Cloud BaaS (Back-End as a Service) solution that will host your database initially free of charge (that is, until your query requests reach a specified limit threshold per second). See https://www.back4app.com/pricing for additional pricing information at scale. I've found Back4App to be highly reliable so far, but if you are interested in hosting your own Parse Server elsewhere, there are tons of useful instructions and tutorials online. This article is a good place to start: https://medium.com/@timothy_whiting/setting-up-your-own-parse-server-568ee921333a

<a name="config"/>
## 2.2 Application Configuration

Simply open **blog.js** and change the configuration values to our own Application Id and Javascript Key, provided to you by Back4App (https://dashboard.back4app.com/ > Core Settings). This is where we connect to Parse. The configuration code will looks like this. The Application Id is the first string and the Javascript Key is the second:

```javascript
    // Connect to Parse API
    Parse.initialize(
        'x0rtG9s535J8ExWWJUXi8WO19C5xHcfDDef68Epm',
        'qX2sBdcEztbNQ9l8D0EZKdq1Suuopdrww310ti5x');
    Parse.serverURL = 'https://parseapi.back4app.com';
 ```

<a name="schema"/>
## 3.0 Database Schema

The complete database schema is documented below. Without configuring the following classes and attributes in your own Parse dashboard, downloading the source code probably won't be much help!

<a name="classes"/>
### 3.1 Classes

For each Class, I've excluded the auto-generated default Parse columns, i.e. objectId, createdAt, updatedAt, ACL, etc. due to redundancy.

* User

<hr>

<a name="user"/>
#### 3.1.1 User

| username (String) | name (String) | bio (String) | websiteLink (String) | profilePicture (File) | phoneNumber (String)
|--------------------------|-----------------|-------------------|--------------|----------------------|---------------|----------------|-------------------------------------|-----------------|-----------------------|----------------------|-------------------|----------------|

<hr>

<a name="libs"/>
## 4.0 Third Party Libraries

The following Third Party Libraries are used in Parsebars.js:

- **MaterialDrawer** by mikepenz: https://github.com/mikepenz/MaterialDrawer
- **Parse-SDK-JS** by ParsePlatform: https://github.com/ParsePlatform/Parse-SDK-JS

<hr>

<a name="license"/>
## 5.0 License

Copyright 2016 Hypercycle, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
