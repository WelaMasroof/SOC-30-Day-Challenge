learned about how to analyze security log related to sign in, login
attempts, wrong auth by users.

\### What are windows security logs?

These are base on these things:

1\. Login attempts (failed or passed) 2. Account lockouts when user puts
max no of wrong passwords 3. Audit policies for change in policy 4.
Group Membership Change 5. Privilege Escalation when a user gets it

\### Event IDs for security:

\- \*\*Event ID 4624\*\*: Successful Logon. - \*\*Event ID 4625\*\*:
Failed Logon. - \*\*Event ID 4740\*\*: Account Lockout. - \*\*Event ID
4732\*\*: A user was added to a security-enabled local group. -
\*\*Event ID 4672\*\*: Special privileges assigned to a new logon
(Privilege escalation).

\### Lab Task: Stimulate Failed Login attempt.

step 1:

1\. created user named user1 2. Then used wrong pass to connect to the
user using this command on power shell \`net use \\\\127.0.0.1\\IPC$
/user:user1 WrongPassword\`

also I can just log out and then try to login with wrong pass

Step2:

1\. Check for the login in the Win event viewer 2. Check for the code
4625 in the event code which can show the failed login

Here 4624 can show the correct login for the user
