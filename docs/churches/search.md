---
sidebar_position: 1
---

# Search

Search for a church based on name, city, and state with other optional parameters for more accurate results.

## Path

Make a GET request to

```
/church
```

## Parameters

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string | The name of the church | Yes |
| city | string | The city where the church is located | Yes |
| state | string | The state where the church is located (i.e. KY, NY, CA) | Yes |
| street | string | The street address of the church | No |
| zip | string | The zip code of the church | No |
| website | string | The website of the church (not all churches have a website in the database) | No |

## Example

```
GET /church?name=Southeast%Christian%20Church&city=Louisville&state=KY
```

## Response

The response will be a JSON object with the following fields:

| Name | Type | Description |
| ---- | ---- | ----------- |
| uuid | string | The UUID of the church (returns `null` if no match is found) |
| name | string | The name of the church |
| city | string | The city where the church is located |
| state | string | The state where the church is located |
| street | string | The street address of the church |
| zip | string | The zip code of the church |
| website | string | The website of the church (returns `null` if no website is found) |

Example response:

```json
{
  "uuid": "00000000-0000-0000-0000-000000000000",
  "name": "SOUTHEAST CHRISTIAN CHURCH OF JEFFERSON COUNTY KENTUCKY INC",
  "city": "LOUISVILLE",
  "state": "KY",
  "street": "920 BLANKENBAKER PKWY",
  "zip": "40243-1845",
  "website": "https://southeastchristian.org/"
}
```

## How it works

The search endpoint uses a cosine similarity search to find the church that most closely matches the input parameters. The search is based on the church's name, city, and state, and can be refined by providing additional parameters such as street address, zip code, and website. The search algorithm uses vector embeddings to represent each church, and calculates the cosine similarity between the input parameters and the embeddings to find the best match. The search results are then sent as a separate request to a LLM to determine if any of the similarity results actually match the given input parameters. If a match is found, the church's UUID is returned along with other information about the church. If no match is found, the response will contain a uuid of `null`. 

