# Ride Requests

## Make a ride request


> The above command returns JSON structured like this:

```json
{
	"status": "success",
	"message": "request to join ride successful"
}
```

This endpoint makes a request to an available ride offer.

<aside class="warning">You can only access this endpoint if you provide a token in the <code>Authorization</code> Header of your request.</aside>

### HTTP Request

* Method: `POST`
* Endpoint: `${baseUrl}/rides/<:rideId>/requests`

### URL Parameters

Parameter | Description
--------- | -----------
rideId    | The ID of the ride offer to retrieve

### HTTP Response

* statusCode: `201 - OK`
* Body: `application/json`

## Get all Ride requests


> The above command returns JSON structured like this:

```json
{
	"status": "success",
	"requests": [
		{
			"requestId": 5,
			"requesterId": 2,
			"rideId": 1,
			"creatorId": 1,
			"offerStatus": "pending",
			"requesterName": "John Doe",
			"createdAt": "2018-07-10T16:01:33.955Z",
			"updatedAt": "2018-07-10T16:01:33.955Z"
		},
		{
			"requestId": 7,
			"requesterId": 3,
			"rideId": 1,
			"creatorId": 1,
			"offerStatus": "accepted",
			"requesterName": "Jude Abaga",
			"createdAt": "2018-07-10T16:01:33.955Z",
			"updatedAt": "2018-07-10T16:01:40.295Z"
		},
		{
			"requestId": 16,
			"requesterId": 4,
			"rideId": 1,
			"creatorId": 1,
			"offerStatus": "pending",
			"requesterName": "Christopher Chance",
			"createdAt": "2018-07-11T15:02:09.714Z",
			"updatedAt": "2018-07-11T15:02:09.714Z"
		}
	]
}
```

This endpoint helps the creator of the ride offer to see the responses so far. All the requests
returned are only for the particular ride offer and ride creator.


<aside class="warning">You can only access this endpoint if you provide a token in the <code>Authorization</code> Header of your request.</aside>

### HTTP Request

* Method: `GET`
* Endpoint: `${baseUrl}/rides/<:rideId>/requests`

### URL Parameters

Parameter | Description
--------- | -----------
rideId    | The ID of the ride offer to retrieve

### HTTP Response

* statusCode: `200 - OK`
* Body: `application/json`

## Respond to a Ride request

> Request body:

```json
{
  "status": "accept"
}
```

> The above command returns JSON structured like this:

```json
{
	"status": "success",
	"message": "Successfully accepted ride request"
}
```

This endpoint helps the creator of a ride offer accept or reject requests for that offer.

<aside class="warning">You can only access this endpoint if you provide a token in the <code>Authorization</code> Header of your request.</aside>

### HTTP Request

* Method: `PUT`
* Endpoint: `${baseUrl}/rides/<:rideId>/requests/<:requestId>`
* Body: `application/json`

<aside class="notice">The <code>status</code> of the request body can have either "accept" or "reject" as it's value.</aside>

### URL Parameters

Parameter | Description
--------- | -----------
rideId    | The ID of the ride offer
requestId | The ID of the ride request to respond to

### HTTP Response

* statusCode: `200 - OK`
* Body: `application/json`
