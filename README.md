# HelloID-Task-SA-Source-AzureActiveDirectory-AccountSearch

## Prerequisites
- [ ] This script uses the Microsoft Graph API and requires an App Registration with App permissions:
  - [ ] Read all user’s full profiles by using <b><i>User.Read.All</i></b>

## Description

This code snippet executes the following tasks:

1. Define a wildcard search query `$searchQuery` based on the search parameter `$datasource.searchUser`
2. Creates a token to connect to the Graph API.
3. List all users in Azure AD using the API call: [List users](https://learn.microsoft.com/en-us/graph/api/user-list?view=graph-rest-1.0&tabs=http)
4. Filter down to only users with `$searchQuery` in their `displayName` or `userPrincipalName`
5. Return a hash table for each user account using the `Write-Output` cmdlet.

> To view an example of the data source output, please refer to the JSON code pasted below.

```json
{
    "searchUser": "James"
}
```