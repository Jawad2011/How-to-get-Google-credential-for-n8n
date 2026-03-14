# How-to-get-Google-credential-for-n8n
![Status](https://img.shields.io/badge/Status-Complete-green?style=for-the-badge)
![Category](https://img.shields.io/badge/Category-Tutorial-blue?style=for-the-badge)
![Tool](https://img.shields.io/badge/Tool-n8n-FF6D5B?style=for-the-badge&logo=n8n&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![License](https://img.shields.io/github/license/Jawad2011/How-to-get-Google-credential-for-n8n?style=for-the-badge)
### Disclaimer: This is for educational/learning purposes only. It cannot be used for business purposes. ###
  Hello, all. In this repo, we will know how to get Google credentials from Google cloud console for n8n. You will set up only once and can use it multiple times in n8n. This process is slightly complex but I will try to break it down step-by-step. So, let's start:

Step 1: 
Search "Google Cloud Console"

Step 2: 
Click on the link shown here
<img width="1696" height="912" alt="Image" src="https://github.com/user-attachments/assets/501c1e77-d1f7-4518-96f3-89b337874710" />


Step 3:
Click here. 
<img width="1919" height="909" alt="Image" src="https://github.com/user-attachments/assets/0d434bb9-b240-45d4-b2db-2d86fce7001b" />


Step 4: 
Click "new project" from here.
<img width="1915" height="910" alt="Image" src="https://github.com/user-attachments/assets/eb70d2bb-7990-4e76-a92e-c610615242a0" />


Step 5:
choose any name and type it here
<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/16241c95-afa0-490a-9812-c704f9c78421" />


Step 6:
Now click "Create"
<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/316dd523-e60c-4216-b9f8-45b4bf1f73ce" />


Step 7:
Select the project you created.
<img width="1000" height="669" alt="Image" src="https://github.com/user-attachments/assets/31204414-874e-4869-a501-13fc2c7e670e" />


Step 8:
Click on this three line icon on the upper left side.
<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/9f9765c4-22d0-405c-8363-f1bf9de46a82" />


Step 9:
select "OAuth consent screen"
<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/9d37a40d-b6ee-417f-9567-1df1197b424a" />


Step 10:
Click here.
<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/188cb26b-2b85-455e-b36b-3d46fd84049a" />



Step 11: 
Fill the details
1. Name it "n8n"
2. put the e-mail where Google will contact with you. It is recommended that you use your own g-mail account
<img width="1917" height="912" alt="Image" src="https://github.com/user-attachments/assets/28f34516-e16b-496b-ab84-38d4b9ff3a28" />



Step 12: 
Select "External"
<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/c2b12993-84f9-4b3c-b207-9e1310c556fc" />


Step 13:
Put an E-mail address. You may use the e-mail address given to the step 11. You can add more than one e-mails too.
<img width="1919" height="908" alt="Image" src="https://github.com/user-attachments/assets/0c80873e-a6f9-44ac-8e60-6f3caa5c366f" />



Step 14: 
Mark it
<img width="1919" height="912" alt="Image" src="https://github.com/user-attachments/assets/d345c0c2-d33d-461d-b80c-1c3c3086a107" />


Step 15:
Click "Submit"
<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/846bfeb1-d072-4b09-b05b-d301f7b23d18" />

After you submit, you will see ths screen:
<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/d8d86058-4388-47e1-bb21-83fcf339146b" />


Step 16:
click "Create OAuth client"
<img width="1918" height="908" alt="Image" src="https://github.com/user-attachments/assets/920d23c8-55bd-4f8a-a20c-caf9f020e7a9" />


Step 17:
Select "Web application" from "Application type"
<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/7f5969a1-a68a-4a07-9229-9cfe1b573fae" />


Step 18: 
Type any name you want
<img width="1919" height="912" alt="Image" src="https://github.com/user-attachments/assets/8c5a38e0-39f5-4340-8980-8fbedc8d649c" />


At this stage, We need to go to n8n.


Step 19:
Log into your n8n and select credentials. Then, click on "Create credential"
<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/4035fdf9-514f-4b2f-99d4-5d4416cd5239" />


Step 20:
Now type "Google OAuth2 API" and select "Google OAuth2 API"
<img width="1919" height="907" alt="Image" src="https://github.com/user-attachments/assets/1fc7ea4c-eacf-4ac8-a50a-65010ea104e5" />


Step 21:
Click "Continue"
<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/685cd47b-b983-47a4-94a0-fa8285a58b36" />


After that you will stumble upon this page:
<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/03919c74-0f16-4f06-a0d0-5231007b3bcc" />

In this part, you must focus. Everyone gets confused at this stage.

1. Redirect URL: you will use this URL. This URL will be in https://example.com/rest/oauth2-credential/callback format. Here example.com is the name of the domain. You must understand it because You will need it to generate "Client ID" and "Client Secret" using this link.

2. Client ID: This will be generated after creating "OAuth Client ID"

3. Client Secret:  This will be generated after creating "OAuth Client ID"

Step 22:
In the box number 1 you will put only https://example.com or https://example.com:xxxx (if the port is mentioned in the link given by n8n)

In the box number 2 you will just copy and paste the link. 


<img width="1919" height="912" alt="Image" src="https://github.com/user-attachments/assets/aac2012e-5104-4f96-86c7-fe329615b8e7" />


Note: example.com is not a real domain. You will just paste the part before /rest/oauth2-credential/callback in the box number 1. You must be exttra careful in this area.


Step 23:
Click "Create"
<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/3d3e0780-aa46-44c1-a37d-41a1af60f014" />


After that your "Client ID" and "Client secret" will be generated. Save that "Client ID" and Client secret" for future purposes. Now we need to go back to Google Cloud Console.


Step 24:
Copy and paster your "Client ID" and "Client secret" into their boxes in n8n.
<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/38580ba3-4301-4c8c-965a-dcd01ab2f40c" />


Step 25:
Click on "Audience"
<img width="1919" height="909" alt="Image" src="https://github.com/user-attachments/assets/96d34ba8-dacb-4a02-9e08-84c45b358b51" />


Step 26:
Scroll down and click on "Add users"
<img width="1919" height="912" alt="Image" src="https://github.com/user-attachments/assets/f5aa8dd2-ef75-4961-93f1-768e9d1e75fb" />


Step 27:
In this box, type the e-mail accounts that you will use to access Google services in n8n. You can add upto 100 e-mail accounts. the e-mail accounts must end with @gmail
<img width="1919" height="915" alt="Image" src="https://github.com/user-attachments/assets/a6e81702-4e23-417c-b785-fee2d60c1bf8" />


Step 28: 
Type the e-mails and press enter. After that click on "Save"
<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/113adcd0-0121-4dfd-b6f8-91d3b435016f" />


If your e-mail shows up here. That means your e-mail has been saved propely.
<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/1b8e2f5c-97f7-4c6c-a2ca-642a1a7a22d9" />

Step 29:
Go to your n8n and scroll down. Then, click on "Sign in with Google"
<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/a97886c0-aac0-40d4-9c10-985dae88c6db" />


Then, sign in with the account that you given as the test user in step 27.


Step 30:
During signing in, you will see something like below. That is not a problem. Just click "Continue"
<img width="1919" height="971" alt="Image" src="https://github.com/user-attachments/assets/ed6db268-f24d-4147-8eea-b1fd363ac62a" />


Step 31:
At one stage, you will get this option. Just checkmark "Select all"

<img width="290" height="444" alt="Image" src="https://github.com/user-attachments/assets/b26fef0a-0a13-4347-83a2-ffc4db6d1a2e" />




After signing in, n8n will test your connection and if they that the connection is okay, that means you succesfully connected n8n and google credential. You can later use this credential to use other Google services.

N.B. In this tutorial, I used G-mail but everything is also same in other services. 





If you have any question, just ask on discussions. I tried to simplify this process as much as I can. If this guide helped you, please give it a ⭐ to help others find it!
