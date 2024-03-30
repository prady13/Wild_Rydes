# Wild_Rydes_App
Deployed a simple web application that enables users to request unicorn rides from the Wild Rydes fleet.
<img width="1396" alt="Screenshot 2024-03-30 at 6 11 42 PM" src="https://github.com/prady13/Wild_Rydes/assets/62207613/1e4d706b-6528-49aa-8af0-28c0828a9a5c">



The application will present users with an HTML based user interface for indicating the location where they would like to be picked up and will interface on the backend with a RESTful web service to submit the request and dispatch a nearby unicorn. The application will also provide facilities for users to register with the service and log in before requesting rides.

Amplify Console hosts static web resources including HTML, CSS, JavaScript, and image files which are loaded in the user’s browser via S3. 
JavaScript executed in the browser sends and receives data from a public backend API built using Lambda and API Gateway. 
Amazon Cognito provides user management and authentication functions to secure the backend API.
DynamoDB provides a persistence layer where data can be stored by the API’s Lambda function.


Steps
<img width="491" alt="Screenshot 2024-03-30 at 6 05 16 PM" src="https://github.com/prady13/Wild_Rydes/assets/62207613/f4726a85-1012-4ff0-8fb4-684d25a19aab">

Hosting on Amplify
<img width="1341" alt="Screenshot 2024-03-30 at 6 06 51 PM" src="https://github.com/prady13/Wild_Rydes/assets/62207613/a3884ccc-fb8b-42dc-93c9-fd2a55c6acdf">


Website Deployed Successfully 
<img width="1416" alt="Screenshot 2024-03-30 at 6 07 39 PM" src="https://github.com/prady13/Wild_Rydes/assets/62207613/b6a59d5c-055e-420f-ad93-11c67f17615c">


Creating User pool on Cognito for sign in/sign up for the users
<img width="1034" alt="Screenshot 2024-03-30 at 6 09 28 PM" src="https://github.com/prady13/Wild_Rydes/assets/62207613/2b0bdbf1-5a56-4935-9390-c3ad133647f3">

After registering with the email and password Cognito will send us verification code via email (which we set up) and then we will be able to register successfully!
<img width="398" alt="Screenshot 2024-03-30 at 6 10 45 PM" src="https://github.com/prady13/Wild_Rydes/assets/62207613/9627be1f-632b-44f3-8ba4-6c752c44d2e5">


Now we will build a REST API to invoke the ride sharing functionality, and we will use API Gateway for that function.
Since we are using Cognito user pools we need to create an authorizer to authenticate calls. API Gateway uses JWTs that are returned by Cognito. (Hooking up the two parts by creating this authorizer)
<img width="1054" alt="Screenshot 2024-03-30 at 6 12 28 PM" src="https://github.com/prady13/Wild_Rydes/assets/62207613/e716a918-8c7e-4da7-941f-4b319d054bc8">

API created
<img width="1079" alt="Screenshot 2024-03-30 at 6 13 02 PM" src="https://github.com/prady13/Wild_Rydes/assets/62207613/3d786892-08e6-4582-87d1-dd103cba430d">


Updated the invoke url in config.js file
<img width="669" alt="Screenshot 2024-03-30 at 6 13 21 PM" src="https://github.com/prady13/Wild_Rydes/assets/62207613/d54abb71-e03c-4dbe-9807-415afdcd5ed8">


The final working of the webapp as shown.
<img width="1431" alt="Screenshot 2024-03-30 at 6 13 59 PM" src="https://github.com/prady13/Wild_Rydes/assets/62207613/94c4262a-280f-4254-bae8-bd29aa0bfa09">





