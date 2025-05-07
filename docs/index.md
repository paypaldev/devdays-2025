# PayPal Developer Days 2025 Hackathon Resources
We’re excited to have you join in on the hackathon. Use this page for anything and everything you’ll need to participate and submit your project.  
 
Don’ t be shy, come say hi: we’ll have PayPal engineers and PMs on-site throughout the event to help you. We can’t wait to see what you build!  

# Requirements 
## What to Build 
Below are three challenges you can choose from. Review each of them for instructions on any account creations, etc. that you may need.  

### Challenge 1: Agentic Integrations 

Develop an agent that addresses a common business challenge that leverage MCP Server, Agent Toolkit or PayPal APIs A few ideas to get you started are:  
* Complete a checkout process using PayPal agentic processes
* Post purchase agentic flows
* Refund and dispute management
* Subscription management

**There are two ways of connecting to PayPal’s MCP server:** 
 
* Local PayPal MCP Server Using the Agent Toolkit: This option enables developers to download, install, and run the PayPal MCP server locally on their own machines. It supports a wide range of MCP clients, including Claude Desktop and Cursor AI. 
* Remote PayPal MCP Server: This option opens the door to a broader audience—particularly users who prefer not to install local MCP servers. With remote PayPal MCP support, users have an endpoint that any MCP client can connect to seamlessly, allowing continuity of work across clients with a simple PayPal login.

**Quick links:** 

