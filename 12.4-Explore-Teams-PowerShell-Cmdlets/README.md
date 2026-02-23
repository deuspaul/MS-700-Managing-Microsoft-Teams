# 🚀Getting Started with Microsoft Teams PowerShell

Welcome to this lab! Follow the steps below to set up your environment and install the necessary modules.

## 📥Prerequisites

Before we begin, we need to open the right tools with the correct permissions.

Open PowerShell ISE: Search for "PowerShell ISE" in your Start menu.

Run as Administrator: Right-click the icon and select "Run as administrator" 🛡️. This ensures you have the permissions required to install new software.

## 🛠️Install the Microsoft Teams PowerShell module

🛠️`Install-Module -Name MicrosoftTeams`
First-time installation: PowerShell will ask for your authorization to install dependencies like NuGet 📦. Type Y or A (Yes to All) when prompted.

🔓 Execution Policy
To run scripts in this session, we need to bypass execution policies. As a best practice, we only bypass the current process so the policy returns to "Restricted" once the session is closed.
`Set-ExecutionPolicy Bypass -Scope Process`

## 🔗 Connecting to Teams

Now, let's load the module and sign in to your organization.

Import the Module:
`Import-Module MicrosoftTeams`
💡 Tip: If you refresh the "Commands add-on" in ISE, you should now see the Teams module listed.

Verify Commands:
List all available commands within the module:
`Get-Command -Module MicrosoftTeams`

Sign In:
`Connect-MicrosoftTeams`
After a successful login, your Tenant Information will be displayed on the screen.

## 📂 Managing Teams

Once connected, you can begin managing your environment using standard PowerShell verbs (Get, New, Remove).

List all teams:
`Get-Team`

Create a team:
`New-Team`
(Note: This can take about 3-5 minutes to provision) ⏳

Remove a team:
`Remove-Team -GroupId <ID>`

## 🔍 Using the Command Add-on

The PowerShell ISE Command Add-on is a great way to explore cmdlets visually.

Select the MicrosoftTeams module from the drop-down.
`Find-CsGroup`: Use this to search for groups. When you select it, a form appears for your parameters.

Try typing the name of a team in the SearchQuery field.

`Get-TeamUser`: To list users in a specific team (e.g., "Sales and Marketing"):

Copy the ID from your team (e.g., 5ad9bfd3-1ec2-4905-accb-be1c7f511d63).

Paste it into the GroupId field and run.

## 📢 Feedback Policies

To wrap up the lab, let’s look at how feedback is handled in your tenant.

Search for "Feedback" in the Commands module.

View Policy:
`Get-CsTeamsFeedbackPolicy`

Modify Policy: You can use `Set-CsTeamsFeedbackPolicy` to edit these details, or use other cmdlets to remove or assign them as needed⚙️
