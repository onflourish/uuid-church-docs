---
sidebar_position: 1
---

# Authorization

In order to use the UUID.church API, you will need to obtain an API key for the main database. Even though this is an open source project and the code is available for anyone to use, we need to ensure that the database is not overloaded with requests. By requiring an API key, we can monitor usage and ensure that the database remains responsive for everyone.

## Obtaining an API Key

To obtain an API key, you will need to contact [matt@church.tech](mailto://matt@church.tech) and request one. Once you have received your API key, you can use it to authenticate your requests to the API.

## Authenticating Requests

To authenticate your requests to the API, you will need to include your API key in the `Authorization` header of your HTTP requests. The value of the `Authorization` header should be `Bearer <API_KEY>`, where `<API_KEY>` is your API key.