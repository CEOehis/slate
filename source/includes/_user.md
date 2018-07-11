# User

## User signup

> Request body:

```json
{
  "email": "jd@mail.com",
  "fullName": "John Doe",
  "password": "somepassword",
  "passwordConfirm": "somepassword"
}
```

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
```

> The above command returns JSON structured like this:

```json
{
  "status": "success",
  "user": {
    "fullName": "John Doe",
    "email": "jd@mail.com",
    "phone": null
  },
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6OCwiaWF0IjoxNTMwODY1NjgyLCJleHAiOjE1MzA5NTIwODJ9.TBCD0rXVGEM5Yez5hnWGUc0VFSot3kP5eVRXdqg1PGA"
}
```

This endpoint creates a new User account and provides an authorisation token with which to access all other RideMyWay endpoints.

### HTTP Request

* Method: `POST`
* Endpoint: `${baseUrl}/users/signup`
* Body: `application/json`

### HTTP Response

* statusCode: `201 - Created`
* Body: `application/json`

## User login

> Request body:

```json
{
  "email": "jd@mail.com",
  "password": "somepassword"
}
```

> The above command returns JSON structured like this:

```json
{
  "status": "success",
  "user": {
    "fullName": "John Doe",
    "email": "jd@mail.com",
    "phone": null
  },
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6OCwiaWF0IjoxNTMwODY1NjgyLCJleHAiOjE1MzA5NTIwODJ9.TBCD0rXVGEM5Yez5hnWGUc0VFSot3kP5eVRXdqg1PGA"
}
```

This endpoint logs in a valid User account and provides an authorisation token with which to access all other RideMyWay endpoints.

### HTTP Request

* Method: `POST`
* Endpoint: `${baseUrl}/users/login`
* Body: `application/json`

### HTTP Response

* statusCode: `200 - OK`
* Body: `application/json`
