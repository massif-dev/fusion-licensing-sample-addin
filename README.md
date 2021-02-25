# Massif Licensing Tools for Python addins for Autodesk Fusion 360

A simple addin sample for Autodesk Fusion 360, that demonstrates the use of the Massif Licensing SDK for Python, to restrict the use of assets hosted on the **Massif Licensing Platform** to users that have valid licenses or subscriptions to use the product/s.
Please note that this SDK should not be used for publishing your addins. To publish your apps on the store, we need to run them through our build process which secures your code. Once you have your addin running and tested, you can submit it to Massif to have it secured, and published on the platform.

Please note: The actual addin code in this sample is written by Autodesk, as sample code.

---

### Prerequisites:

* **Autodesk Fusion 360** - For testing and debugging your addin. Available at https://fusion360.autodesk.com/
* **Massif Desktop App** must be installed, and user logged in, to be able to provide the asset information.
* Port 30011 must be open to allow the licensing tools to access the **Massif Desktop App** local web server. 

---

### What you get:

* **Addin boilerplate** - Sample python project, for an addin for Fusion 360 that should you get up and running quickly with a simple toolbar button that performs a license check.   

---

### How to use this:

1. Request developer access from Massif (email info@massif.dev for more information).
2. Copy these files onto your machine.
3. Replace or modify `SketchChecker_Python.py` with your addin code and rename the file. Make sure it has the following code at the top, wrapped in `"""` and populate with correct information. You must use semantic versioning formatted as `v<major>.<minor>.<patch?`, e.g. `v1.2.3`.
~~~
"""/*
  ^^massifInfo: {
    "vendor": "Williams Wally Workshop",
    "version": "v1.0.0",
    "release-notes": "*Initial release"
  }^^
*/"""
~~~
4. Create a private Bitbucket repo (GitHub and GitLab will be supported in the near future), and upload these files
5. Create a branch in this format ```client/{name-provided-by-massif}/live```
6. Invite "bot@massif.dev" as a read-only user to your repo.
7. Create a webhook in your repo, and configure it to use this URL: https://massif.dev/api/v2/bb/updates?type=bitbucket on repository push.
8. Commit and Push your Python addin to the branch created in Step 5.
9. Go to the developer tab, and enter your bitbucket repo details, then save.
10. Sign in to https://massif.dev/admin, navigate to the Products page and then click 'Add New Product' to complete the Product Registration workflow. Note: make sure you enter the correct Git branch and file name otherwise your Addin will not work.
11. You're all done!

---

### Known issues:
- Icons must be in a top level "resources" directory. Sub-directories are not currently supported

---

## License

See `EULA.html` in the repo.

Copyright 2021 - **Massif Limited.**
