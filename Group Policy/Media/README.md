Group Policy Password Policy Configuration



This lab demonstrates how I created and enforced a new Password Policy using Group Policy Management on a Windows Server domain.  

The goal was to apply a stricter password policy for all domain users and verify that the configuration was successfully applied to the environment.



&nbsp;Steps Taken



1\. Created a New Password Policy GPO

\- Opened \*\*Group Policy Management (GPMC)\*\*.

\- Right-clicked the \*\*Domain\*\* and selected \*\*Create a GPO in this domain, and Link it here...\*\*

\- Named the GPO: \*\*Password Policy\*\*.

\- Edited the GPO and navigated to: Computer Configuration

→ Policies

→ Windows Settings

→ Security Settings

→ Account Policies

→ Password Policy



Modified key settings such as:

\- Minimum Password Length  

\- Maximum Password Age  

\- Password History  

\- Complexity Requirements



2\. Linked and Applied the GPO

\- Confirmed the GPO was linked at the domain level to ensure coverage for all users.

\- Ensured the policy was properly linked and visible under the domain in GPMC.



3\. Forced Group Policy Update

To apply the policy immediately, I ran the following command: "gpupdate /force"



This enforced the new password policy across domain computers without waiting for the default refresh interval.



Verification

To confirm the policy was applied

\- Checked \*\*Resultant Set of Policy (RSoP) or ran: "gpresult /r"





\- Confirmed the new Password Policy settings appeared under Computer Settings → Security Settings.



Evidence

Screenshots captured for:

\- The Password Policy within the GPO Editor  

\- The GPO linked under the domain in GPMC  

\- Command prompt showing `gpupdate /force`  

\- gpresult output verifying policy application  



Summary

This lab demonstrates understanding of:

\- Creating and editing Group Policy Objects  

\- Enforcing domain-wide security settings  

\- Using command-line tools to apply and verify policies  



Group Policy\\Media\\GROUP POLICY.png

Group Policy\\Media\\GP CMD PROMPT.png

Group Policy\\Media\\GPO Editor.png

