---
sidebar_position: 1
---

# About

UUID.church was started by [CHURCH.tech](https://church.tech) as an open source project to provide unique identifiers for each church to make it easier for church products to integrate with each other.

## Why UUIDs?

UUIDs are a great way to uniquely identify things. They are universally unique, meaning that no two UUIDs will ever be the same. This makes them perfect for identifying churches, as there are many churches with the same name.

## How does it work?

UUID.church generates a UUID for each church based on the church's name and location. This UUID is then stored in a database, and can be retrieved by anyone who knows the church's name and city/state. This makes it easy for church products to integrate with each other, as they can use the UUID to identify the church.

Vector embeddings are created for each church name and location, and then exposed by a REST API to allow for easy searching and retrieval of UUIDs. This open source project outlines the process used to generate these embeddings and the weightings used to perform the cosine similarity search.
