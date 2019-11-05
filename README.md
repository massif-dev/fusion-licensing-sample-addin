# Massif Licensing Tools for Python addins for Autodesk Fusion 360

A simple addin sample for Autodesk Fusion 360, that demonstrates the use of the Massif Licensing SDK for Python, to restrict the use of assets hosted on the **Massif Licensing Platform** to users that have valid licenses or subscriptions to use the asset/s.
Please note that this SDK should not be used for publishing your addins. To publish your apps on the store, we need to run them through our build process which secures your code. Once you have your
addin running and tested, you can submit it to Massif to have it secured, and published on the platform.

Please note: The actual addin code in this sample is written by Autodesk, as sample code.

---

### Prerequisites:

* **Autodesk Fusion 360** - For testing and debugging your addin. Available at http://fusion360.autodesk.com/
* **CPS Desktop App** must be installed, and user logged in, to be able to provide the asset information.
* Port 30011 must be open to allow the licensing tools to access the **CPS Desktop App** local web server. 

---

### What you get:

* **Addin boilerplate** - Sample python project, for an addin for Fusion 360 that should you get up and running quickly with a simple toolbar button that performs a license check.   

---

### How to use this:

0. Request developer access from Massif (info@massif.dev)
1. Clone this github repo to your machine.
2. Replace or modify SketchChecker_Python.py with your addin code. Make sure it has the following code at the top, wrapped in `"""` and populate with correct information. You must use a "v" followed by a semantic versioning formatted (major.minor.patch) version number. e.g. `v1.2.3`
~~~
"""/*
  ^^massifInfo: {
    "vendor": "Williams Wally Workshop",
    "version": "v1.0.0",
    "release-notes": "*Initial release"
  }^^
*/"""
~~~
3. Add your product code (supplied to you by Massif) as shown below:
~~~
#Globals
handlers = []
product_code = "FusionTestAddin" # <<<<<<<<<<< Your product code (supplied by Massif) goes here
    
def getProductCode():
    return product_code # Make sure you leave this function as is.
~~~

4. Check that your `Stop()` method doesn't have a "Context" argument.
5. Create a private bitbucket repo (github and gitlab will be supported in future.)
6. Create a branch in this format ```client/{name-provided-by-massif}/live```
7. Invite "bot@massif.dev" as a read-only user to the repo.
8. Create a webhook in your repo, and configure it to use this URL: https://cps.cadpro.co.nz/api/v1/bb/updates?type=bitbucket on repository push.
9. Commit and Push your Python addin to the branch created in 4.
10.  Sign in to https://massif.dev/admin
11.  Go to the developer tab, and enter your bitbucket repo details, then save.
12.  (Product creation workflow will go here.)
13.  Notify Massif that your addin is ready for delivery.

---

### Known issues:
- Icons must be in a top level "resources" directory. Sub-directories are not currently supported
- Only 1 python addin for Fusion 360 can be licensed and run at a time, on any single machine.

---

## License

See `EULA.html` in the repo.

Copyright 2019 - **Massif Limited.**
