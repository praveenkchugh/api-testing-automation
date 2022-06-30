# api-testing-automation-app

## Pre-requisites

1. Download Anypoint Runtime from https://www.mulesoft.com/lp/dl/mule-esb-enterprise

2. Unzip the folder in your local system under c:\ drive and rename it to "mule-runtime-local"

3. Save api-testing-automation-app.jar file under "c:\mule-runtime-local\app\api-testing-automation-app.jar" 

4. Open Command prompt and go to "c:\mule-runtime-local\bin" folder and enter below command and press enter.
   c:\mule-runtime-local\bin\mule

5. Create below Folder structure in your system

    C:\api-testing-automation
    C:\api-testing-automation\archived
    C:\api-testing-automation\auth0
    C:\api-testing-automation\input
    C:\api-testing-automation\java-api-response
    C:\api-testing-automation\mule-api-response

6. Place auth0 config file under "auth0" folder

  Sample File:
  
{
    "url": "https://auth0.xxxxxxxxx.xxxxxxxx.com/oauth/token",
    "client_id":"ABCFDAJDHALJSasdaljdsasHC",
    "client_secret":"asdlkjasSADkADkhaakshfsakhFAA_sakahf_ashakjf",
    "audience":"https://abc.wfs.wfscorp.com",
    "grant_type":"client_credentials"
}

## Processing 

1. create a csv with below structure and place it under "input" folder

tcnum,mule_api_url,java_api_url,no_of_executions
tc1,https://mule_server/api/v1/customers?customerNumber=12345,https://java_server/api/v1/customers?customerNumber=12345,5
tc2,https://mule_server/api/v1/customers?customerNumber=12345,https://java_server/api/v1/customers?customerNumber=12345,5

2. Program will run in backend and process as below:
    2.1 call mule_api_url 5 times for tc1 & tc2 and place the response under "mule-api-response"
    2.2 call java_api_url 5 times for tc1 & tc2 and place the response under "java-api-response"
    
## More features to be added    