* [PayPal MCP Server](https://developer.paypal.com/tools/mcp-server/): how to set up, run locally, connect remotely
* [Blog: PayPal Begins Rollout of MCP Servers to Accelerate Agentic Commerce](https://developer.paypal.com/community/blog/paypal-model-context-protocol/)
* [More on Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction?wt.mc_id=studentamb_263805)
* Agent Toolkit:
  * [Blog: PayPal Releases Agent Toolkit](https://developer.paypal.com/community/blog/paypal-agentic-ai-toolkit)
  * [paypal/agent-toolkit](https://github.com/paypal/agent-toolkit/) 
* [PayPal APIs Public Postman Collection](https://www.postman.com/paypal)

**PaymentlinkServ is a limited release and will work with local MCP server only.**
In order to use paymentlinkserv to generate a PaymentLink as part of the hackathon do the following:
* Clone repo  https://github.com/paypal/agent-toolkit
* Switch to branch https://github.com/paypal/agent-toolkit/tree/feature/payment-links
* Update config in ~/Claude/claude_desktop_config.json with the below config.
```
{
  "mcpServers": {
   "paypal": {
    "command": "npx",
    "args": [
     "-y",
     “/<path>/agent-toolkit/modelcontextprotocol/dist/index.js",
     "--tools=all"
    ],
    "env": {
     "PAYPAL_ACCESS_TOKEN”:”<token>,
     "PAYPAL_ENVIRONMENT": "SANDBOX"
    }
   }
  }
} (
```

**Recommended platforms (but use what you want):**  
* [Cursor](https://www.cursor.com/en)
* [Claude](https://claude.ai/login?returnTo=%2F%3F#features)
* [There really are so many… ](https://modelcontextprotocol.io/clients)

**Note:** Please see the specific setup instructions for this challenge [below](#sandbox-setup-for-challenge-1-agentic-integration)

### Challenge 2: Vibe Coding with Replit  
We’ve partnered with Replit, a Conversational AI and browser-based IDE that simplifies building, testing, and deploying applications. For this challenge, build an application on Replit using PayPal integrations. Get creative, take advantage of [Pay your own way](https://www.youtube.com/watch?app=desktop&v=oZNeLfLEkCs) options when you’re building out your app.

For this challenge, you’ll need a Replit account. Sign up here for a free account: [https://replit.com/signup](https://replit.com/signup) (note that the free account limits you to 20 checkpoints) 

To get a quick sense of how Replit works, check out these resources:  

* **Getting Started:** [Quickstart tutorial](https://docs.replit.com/getting-started/quickstarts/no-code-cat-image-generator)  
* **Video Overviews:**
    * [Introduction to Replit](https://www.youtube.com/watch?v=ji8C1LxWyXU)
    * [More Features](https://www.youtube.com/watch?v=JNH2g53T3zE)  
* **Technical Deep Dive (for developers):** [Tech Talk](https://www.youtube.com/watch?v=dtuwxIJrnS0)  
* New Replit Agent v2: [Clone Reddit in two prompts](https://www.youtube.com/watch?v=fAYO58NqMog) *(only available with Core membership)*

### Challenge 3: Upgrade your legacy integration
Bring your existing use case and work with the PayPal team to upgrade using our latest SDKs and beta products – specifically focusing on upgrades to web integrations to adopt our latest Web SDK (V6 JS SDK) or some of our latest best practices for accepting PayPal Payments. 

**Quick links:** 
* [V6 JS SDK Integration Guide](https://developer.paypal.com/limited-release/sdk/js/v6/integrate/)
* [PayPal Server SDKs](https://developer.paypal.com/serversdk/net-standard-library/getting-started/how-to-get-started)
* [Best Practices for PayPal Checkout](https://developer.paypal.com/docs/checkout/standard/best-practices/)
* [Pay Now vs Continue Flow](https://developer.paypal.com/docs/checkout/standard/customize/pay-now/)
* [Shipping Module](https://developer.paypal.com/docs/checkout/standard/customize/shipping-module/)

## What to Submit

You’ll submit your project via a Microsoft form. **Deadline is Wednesday April 30th, 5PM PT.**

Link to the submission form: [DevDay 2025 hackathon Submission Form](https://forms.office.com/r/hJJrg2X1xJ)

What to submit: Click the form link to see what information you’ll be required to submit.  

* General team info: You’ll need to submit everyone on your teams information, your team name, contact information etc.
* A link to your project code (make sure it’s public/ visible in GitHub)
* A video (about 5 minutes) that demonstrates your submission.
   * Videos must be viewable for the judges, suggested to upload to YouTube, Vimeo, or Facebook Video.
   * Another idea is to do a virtual meeting and make a recording, teams or google depending on what is easy for you. **NOTE:** please test the URL to make sure the link you send in your submission is viewable for the judges.
   * Please use audio to talk through your demo and answer the following questions and include the following details:
      * Team name
      * Challenge you chose
      * 1-2 sentence pitch, tell us about your project
      * What was used & what else would you do if you had more time? 

Please check the **[Official Rules](./Developer_Day_Hackathon_ 2025_Official_Rules_v4_04_27_25.pdf)** for full details. 

# Resources
## Sandbox Overview & Setup 
To start working with the PayPal APIs, you’ll need to have a PayPal account to log in to the Developer Dashboard.  

### Account Setup 

If you don’t already have a PayPal account, start at Step 1. Otherwise, you can skip to Step 2. 

**Step 1:** 

Go to [developer.paypal.com](https://developer.paypal.com/), click the Sign Up button in the upper right corner and follow the prompts to create a **Personal** account & complete all the verification steps.  

**Step 2:**

Log in to the Developer Dashboard at [developer.paypal.com](https://developer.paypal.com/). 

By default, you will automatically have one default buyer account (personal) and one default seller (business) account, which you can see by going to Testing Tools > Sandbox Accounts.  From here, you can click on the buyer account to obtain the login & password required for completing payments. 

If you’d like additional buyer accounts with ample pre-loaded funding, come see us at the table. We have easy to use, pre-configured accounts available for you.  

## Sandbox Setup for Challenge 1: Agentic integration  

### May 7, 2025 Update: Now that the hackathon has ended, we're no longer provisioning accounts with this scope. It will be released in the near future and will be available to all developers through the PayPal Developer Dashboard.

For this challenge, we’ll need to add a new scope to your client ID for a new feature not yet available directly from the developer dashboard. 

**Steps to find your client ID and send it to us:** 

Go to the developer dashboard: [developer.paypal.com/dashboard](https://developer.paypal.com/dashboard/) 

1. Click on Apps and Credentials from the top menu
2. Copy your Client ID to the clipboard
3. Send an email:

   ```
   To: **REDACTED AFTER THE HACKATHON ENDED**
   Subject: Please update my client ID
   Body:
   Hi PayPal,

   Please add the new scope to my client ID.

   Name: ADD YOUR NAME HERE
   My Client ID: PASTE YOUR CLIENT ID HERE

   Thanks! 
   ```
5. Wait for your email reply confirming the scope was added.
6. Generate a new access token with the following cURL command:
   ```
   curl --location 'https://api.sandbox.paypal.com/v1/oauth2/token'
   --header 'Content-Type: application/x-www-form-urlencoded' \
   --header 'Accept: application/json' \
   --header 'Accept-Language: en_US' \
   --user 'CLIENT_ID:CLIENT_SECRET'\
   --data-urlencode 'grant_type=client_credentials' \
   --data-urlencode 'ignoreCache=true' \
   --data-urlencode 'response_type=token' 
   ```
   Questions, didn’t get an email? Come find a staff member onsite in the room.

   ## How judging will work
   You must submit your project by Wednesday April 30th at 5PM PT to be eligible for judging.

   Quickly after the deadline, a team of PayPal engineers and executives will review the submissions and select the finalists who will be invited to present live on Thursday morning during the general session. Up to ten teams will be invited to demo live on-site. You will be notified via email within a few hours if you’ve made it to the finalist round or not.

   After the finalist teams demo their projects, a panel of PayPal executives will judge and select the First, Second, and Third place winning teams.

   **NOTE:**  When you submit your project via the Microsoft form, you’ll be asked to acknowledge that you will be available to demo live in person on Thursday and that you’re able to participate if selected as a finalist.  

## Judging Criteria 

Below are the categories to which your project will be evaluated. Think about the following questions when working through your idea.  

**Business Relevance** 
* Does the solution address a specific, real-world business challenge or opportunity?
* Presentation: How clearly is the project communicated? Was the demo effective?   

**Innovation/ Creativity / Potential Impact**
* Is the solution unique or does it introduce a novel approach to an existing problem?
* How effectively does the project deliver measurable value (e.g. increased efficiency, cost savings, revenue growth)?  

**Technical Implementation**
* End-to-End Functionality: Does the submission present a fully working demo or proof of concept from start to finish (e.g., user flow, payment flow, confirmation)?
* How effectively is PayPal integrated into the project’s workflow?    

**Technical Quality**   
* Does the solution demonstrate quality software development?
* Production Readiness: If expanded, could the project go live with minimal additional effort?
* Use of Features: Does the solution go beyond basic payment acceptance to utilize PayPal’s other capabilities where applicable?
* How effectively is PayPal integrated into the project’s workflow?

## Agenda
The hackathon is open for about 24 hours, starting on Tuesday April 29th at 5:515PM PT (when the welcome presentation starts) and goes until Wednesday April 30th at 5PM PT when your project is due.  

The room is a resource to you, come hack, ask questions from PayPal engineers, etc. You are not required to stay in the room during the entirely of the hackathon. 

The room (Café 17) will be open during the following times: 

<table>
<tr>
<th colspan="2">Tuesday, April 29</th>
</tr>
<tr>
<td> 5:15 </td>
 <td> PM Attendee check-in <br/> Welcome presentation <br/> Start hacking! </td>
</tr>
 <tr>
  <td> 7:00 PM </td>
  <td> Doors close for the night </td>
 </tr>
<tr>
<th colspan="2">Wednesday, April 30</th>
</tr>
<tr>
<td> 9:00 AM </td>
 <td> Room opens for hackers, mentors available to answer questions </td>
</tr>
 <tr>
  <td> 11:45 PM- 1:00 PM </td>
  <td> Lunch Break (can continue hacking in room) </td>
 </tr>
 <tr>
  <td> 3:00 PM </td>
  <td> Room closing soon! Final reminder on submission deadline + link </td>
 </tr>
 <tr>
  <td> 3:30 PM </td>
  <td> Room Closed - General Session Starts NOW </td>
 </tr>
 <tr>
  <td> 5:00 PM </td>
  <td>Submissions Due via submission link – hackathon finished </td>
 </tr>
</table>

