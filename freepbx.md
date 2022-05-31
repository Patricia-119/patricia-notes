# DEPLOYING FREEPBX MANUALLY
- Login to aws console
- Then click on aws market to select a FREEPBX 
- After selecting the ```freepbx ami```, click on launch instance.
- Click on create key pair and give the pair a name.
- Then finally launch instance.

- After creating an instance, you open the created instance.
- Clikc on the public address to log into freepbx.

### Login to freepbx.
- After login, you do the following.
    - Click on applications to add users
    - Click on extensions(users)
    - Click on quick extensions(uses system settings)
    - Click on submit and apply config.
    ##   TESTING AND REGISTERING EXTENTIONS ON ZOIPER
- Downloaded zoiper and registered the extensions on zoiper with credentials such as user name, password and domain.
- After that was done , we called the extension created and they rang without audio.
### CREATING INBOUND AND OUTBOUND ROUTES.
- To create inbound route click on ```connectivity```>```inbound route``` once clicked a form will appear and enter the credentials.
- To create outbound route click on ```connectivity```>```outbound route``` once clicked a form will appear and enter the credentials and select the anny of the credentials created ealier on and ```apply config```.
- To enable audio, we created the sip-trunk which was used to establish communication between the two PBXs. 
- After creating the  trunk we got the trunk's credentials and used it in the second pbx as the second PBXs sip-trunk.
- Then created the inbound and outbound routes for making the calls between the pbxs using the registered extensions. Additional information includes the following; trunk name, dial pattern and the inbound route.
- Clicked on ```settings``` > ```asterisk sip settings``` ,then click on ```detect network settings under NAT settings``` then click ```submit``` and ```apply config```.
- Then click ```admin``` >```asterisk CLI```and a form appeared where we ```entered core restart now``` as a command and clicked on the ```send``` button. Wait for 10-20 minutes for it to execute the command and refresh the page.

