# Phishing-Attack-Simulation-with-Gophish

<h2>Utilities and Languages Used</h2>

- <b>Gophish: Phishing simulation tool</b> 

- <b>Railway: Platform for deploying and hosting Gophish</b>
  
- <b>GitHub: Code repository platform used to fork and store the Gophish code</b>
  
- <b>Docker: Used to containerize the Gophish application for easier deployment</b>
  
- <b>Git: Version control system for tracking changes and deploying updates</b>

- <b>JSON: Configuration format for Gophish settings.</b>

- <b>Web Browser: For accessing deployed Gophish and Railway dashboards</b> 


 <h2>Program Walkthrough</h2>
 
- <h2>Prerequisites:</h2>
  
  <b>- GitHub account</b>
  
  <b>- Railway account</b>
  
  <b>- Basic understanding of phishing simulations and security awareness</b>

 <h2>Step 1: Fork the Gophish Repository</h2>
    <p>Fork the <a href="https://github.com/gophish/gophish(https://github.com/immanuellee/Gophish/tree/master)">Gophish GitHub repository</a> to your own account.</p>

<h2>Step 2: Edit the config.json File</h2>
    <p>Modify <code>listen_url</code> to <code>0.0.0.0:3333</code>, set <code>use_tls</code> to <code>false</code>, and add Railway domain under <code>trusted_origins</code>.</p>
<img width="868" alt="Screenshot 2025-03-04 at 10 32 44 PM" src="https://github.com/user-attachments/assets/3858d790-8db4-49fa-bd77-204a5a63eb2c" />


<h2>Step 3: Deploy Gophish on Railway</h2>
    <p>Sign up/log in to <a href="https://railway.app/">Railway</a>, create a new project, and deploy from your GitHub repo.</p>
    <h2>Step 4: Configure Environment Variables in Railway</h2>
    <p>Next, in the <strong>Variables</strong> tab on Railway, create a new variable:</p>
    <pre><code>PORT = 3333</code></pre>
    <p>This is because the Gophish admin server listens on port 3333.</p>

<h2>Step 5: Access Deployment Logs</h2>
    <p>Under the <strong>Deployments</strong> section of your Railway project, click <strong>View Logs</strong> to view the latest deployment logs.</p>
    <p>In the logs, you will find an entry similar to:</p>
    <pre><code>Please login with the username admin and the password ce9c0af546f4411.</code></pre>
    <p>You'll need these credentials to log into the Gophish admin server.</p>
<img width="990" alt="Phishing 1" src="https://github.com/user-attachments/assets/38c7e482-044d-4f31-8a0f-f441daead9ff" />

<h2>Step 6: Log in to the Gophish Admin Interface</h2>
    <p>After deployment, use the temporary admin credentials from Railway logs to log in to Gophish. After you will be able to create a new login</p>

<h2>Step 7: Configure Gophish for Phishing Simulations</h2>
    <p>Create users, groups, email templates, sending profiles, and landing pages.</p>

<h2>Step 8: Launch a Phishing Campaign</h2>
    <p>Set up a new campaign using the configured templates, users, and landing pages. Click <strong>Launch Campaign</strong>.</p>

<h2>Step 9: Monitor Campaign Results</h2>
    <p>Track user interaction with phishing emails, such as clicks and credential submissions.</p>

<h2>Step 10: (Optional) Set Up a Custom Domain</h2>
    <p>If preferred, configure a custom domain on Railway and update <code>trusted_origins</code> in <code>config.json</code>.</p>
