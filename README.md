# Wild_Rydes_App
Deployed a simple web application that enables users to request unicorn rides from the Wild Rydes fleet.
<img width="561" alt="Screenshot 2024-03-30 at 1 05 36 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/ec5e3815-f31e-438a-bc95-5761a8a94973">
<img width="1077" alt="Screenshot 2024-03-30 at 5 25 17 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/9458cdf4-2bf8-4add-9e6a-d1c8243561bd">


The application will present users with an HTML based user interface for indicating the location where they would like to be picked up and will interface on the backend with a RESTful web service to submit the request and dispatch a nearby unicorn. The application will also provide facilities for users to register with the service and log in before requesting rides.

Amplify Console hosts static web resources including HTML, CSS, JavaScript, and image files which are loaded in the user’s browser via S3. 
JavaScript executed in the browser sends and receives data from a public backend API built using Lambda and API Gateway. 
Amazon Cognito provides user management and authentication functions to secure the backend API.
DynamoDB provides a persistence layer where data can be stored by the API’s Lambda function.

![image](https://github.com/prady13/Wild_Rydes_App/assets/62207613/b79d3ee0-a74c-432a-8249-64e3d9217444)


Step 1- Create an IDE environment on Amazon Cloud9 with the required specs to run AWS CLI commands on the local computer.
<img width="1440" alt="Screenshot 2024-03-22 at 7 55 42 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/965c5447-715d-41ee-8746-0806d2be6435">


Step 2- Now we'll configure AWS Amplify Console to host the static resources for the web application.
<img width="1440" alt="Screenshot 2024-03-22 at 8 11 31 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/32d8b5f8-3ac4-4e12-b041-0f20dd40f2f0">
<img width="1440" alt="Screenshot 2024-03-22 at 8 13 13 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/16768581-788e-467d-b6b5-05ec969bb827">

<img width="1440" alt="Screenshot 2024-03-30 at 2 26 13 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/e998d2db-bdc5-4245-9ac3-6c0c9ba5cba2">
Website Deployed Successfully 

<img width="1440" alt="Screenshot 2024-03-30 at 2 26 33 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/e83b1b5f-692f-4ec6-bee2-ca8e03302664">

Creating User pool on Cognito for sign in/sign up for the users
<img width="1440" alt="Screenshot 2024-03-30 at 2 33 46 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/ea6c9984-5e61-4a14-8924-5d8d87af5c52">

Commited changes in the repo by adding user pool and client ID then we'll be able to sign up through cognito
<img width="1440" alt="Screenshot 2024-03-30 at 2 38 58 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/1c7e4a96-05eb-4a00-b417-874ce83f0d5f">

Successful
<img width="1440" alt="Screenshot 2024-03-30 at 2 40 16 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/59982543-f3f7-45d2-b741-e7e06664f058">

After registering with the email and password Cognito will send us verification code via email (which we set up) and then we will be able to register successfully!
<img width="941" alt="Screenshot 2024-03-30 at 2 43 52 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/90a9f7cd-695e-4a43-8ac7-1c8e3b5b2de2">

<img width="453" alt="Screenshot 2024-03-30 at 2 44 21 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/aca0ef83-2fc2-4e01-a2ba-01edcc6de916">

Now we will build a REST API to invoke the ride sharing functionality, and we will use API Gateway for that function.
Since we are using Cognito user pools we need to create an authorizer to authenticate calls. API Gateway uses JWTs that are returned by Cognito. (Hooking up the two parts by creating this authorizer)
<img width="1083" alt="Screenshot 2024-03-30 at 5 31 00 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/af8b0bb8-b5e5-4dd2-a412-712cc9aac0bf">

API created
<img width="1090" alt="Screenshot 2024-03-30 at 5 40 13 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/abd8b494-caf6-43d4-bd3b-7e178b89ab84">

Updated the invoke url in config.js file
<img width="627" alt="Screenshot 2024-03-30 at 5 41 46 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/c80db234-b799-4d0c-ba0b-4d3bba0261df">

The final working of the webapp as shown.
<img width="1440" alt="Screenshot 2024-03-30 at 5 43 51 PM" src="https://github.com/prady13/Wild_Rydes_App/assets/62207613/2fae3eb2-2bdb-4f50-8969-fc67070fb713">





