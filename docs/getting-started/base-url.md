---
sidebar_position: 2
---

# Base URL

The base URL for the UUID.church API is:

```
https://api.uuid.church
```

All API requests should be made to this URL.

For example, to create an axios instance with the base URL:

```javascript
import axios from 'axios';

const uuidChurch = axios.create({
  baseURL: 'https://api.uuid.church',
  headers: {
    'Authorization': 'Bearer YOUR_API_KEY'
  }
});
```