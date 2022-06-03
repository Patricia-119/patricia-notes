### ENABLING AUDIO ON FREE PRIVATE BRANCH EXCHANGE (PBX)
- To enable audio, we created the two extensions which were used to establish communication between the two PBXs. 
- After creating the extensions we got the extension's credentials and registered the extentions on zoiper.

**NOTE**
- To resgister the Sip credentials (extensions created on free pbx).
- Go to ```seetings``` on zoiper >```accounts```, then it will load, for example below;

**SIP**
~~~~
 201@13.244.123.242
 ~~~~
- click on it ```201@13.244.123.242``` then  a form of *SIP CREDENTIALS* will appear as follows;
- Domain 
    - This is where you enter your ip address generated from the free PBx instance created automatically using the script.
- Username 
    - This where you enter the username  created in the extension (free pbx) which is always supposed to be a number.
- Password
    - this is where you enter the ```secrete``` created when creating the extensions in the free PBX.
- After that press ```register``` on the right top of the appliaction or softphone 
(zoiper).


### ENABLE AUDIO ON A LAPTOP OR DESKTOP ON ZOIPER
- Click no ```seetings```>```advanced settings```> then on the right side of the application a form will appear with three different parts will appear of will be;
1. Global Stun
    - below it the is a small squared box and if it is ```ticked``` untick it.
2. TLS Options 
    - which is professional so unless you want to use advanced features you can pay for it and use it but if not ignore it. In our case skipp it.
3. Network
    - This is where our main focus is where we have the form that contains the *sip options* and on the right side of each option there are small squared boxes tick in them or click in them all to enable *Sip networks settings* as all the extensions and trunks were created using the sip settings.
- Then call the registered extensions to see if it returns audio or sound, otherwise it should work.
### ENABLE AUDIO ON A MOBILE PHONE (SMART PHONE) USING ZOIPER
- Click no ```seetings```> Select ```accounts```> then scroll down to >```Network settings``` then try enabling or disabling RPORT for signaling and if the issue still persists open the network settings again and activate or diactivate **STUN** save the changes and make the test call.
- if the issue still persists again try to change the transport type for the account created as follows;

- Go on ```settings``` again > select your account on ```accounts```, scroll down to to ```network settings```  and change the transport type to *UDP*, *TLS* OR *TCP* select according to the providers recommendation but in our case select *TCP*. Once this is done save changes and test a  call.
### CREATING INBOUND AND OUTBOUND ROUTES.
- To create inbound route click on ```connectivity```>```inbound route``` once clicked a form will appear and enter the credentials.
- To create outbound route click on ```connectivity```>```outbound route``` once clicked a form will appear and enter the credentials and select the anny of the credentials created ealier on and ```apply config```.
### CONNECTING FREE PBXS ON A DIFFERENT DOMAIN TO ESTABLISH A CALL (PEER TO PEER)
- Create a *sip-trunk* on the two differant domains of the free pbx which will be used to establish communication between the two PBXs.
- when connecting trunks the other freePBX account in the out bound routes needs to be on receive and the other on send. 
- After creating the trunks, exchange each others IP addresses or the domain and the port number of each pbx and eastablish the communication.
- Then call each other using the resgistered extensions or registered accounts on zoiper. 
