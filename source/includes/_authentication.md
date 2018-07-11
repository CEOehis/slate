# Authentication

> To authorize, use this code:

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.

All endpoints relating to Ride offers or requests are protected and require the use of a token to access them, in order to be able to fetch them or create them as the case may be.

This token can be gotten by [creating a user account](/#user) and must be supplied in the `Authorization` Header with subsequent requests to other RideMyWay API endpoints as follows.

`Authorization: "Bearer somerandomlygeneratedToken.WhichMustBeSentwithsubsequentrequests.inOrdertoAccessOtherEndPoints"`

Only the `users` endpoints do not require an access token.


<aside class="notice">
You must replace <code>somerandomlygeneratedToken.WhichMustBeSentwithsubsequentrequests.inOrdertoAccessOtherEndPoints</code> with your generated token.
</aside>
