# 🚀 Lab: Exploring the Microsoft Graph API

Welcome to this quick overview of the Microsoft Graph Explorer! In this lab, we will review the tool's interface and practice running sample queries to understand how data is retrieved.

## 🌐 Getting Started

To start out with this lab, open your web browser and navigate to the Graph Explorer:
`aka.ms/ge`

## 🗺️ Navigating the Interface

Once the page loads, let's take a look at the main components:

* **The Address Bar:** Located near the middle of the site (similar to a browser's address bar), this is where you input the **API endpoint** you want to reach.
* **API Operations:** To the left of the address bar, a drop-down menu allows you to select your HTTP Method.

| Method | Description in Graph API |
| --- | --- |
| **GET** | Retrieves or fetches data from the API endpoint. |
| **POST** | Creates new resources (like teams, chats, or channels). |
| **PUT / PATCH** | Updates existing resources. |
| **DELETE** | Removes resources. |

### 👤 Sample Tenant vs. Your Tenant

Because we are not currently signed in, the Graph Explorer is running in a **sample tenant**.

* If you run a query right now, you will get a response containing information about a sample user.
* *Note: If you wanted to query your own tenant, you would click the **Sign In** button at the top right. For this lab, we will **stay signed out** to continue using the sample data.*

## 🧪 Running Sample Queries

On the left side of the screen, you will see a menu packed with sample queries for various Microsoft services.

### 1. Locate Teams Queries

Scroll through the menu to find the Teams categories:

* `Microsoft Teams`
* `Microsoft Teams beta`
* `Teams targeting`

Expand the **"Microsoft Teams"** section. You'll notice examples using both `POST` (to create items) and `GET` (to fetch data).

### 2. Fetch Joined Teams

Let's try a `GET` request to see what teams our sample user belongs to.

1. Click on **"my joined teams"** in the left menu.
2. Click the **Run query** button.
*At the bottom of the screen, the response will list the teams that your account is a member of.*

## 🔄 Modifying Queries with IDs

Let's practice swapping out that Team ID to get information about a different group.

### **Step 1: Get a new Team ID**

1. Run the **"my joined teams"** query one more time.
2. Look through the results at the bottom and copy the id for the **"Sales and Marketing"** group:
`52987f91-5a61-4c25-8a22-c55ce1b446d6`

### **Step 2: Check the new team's members**

1. Click on **"channels of a team which I am a member of"** in the left menu.
2. Replace the default team-id in the URL with the one you just copied.
3. Click **Run query**.
*You will now see the channels in the Sales and Marketing team!*

> 💡 **How does it know which team to query?**
> Look at the URL in the address bar. After `/teams/`, there is a specific **team id**. We can replace this ID to target completely different teams!

## 📜 Wrap-Up: Documentation

To review the documentation for each endpoint, click on the 📂 icon to the right side of the endpoint
*Those with a little 🔓 icon are the ones that require authentication, mostly those that go beyond just reading data from the graph.*

## 📥 Wrap-Up: Documentation

And lastly, just like in the powershell lab, if we click on ‘history’ we will be able to review the previous commands that were executed.
