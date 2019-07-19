---
title: "Upload Test Results using Command Line" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/project-management-import-cli.html 
redirect_from:
    - "/display/KA/From+Command+Line/"
    - "/display/KA/From%20Command%20Line/"
    - "/x/FhbR/"
    - "/katalon-analytics/docs/project-management-import-cli/"
description: How to import test results using CLI
---

Katalon Analytics supports various types of test automation report generated by Katalon Studio and Katalon Recorder, and in JUnit formats.

1. Download [Reports Uploader](https://github.com/katalon-studio/report-uploader/releases) and install [Java JRE](https://www.java.com/en/download/manual.jsp) and [Java JDK](https://www.oracle.com/technetwork/java/javase/downloads/index.html).

2. Get the path to your Katalon Report folders, e.g. `C:\Users\alex\Katalon Studio\Web Sample\Reports\Test Suite\20190523_143946`.

3. Start Command Prompt and use the following command to upload Katalon Report:

```
java -jar katalon-report-uploader-0.0.5.jar --projectId=3 --path="d:\katalon-reports" --email=admin@mail.me --password=admin --type=katalon
```
* `projectId`: your project ID in Katalon Analytics.
* `path`: a local path of Katalon Studio Reports folder identified in step 2.
* `email`: the email registered for your Katalon account.
* `password`: the password used for signing in Katalon Analytics or an API Key.
* `type`: one of the values including "katalon", "JUnit", or "katalon_recorder".