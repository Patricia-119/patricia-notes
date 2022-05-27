## ANALYSIS OF THE CAMERA SYSTEM
The main purpose of this analysis is to tell how the _camera system_ should be able to send the _video streams_ to the _Amazon Web Services_, how the _application programming interface_ (```API```) will be able to get access to credentials of the cameras from the _amazon web services_ and how the amazon web services will return those camera credentials to the application programming interface (```API```) inform of a **token** so that the front-end (```user```) can have access to the list of sites and cameras on the screen.
### CAMERAS AND AMAZON WEB SERVICES
- Each camera has its own certificate that it sends inform of a _key_  to the Amazon web services so that it can get the credentials.
### AMAZON WEB SERCIVES (AWS) AND APPLICATION PROGRAMMING INTERFACE (API)
- The appliaction programming interface (```API```) has _keys_ for each camera, the ```API``` then sends the _keys_ to the _Amazon Web Services_ so that the Amazon Web Services can return credentials in form of a **token**.

### FRONT-END AND APPLICATION PROGRAMMING INTERFACE (API)
- The Front-End sends an **empty request** to the ```API``` to check the _list of sites_ and the _list of cameras_ the user(```front-end```) has access to.
- The application programming interface (```API```) responds to the Front-End with the **token** that gives the credentials of the cameras and sites available, which will enable the user to have access to the video streams on the screen.