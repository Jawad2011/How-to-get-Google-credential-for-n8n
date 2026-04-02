# 🔑 How to Get Google Credentials for n8n

![Status](https://img.shields.io/badge/Status-Complete-green?style=for-the-badge)
![Category](https://img.shields.io/badge/Category-Tutorial-blue?style=for-the-badge)
![Tool](https://img.shields.io/badge/Tool-n8n-FF6D5B?style=for-the-badge&logo=n8n&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![License](https://img.shields.io/github/license/Jawad2011/How-to-get-Google-credential-for-n8n?style=for-the-badge)

> ⚠️ **Disclaimer:** This guide is for educational and personal learning purposes only. It is not intended for business or commercial use.

Connect Google Cloud to n8n **once** and reuse the credential across Google Sheets, Gmail, Drive, and more. The process is slightly involved — but this guide breaks it down into clear, numbered steps.

---

## 📋 Overview

| Phase | Steps | What You'll Do |
|---|---|---|
| **Google Cloud** | 1–18 | Create a project and configure OAuth |
| **n8n** | 19–21 | Create the credential and grab the redirect URL |
| **Back to Google Cloud** | 22–23 | Add redirect URLs and generate Client ID & Secret |
| **Finish in n8n** | 24–32 | Paste credentials, add test users, and connect |

---

## ☁️ Phase 1 — Google Cloud Console Setup

### Step 1 — Search for Google Cloud Console
Search **"Google Cloud Console"** in your browser.

### Step 2 — Open the Console
Click on the official Google Cloud Console link from the search results.

<img width="1696" height="912" alt="Image" src="https://github.com/user-attachments/assets/501c1e77-d1f7-4518-96f3-89b337874710" />

### Step 3 — Open the Project Selector
Click the project selector dropdown at the top of the page.

<img width="1919" height="909" alt="Image" src="https://github.com/user-attachments/assets/0d434bb9-b240-45d4-b2db-2d86fce7001b" />

### Step 4 — Create a New Project
Click **"New Project"** from the project selector panel.

<img width="1915" height="910" alt="Image" src="https://github.com/user-attachments/assets/eb70d2bb-7990-4e76-a92e-c610615242a0" />

### Step 5 — Name Your Project
Enter any name you like for your project.

<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/16241c95-afa0-490a-9812-c704f9c78421" />

### Step 6 — Click "Create"
Hit the **Create** button to finish creating your project.

<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/316dd523-e60c-4216-b9f8-45b4bf1f73ce" />

### Step 7 — Select Your New Project
Open the project selector again and select the project you just created.

<img width="1000" height="669" alt="Image" src="https://github.com/user-attachments/assets/31204414-874e-4869-a501-13fc2c7e670e" />

### Step 8 — Open the Navigation Menu
Click the **three-line (hamburger) icon** in the upper-left corner.

<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/9f9765c4-22d0-405c-8363-f1bf9de46a82" />

### Step 9 — Go to OAuth Consent Screen
Navigate to **APIs & Services → OAuth consent screen**.

<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/9d37a40d-b6ee-417f-9567-1df1197b424a" />

### Step 10 — Start Configuration
Click the button to begin setting up the consent screen.

<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/188cb26b-2b85-455e-b36b-3d46fd84049a" />

### Step 11 — Fill in App Details
Fill in the required fields:
- **App name:** `n8n`
- **Support email:** your personal Gmail address *(recommended)*

<img width="1917" height="912" alt="Image" src="https://github.com/user-attachments/assets/28f34516-e16b-496b-ab84-38d4b9ff3a28" />

### Step 12 — Select "External" User Type
Choose **External** so you can authorize your own Google account to use the app.

<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/c2b12993-84f9-4b3c-b207-9e1310c556fc" />

### Step 13 — Add a Contact Email
Enter an email address for developer contact. You can reuse the same address from Step 11. Multiple emails are allowed.

<img width="1919" height="908" alt="Image" src="https://github.com/user-attachments/assets/0c80873e-a6f9-44ac-8e60-6f3caa5c366f" />

### Step 14 — Accept the Terms
Check the checkbox to agree to Google's API terms.

<img width="1919" height="912" alt="Image" src="https://github.com/user-attachments/assets/d345c0c2-d33d-461d-b80c-1c3c3086a107" />

### Step 15 — Submit
Click **Submit** to save your consent screen configuration.

<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/846bfeb1-d072-4b09-b05b-d301f7b23d18" />

You'll land on this confirmation screen:

<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/d8d86058-4388-47e1-bb21-83fcf339146b" />

### Step 16 — Create OAuth Client
Click **"Create OAuth Client"** to proceed.

<img width="1918" height="908" alt="Image" src="https://github.com/user-attachments/assets/920d23c8-55bd-4f8a-a20c-caf9f020e7a9" />

### Step 17 — Set Application Type
From the **Application type** dropdown, select **Web application**.

<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/7f5969a1-a68a-4a07-9229-9cfe1b573fae" />

### Step 18 — Name the OAuth Client
Enter any name you like (e.g. `n8n OAuth Client`). **Don't click Create yet** — you need the redirect URL from n8n first.

<img width="1919" height="912" alt="Image" src="https://github.com/user-attachments/assets/8c5a38e0-39f5-4340-8980-8fbedc8d649c" />

---

## ⚙️ Phase 2 — n8n Credential Setup

### Step 19 — Create a Credential in n8n
Log into n8n, go to **Credentials**, and click **"Create credential"**.

<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/4035fdf9-514f-4b2f-99d4-5d4416cd5239" />

### Step 20 — Search for Google OAuth2 API
Type **"Google OAuth2 API"** in the search bar and select it.

<img width="1919" height="907" alt="Image" src="https://github.com/user-attachments/assets/1fc7ea4c-eacf-4ac8-a50a-65010ea104e5" />

### Step 21 — Click "Continue"

<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/685cd47b-b983-47a4-94a0-fa8285a58b36" />

You'll see this page — **pay close attention here, this is where most people get confused:**

<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/03919c74-0f16-4f06-a0d0-5231007b3bcc" />

There are **3 important fields** on this screen:

| Field | What It Is |
|---|---|
| **Redirect URL** | Auto-generated by n8n. Format: `https://yourdomain.com/rest/oauth2-credential/callback` |
| **Client ID** | Generated in Google Cloud after creating the OAuth client |
| **Client Secret** | Generated in Google Cloud after creating the OAuth client |

---

## 🔗 Phase 3 — Link n8n Redirect URL in Google Cloud

### Step 22 — Add Authorized Redirect URIs
Back in Google Cloud, scroll to **Authorized redirect URIs** and fill in two boxes:

- **Box 1 (Authorized JavaScript origins):** paste only the domain part — `https://yourdomain.com` or `https://yourdomain.com:PORT` if a port is shown in your n8n redirect URL
- **Box 2 (Authorized redirect URIs):** paste the **full redirect URL** from n8n exactly as shown

> 💡 **Note:** `example.com` is used as a placeholder. Replace it with your actual n8n domain. Be careful not to include `/rest/oauth2-credential/callback` in Box 1.

<img width="1919" height="912" alt="Image" src="https://github.com/user-attachments/assets/aac2012e-5104-4f96-86c7-fe329615b8e7" />

### Step 23 — Click "Create"
Click **Create** to generate your **Client ID** and **Client Secret**. Save both — you'll need them in the next step.

<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/3d3e0780-aa46-44c1-a37d-41a1af60f014" />

---

## ✅ Phase 4 — Complete Setup in n8n

### Step 24 — Paste Client ID and Client Secret
Go back to n8n and paste your **Client ID** and **Client Secret** into their respective fields.

<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/38580ba3-4301-4c8c-965a-dcd01ab2f40c" />

### Step 25 — Go to the Audience Tab
Back in Google Cloud, click on the **"Audience"** tab.

<img width="1919" height="909" alt="Image" src="https://github.com/user-attachments/assets/96d34ba8-dacb-4a02-9e08-84c45b358b51" />

### Step 26 — Add Test Users
Scroll down and click **"Add users"**.

<img width="1919" height="912" alt="Image" src="https://github.com/user-attachments/assets/f5aa8dd2-ef75-4961-93f1-768e9d1e75fb" />

### Step 27 — Enter Gmail Accounts
Add the Gmail accounts you'll use to access Google services through n8n. You can add up to **100 accounts**. All addresses must end in `@gmail.com`.

<img width="1919" height="915" alt="Image" src="https://github.com/user-attachments/assets/a6e81702-4e23-417c-b785-fee2d60c1bf8" />

### Step 28 — Save the Test Users
Type each email, press **Enter**, then click **Save**.

<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/113adcd0-0121-4dfd-b6f8-91d3b435016f" />

If your email appears in the list, it was saved successfully ✅

<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/1b8e2f5c-97f7-4c6c-a2ca-642a1a7a22d9" />

### Step 29 — Add the Required API Scope
Enter the API scope URL for the Google service you want to connect. Common examples:

```
https://mail.google.com/
https://www.googleapis.com/auth/drive
https://www.googleapis.com/auth/spreadsheets
https://www.googleapis.com
```

<img width="1357" height="738" alt="Image" src="https://github.com/user-attachments/assets/c5dda6da-ef51-4120-99a3-750b4aeba92e" />

Sign in using the Gmail account you added as a test user in Step 27.



### Step 30 — Sign in with Google in n8n
Back in n8n, scroll down and click **"Sign in with Google"**.

<img width="1919" height="910" alt="Image" src="https://github.com/user-attachments/assets/a97886c0-aac0-40d4-9c10-985dae88c6db" />


### Step 32 — Continue signing in.

#### N.B. The acount that you will use to sign into n8n must remain signed in your device. If it is not, then you have to first sign in the acoount into your device first.



### Step 32 — Bypass the "Unverified App" Warning
You may see a warning screen. This is expected for apps in testing mode — just click **"Continue"**.



### Step 33 — Grant All Permissions
When prompted, check **"Select all"** to grant the necessary permissions, then continue.

<img width="290" height="444" alt="Image" src="https://github.com/user-attachments/assets/b26fef0a-0a13-4347-83a2-ffc4db6d1a2e" />

---

## 🎉 You're Connected!

Once you sign in, n8n will automatically test the connection. A successful test means your Google credential is live and ready to use.

> 📝 **Note:** This guide uses Gmail as the example, but the exact same steps apply to Google Sheets, Drive, Calendar, and all other Google services.

You only need to do this **once**. After that, you can reuse this credential across all your n8n workflows.

---

## ❓ Questions & Support

Got stuck? Open a [GitHub Discussion](../../discussions) — I'll do my best to help.

If this guide saved you time, please give it a ⭐ to help others find it!

---

*Built by [Jawad](https://github.com/Jawad2011) · Educational use only · Open source*
