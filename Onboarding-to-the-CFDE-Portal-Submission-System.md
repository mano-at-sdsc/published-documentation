As a Common Fund Data Coordinating Center (DCC) you have 3 role options for your users of the submission system:
- **Reviewer**: This is a read only account. Users can see submitted packages, but can’t do anything with them. You can have as many users in this role as you want.
- **Submitter**: Can submit data packages, but can’t approve a package for inclusion in the public portal. You can have as many users in this role as you want.
- **Approver**: Can approve a submitted package to be published to the CFDE portal, but can’t submit new packages. Each DCC has one person who is the approver.

Any given person in your organization can have 0-3 roles. If they have 0, then they can only see the published data, so they will have exactly the same privileges as any regular user of the portal. 

If a user is getting Submitter or Approver privileges, also giving them Reviewer does not add anything

If a user has one or more of the other roles, they get those privileges. Privileges stack. So if one person needs to submit packages and is the final approver, then they need to have both roles. 

The system can only currently support *a single approver* per DCC.

We’re still working out how we will administer roles long term in practice. For the moment, @jeremywalter is acting as admin on all role groups, and will manage adding and removing members from your roles at your request. In the future, we may enable each DCC to manage roles directly.

## Onboarding Process

To do the onboarding, please have a PI or PM at your organization give us a list of people in your org who need Submission System access. For each person please list:

- [their Globus display name](#finding-your-globus-display-name)
- what role(s) you want them to have

Please email your request to the helpdesk: support@cfde.atlassian.net

When your request has been processed, each named will receive an invitation from Globus. *They must [accept this invitation](accepting-a-globus-invitation) to gain access.*

## Finding your Globus Display Name

1. Create a login at https://app.nih-cfde.org/ by clicking “Log In” button on the top left corner of the page.
1. The “Log In” button will open a “Globus” pop-up window requiring you to login using existing credentials.
1. Select your organization, or select to log in using Google or an ORCID ID 
1. Use your relevant credentials to log in
1. Successful processing of your login will give you access to the CFDE portal. You will now see your name displayed on the top right corner if logged in successfully.
1. Click on the drop down button next to your name. Select “My profile” from the menu. This will open a pop-up window with some details about your profile.
1. You will see your “Display Name” (Eg: xxxxxx@umaryland.edu) in the window. This is your “Globus display name”


## Accepting a Globus Invitation

1. You will receive the invitation by email from `noreply@groups.globus.org`
1. In the email click the link that reads "Click here to apply for membership"
1. This will open a Globus log in page in your web browser
1. Log in using the same Globus credentials you used to [find your Globus display name](#finding-your-globus-display-name)
1. You will be asked if the CFDE submission system can have permission to use your account, you must choose `Allow`