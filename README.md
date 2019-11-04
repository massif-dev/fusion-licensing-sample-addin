# Massif Licensing Tools for Python addins for Autodesk Fusion 360

A simple addin sample for Autodesk Fusion 360, that demonstrates the use of the Massif Licensing SDK for Python, to restrict the use of assets hosted on the **Massif Licensing Platform** to users that have valid licenses or subscriptions to use the asset/s.
Please note that this SDK should not be used for publishing your addins. To publish your apps on the store, we need to run them through our build process which secures your code. Once you have your
addin running and tested, you can submit it to Massif to have it secured, and published on the platform.

Please note: The actual addin code in this sample is written by Autodesk, as sample code.

---

### Prerequisites:

* **Autodesk Fusion 360** - For testing and debugging your addin. Available at http://fusion360.autodesk.com/
* **CPS Desktop App** must be installed, and user logged in, to be able to provide the asset information.
* Port 3002 must be open to allow the licensing tools to access the **CPS Desktop App** local web server. 

---

### What you get:

* **Addin boilerplate** - Sample python project, for an addin for Fusion 360 that should you get up and running quickly with a simple toolbar button that performs a license check.   

---

### How to use this:

0. Request developer access from Massif (info@massif.dev)
1. Clone this github repo to your machine. (optional)
2. Replace or modify SketchChecker_Python.py with your addin code.
3. Create a private bitbucket repo (github and gitlab will be supported in future.)
4. Create a branch in this format ```client/{name-provided-by-massif}/live```
5. Invite "bot@massif.dev" as a read-only user to the repo.
6. Commit and Push your Python addin to the branch created in 4.
7. Sign in to https://massif.dev/admin
8. Go to the developer tab, and enter your bitbucket repo details, then save.
9. (Product creation workflow will go here.)
9. Notify Massif that your addin is ready for delivery.

---

## License

See `EULA.html` in the repo.

Copyright 2019 - **Massif Limited.**
