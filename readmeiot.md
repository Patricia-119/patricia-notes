# AWS IOT CAMERA SYSTEM
The project is about aws iot camera system,  the cameras will be sending streams to aws and aws will do **NVR** things and send the stream to the user.
 
#### CREATING A THING TYPE
To create a thing type enter the following commands ```"aws iot create-thing-type --thing-name <value>
    --thing-type-name <value>" ``` and we give it the flag of the name of the thing type we creating and we store it in the **iot thing type**  file in json format.
#### CREATING A THING
A thing is a representation of specific device.
To create a thing we can use this command ```"aws iot create-thing"``` and we give it the flag of the thing name we are creating and the flag of the name of the thing type we created and we are writing to the **iot-thing.json** file.
### CREATING A ROLE
A role is a set of permissions that define what actions are allowed and denied by a user in the AWS console. These permissions are defined in the role policy document.
- To create a role you can use the following command ```"aws iam create-role"```. This command has two flags, which are ```--role-name ``` and ```--assume-role-policy-document```.
- The  ```--role-name ``` flag is used to store the name of the role. It has to be unique and cannot be distinguished by case. 
- The ```--assume-role-policy-document``` flag is used to grant a user permission to take on the role. This flag stores the path to the role policy JSON document which has been converted to a string.
- Then the file should be in JSON format.
### ADDING A PERMISSION POLICY
A role policy is used to define the permissions for a specific role. 
- To add  a pollicy use the following command ```put-role-policy
--role-name <value>
--policy-name <value>
--policy-document <value>```

- To add a role policy you can use the ```aws iam put-role-policy ```. It has three flags which are ```--role-name ```, ```--policy-name ``` and ```--policy-document ```.
- The ```--role-name ``` flag is the name of the role linked to this specific policy.
- The ```--policy-name ``` flag is used to store the name of the policy that we are creating.
- The ```--policy-document ``` flag is the file that stores the permissions for the role.
### CREATING A ROLE ALIAS
A role alias allows you to change a role without having to update the device. To create a role alisa you should run this command ```aws iot create-role-alias 
    --role-alias <value>
    --role-arn <value>
    --credential-duration-seconds <value> ```
- To create a role alias you use the command ```aws iot create-role-alias ```. It has three flags which are ```--role-alias ```, ```--role-arn ``` and ```--credential-duration-seconds ```.
- The ```--role-alias ``` flag stores the name of the role alias.
- The ```--role-arn ``` flag stores the credeentials that give acces to the resources related to the role. 
- The ```--credential-duration-seconds ``` flag stores the amount of time the credentials being used will be valid. This value is an integer.
- **OPTIONAL** To test the creation of the pollicy document you can create a file using the following code ```cat > $GIT_SHA_PATH/iot-policy-document.json <<EOF``` and write out the details of the policy document in json formant. When this is run a policy document will be created.
### CREATING A POLICY
A  policy is used to define the permissions for a user. To create a policy use the following command ```'''aws iot create-policy --policy-name <value> --policy-document <value>'''```
- To create the policy use this command ```'''aws iot create-policy'''``` which has two flags which is ```--policy-name ``` and ```--policy-document```
- The ```--policy-name ``` flag stores the name of the policy created.
- The  ```--policy-document``` flag store the document that stores the policy.
### CREATING KEYS AND CERTIFICATES
Keys are used to control  encryption across a wide range of AWS services and in our applications/environment. Certificates provide AWS IoT with the ability to authenticate client and device connections.
to create keys and certicficate use the following command ```create-keys-and-certificate
[--set-as-active | --no-set-as-active]
[--certificate-pem-outfile <value>]
[--public-key-outfile <value>]
[--private-key-outfile <value>]```
- The create keys and certificate has four main flags which are ```--set-as-active | --no-set-as-active```,```--certificate-pem-outfile``` ```--public-key-outfile``` and ```--private-key-outfile```.
- The ```--set-as-active | --no-set-as-active```flag is a boolean Specifies whether the certificate is active or not active.
- The ```--certificate-pem-outfile``` flag  Saves the command output contents of certificatePem to the given filename.
- The ```--public-key-outfile``` flag Saves the command output contents of keyPair.PublicKey to the given filename.
- The ```--private-key-outfile``` flag Saves the command output contents of keyPair.PrivateKey to the given filename.
### ATTACHING A POLICY TO A CERTIFICATE
  - We are attaching the policy to the certificate using the command ```aws iot attach-policy```.
  - Then the flag of the policy name which we are attaching to a certificate is ```--policy-name```.
  - We specify the certificate we are targeting ```--target``` and give the path where the certificate is located. 

  ### ATTACHING A PRINCIPAL TO A CERTIFICATE
  - We are attaching the principal to the certificate using the command ```aws iot attach-thing-principal ```.
  - Then the flag of the thing name which we are attaching to a certificate to ```--thing-name```
  - We give a flag of the principal ```--principal``` and path of the target certificate.
### DESCRIBING AN END POINT
 An endpoint is the URL of the entry point for an AWS web service. 
 To describe an end-point use the following command ```aws iot describe-endpoint 
    --endpoint-type iot:CredentialProvider 
    --output text ```. 
- The ```--endpoint-type iot:CredentialProvider``` flag  Returns an IoT credentials provider API endpoint.
- The ```--output text``` flag gives out put in text format.
### CREATING KINESIS VIDEO 
- To create a kinesis video stream we used the following command ``` create-stream```.
- Then we set the time which is retention of how long video streams will be lasting before deletion.
- We set stream name ```--stream-name``` flag which is thing name we have created.
 - We use the curl command to send our credentials of the thing we have created to the amazon server.
 ### GETTING CREDENTIALS
 We are getting our credentials for loging in the AWS.
 ### DESCRIBING THE KINESIS VIDEO STREAM
 Returns the most current information about the specified stream and gives the output of the things created. Use the following  command 
 
 ```aws kinesisvideo describe-stream --stream-name <value>```. 
 - The ```--stream-name``` flag we give it the name of the thing we had created. Then we create variables that are going to store information of the things created.
 - Create a new file to keep the renewed token.
