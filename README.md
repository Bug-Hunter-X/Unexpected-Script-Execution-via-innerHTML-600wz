# Unexpected Script Execution in HTML using innerHTML

This repository demonstrates an uncommon HTML bug related to the use of `innerHTML`.  Improperly using `innerHTML` with user-supplied data can introduce cross-site scripting (XSS) vulnerabilities.  The `bug.html` file showcases the problem, while `solution.html` provides a safer alternative.

## Problem

The `bug.html` file contains a `<div>` element and JavaScript code that uses `innerHTML` to modify its content.  The issue is that a malicious script is included within the string assigned to `innerHTML`, resulting in unexpected script execution. This is a serious security risk if user inputs are used within `innerHTML`.

## Solution

The `solution.html` file demonstrates a safer way to update the HTML content.  Instead of directly using `innerHTML`, it utilizes `textContent` or DOM manipulation methods to add or change elements. This avoids the possibility of inadvertently executing malicious code.

Always sanitize user input before inserting it into the DOM to prevent XSS attacks.