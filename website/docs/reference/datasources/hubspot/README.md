
# HubSpot


HubSpot is a **cloud-based CRM** designed to help align sales and marketing teams, promote sales enablement, increase ROI, and improve your inbound marketing strategy to produce more qualified leads. In simple words, it is a software platform created to assist your business with marketing and sales.

:::info
To integrate Hubspot with Appsmith, you should understand the [basics of connecting to databases](core-concepts/connecting-to-data-sources/) on Appsmith.
:::

Appsmith provides an easy way to integrate with HubSpot, and enables you to perform different operations using a custom UI built with minimal configurations.


# Create HubSpot Datasource

To add a HubSpot API, navigate to **Explorer** >> Click on the **+** icon (next to Datasources) >> Select **HubSpot** under APIs.

<figure>
 <object data="https://www.youtube.com/embed/h2Jp8PenbTM" width='750px' height='400px'></object>
 <figcaption align="center"><i>Create Hubspot Datasource</i></figcaption>
</figure>

<!-- <figure>
<VideoEmbed host="youtube" videoId="Dxe_NzdGzL4" /> 
</figure> -->


## Connection Settings

Configure the HubSpot API as illustrated below:

![](/img/hubspot-connection.png)



### Authentication Type
Appsmith allows you to select from the available authentication types to integrate with an Hubspot database:

#### Bearer Token 

Bearer Tokens are the predominant access token used with [OAuth 2.0](https://docs.appsmith.com/core-concepts/connecting-to-data-sources/aut}hentication/authentication-type/oauth2-authentication/).
You can authenticate to the API by providing your access token in the HTTP authorization bearer token header.

Let's see how you can fetch your Bearer Token:



<figure>
 <object data="https://www.youtube.com/embed/q1DkGLJ6JFU" width='750px' height='400px'></object>
 <figcaption align="center"><i>Fetching Access Token</i></figcaption>
</figure>


* Open [**HubSpot**](https://www.hubspot.com/products).
* You can **create a new account** or select an existing one.
* Click on the **settings** icon on top-right corner, and select integrations.
* Create a private app (or open an existing one).
* Navigate to **Scopes**.
* Allow necessary permissions for **CMS, CRM, and Settings**.
* Navigate to the auth page of your app settings.
* Here you'll be able to find the app's **client ID** and [**access token**](https://developers.hubspot.com/docs/api/oauth/tokens).


Access token will look something like this:

```js
pat-na1-217ee**-****-****-****-***
```


## Create Queries

You can add queries to the newly created HubSpot datasource in one of the below ways:


### Datasource Page
You can add queries to Hubspot datasource by selecting the **New API +** button available on the datasource page.

![](/img/hubspot-create-query-from-datasource-page.png)

### Query/JS page
By navigating to **Explorer** >> **Click plus sign** (+) next to Queries/JS >> Select the **Hubspot datasource**.


![](/img/create-hubspot-query-from-Query-JS-page.png)

## Query

You can create queries to fetch, update and delete data from a datasource using the Appsmith query editor. Hubspot integration supports the following query methods:

|                Query Name                |              Description              |
|:----------------------------------------:|:-------------------------------------:|
| HubDB - Get Published Tables             | Fetches all the published table from the database. |
| HubDB - Create Table                     | Creates a new table in the HubDB database. |
| HubDB - Get Details of a Published Table | Retrieve details of an existing table.  |
| HubDB - Archive Table                    | Archive or delete an existing table.                                 |
| HubDB - Update Existing Table            | Update a few fields in a table.                                   |
| HubDB - Clone Table                      |     Clone an existing HubDB table.                                  |
| HubDB - Export Published Version Table   |  Export table data.                                |
| HubDB - Unpublish Table                  | Unpublish table or unpublish multiple pages                                |
| HubDB - Get Table Rows                   |  Get the rows for a specific HubDB table.                                |
| HubDB - Add New Table Row                |   Add a new row to a HubDB table.                                |
| HubDB - Get Table Row                    | Get the rows for a specific HubDB table.                                       |
| HubDB - Update Existing Row              | Update a specific row in a HubDB table.                                    |
| HubDB - Replace Existing Row             | Replace a specific row in a HubDB table.                                   |
| HubDB - Permanently Delete Row           |   Delete a specific row in a HubDB table.                                    |
| HubDB - Clone Row                        |  Duplicate/clone  a specific row.                                   |
| HubDB - Get Set Rows                     |   Get set of rows from the table.                                    |
| HubDB - Permanently Delete Rows          |   Delete a set of rows from a HubDB table.                                    |
| Domains - Get Current Domains            |  Returns all existing domains that have been created.                                     |
| Domains - Get Single Domain              |  Returns a single domain with the id specified.                                     |
| URL Redirects - Get Current Redirects    |  Returns all existing URL redirects.                                     |
| URL Redirects - Create Redirect          |   Creates and configures a new URL redirect.                                    |
| URL Redirects - Get Details Redirect     |   Returns the details for a single existing URL redirect by ID.                                    |
| URL Redirects - Update Redirect          |  Updates the settings for an existing URL redirect.                                      |
| URL Redirects - Delete Redirect          |  Delete one existing redirect.                                      |
| CRM - List Objects                       |    Fetches all the object from the database. |
| CRM - Create Object                      |   Creates a new object in the database.                                    |
| CRM - Read Object                        | Retrieve a particular object. |
| CRM - Update Object                      |  Update a few fields in a object.                                       |
| CRM - Archive Object                     |  Archive or delete an existing object.                                     |
| CRM - Search Object                      | Search any object.                                      |
| CRM - GDPR Delete                        |  Deletes the record and any associations.                                     |
| Files - Import File                      | Imports CRM records into your HubSpot account.    |
| Files - Delete File                      |  Deletes the file at the specified path in the specified environment.                                     |
| Files - Get File                         |   Gets the file at the specified path in the specified environment.                                    |
| Files - Create Folder                    | Create a folder in the specified environment.                                     |
| Files - Search File                      |  Search for any file in the specified environment.                                                     |
| Files - Search Folder                    |   Search for any folder in the specified environment.                                    |
| Files - Update Folder Properties         |  Perform a partial update of a property.                                    |
| Files - Check Folder Update Status       |   Check the status of a batch file access update task.                                    |
| Files - Get Folder                       |  Get the details for a specific folder.                                     |
| Files - Delete Folder                    |   Delete a specific folder.                                    |
| Settings - Retrieve List of Users        |  Get a list of authorized users.                                   |
| Settings - Add User                      |  Add users to your hubSpot account.                                     |
| Settings - Retrieve User                 |  Retrieve an existing user.                                  |
| Settings - Modify User                   |  Update user details.                                  |
| Settings - Remove User                   |  Remove set of user.                                    |
| Settings - Retrieve Roles Account        |  View users in your HubSpot account.                                     |
| Settings - See Details Account's Teams   |  Obtain information about the team's account.                                    |


You can check the [Query Settings Guide ](https://docs.appsmith.com/core-concepts/data-access-and-binding/querying-a-database/) to learn more about queries.




## Using Queries in Applications

Once you have successfully run a Query, you can use it in your application to:

* [Display Data ](/core-concepts/data-access-and-binding/displaying-data-read/)
* [Capture Data ](/core-concepts/data-access-and-binding/capturing-data-write/capture-form-data.md)
* [Execute Queries](/core-concepts/data-access-and-binding/querying-a-database/)