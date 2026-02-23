# 🚀 Lab 12.2: Learn PowerShell Basics

Welcome to this introductory lab! We will start by opening the PowerShell Command Line Interface (CLI) and running some fundamental commands, then transition into the PowerShell ISE to write our first scripts.

## 🔍 Exploring Fundamental Commands

Let's run a few basic commands directly in the console to see how PowerShell behaves.

**1. The Help Command:**
If you ever need help with a command, this is your best friend. It returns descriptions, official documentation, and syntax examples.

```powershell
Get-Help

```

**2. List All Commands:**
This retrieves a massive list of every command available on your system. We will learn how to filter this list later in the lab.

```powershell
Get-Command

```

**3. Browse Directories:**
This command lists the files and folders in your current directory. It is the PowerShell equivalent of running `dir` in Command Prompt or `ls` in Linux.

```powershell
Get-ChildItem

```

## 🛠️ Navigating the PowerShell ISE

Now let's move over to the **PowerShell Integrated Scripting Environment (ISE)**. While we could use Visual Studio Code, the ISE interface is incredibly helpful for this specific lab.

```text
1. Click **Start** > search **"PowerShell"** > Open **PowerShell ISE**.
2. Customize your view by clicking on the **View** menu at the top. Ensure the following are checked:
* **Show Script Pane** (Top: Your text editor for writing code)
* **Show Command Add-on** (Right: A searchable list of installed commands)
* *The bottom pane is your Console/Terminal where the output appears.*
```

## 🔢 Working with Variables

Let's declare some variables in the **Script Pane** (the top section) and output their values.

Type the following code into the Script Pane:

```powershell
$stringVariable = "Hello World"
$numberVariable = 5
$numberVariable2 = 10

$stringVariable
$numberVariable
$numberVariable2

```

▶️ **Run the Code:** Click the green **Play** button. You will see the variables get declared, called, and outputted in the console below.
🎯 **Run Selection:** Highlight *only* the bottom three variable names and click the **"Run Selection"** button (or press `F8`) to execute just the highlighted text.

## ⚖️ Comparison Operators

Next, let's test how PowerShell compares data. Run each of these lines individually using the "Run Selection" method to see the results (True or False).

```powershell
$numberVariable -eq $numberVariable2
$numberVariable -lt $numberVariable2
$stringVariable -isnot [string]
$stringVariable -contains "Hello World"

```

## 🚰 The Pipeline & Filtering

Remember when we ran `Get-Command` earlier and got a massive, overwhelming list? Let's use the **Pipe** (`|`) and the **Pipeline Variable** (`$_`) to filter that list down to a specific source.

Run the following command to only show core PowerShell commands:

```powershell
Get-Command | Where-Object {$_.Source -eq "Microsoft.PowerShell.Core"}

```

🧪 **Lab Challenge:** Try modifying the command above! Replace `"Microsoft.PowerShell.Core"` with `"Microsoft.PowerShell.Utility"` or `"Microsoft.PowerShell.Management"` to see how the output changes.

## 📜 Wrap-Up: Reviewing History

To finalize this lab, let's look back at everything we accomplished today. Run the following command to review a list of all the commands you executed during this session:

```powershell
Get-History

```
