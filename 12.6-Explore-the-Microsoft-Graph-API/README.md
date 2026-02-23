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
*At the bottom of the screen, the response will list the teams that Megan is a member of.*

### 3. List Members of a Team

Now let's see who is inside a specific team.

1. Click on **"members of a team"**.
2. Click **Run query**.
*The results at the bottom will list the members of that default team.*

> 💡 **How does it know which team to query?**
> Look at the URL in the address bar. After `/groups/`, there is a specific **Team ID**. We can replace this ID to target completely different teams!

## 🔄 Modifying Queries with IDs

Let's practice swapping out that Team ID to get information about a different group.

### **Step 1: Get a new Team ID**

1. Run the **"my joined teams"** query one more time.
2. Look through the results at the bottom and copy the ID for the **"Business Development"** group:
`13be6971-79db-4f33-9d41-b25589ca25af`

### **Step 2: Check the new team's members**

1. Click on **"members of a team"** in the left menu again.
2. Replace the default Team ID in the URL with the one you just copied.
3. Click **Run query**.
*You will now see the members specific to the Business Development team!*

### **Step 3: Get Group Properties**

1. In the left menu, locate the **"groups"** sample queries.
2. Click on **"get properties and relationships of group"**.
3. If you run it as-is, it will reply with details about the "HR taskforce" team.
4. Replace the ID in the URL with our copied ID: `13be6971-79db-4f33-9d41-b25589ca25af`
5. Run the query again to see the properties of the Business Development team.

*These were just a few examples. In the official documentation, there are hundreds of API endpoints that you can query with the Graph API!*
