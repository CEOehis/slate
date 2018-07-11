# Ride Offers

## Get all Ride Offers


> The above command returns JSON structured like this:

```json
{
	"status": "success",
	"rides": [
		{
			"rideId": 1,
			"origin": "Some place from where the journey will begin",
			"destination": "The place where we will to go",
			"departureDate": "2018-07-09T23:00:00.000Z",
			"departureTime": "11:11:00+00",
			"seats": 3,
			"rideCreator": "John Doe",
			"createdAt": "2018-07-10T04:14:29.717Z",
			"updatedAt": "2018-07-10T04:14:29.717Z"
		},
		{
			"rideId": 1,
			"origin": "Another place from where the journey will begin",
			"destination": "Some other place where we will to go",
			"departureDate": "2018-07-09T23:00:00.000Z",
			"departureTime": "11:11:00+00",
			"seats": 3,
			"rideCreator": "Jane Doe",
			"createdAt": "2018-07-10T04:14:29.717Z",
			"updatedAt": "2018-07-10T04:14:29.717Z"
		}
	]
}
```

This endpoint fetches and returns all available ride offers.

<aside class="warning">You can only access this endpoint if you provide a token in the <code>Authorization</code> Header of your request.</aside>

### HTTP Request

* Method: `GET`
* Endpoint: `${baseUrl}/rides`

### HTTP Response

* statusCode: `200 - OK`
* Body: `application/json`

## Get a specific Ride Offers


> The above command returns JSON structured like this:

```json
{
	"status": "success",
	"ride": {
		"rideId": 1,
		"origin": "Some place from where the journey will begin",
		"destination": "The place where we will to go",
		"departureDate": "2018-07-09T23:00:00.000Z",
		"departureTime": "11:11:00+00",
		"seats": 3,
		"rideCreator": "John Doe",
		"phone": null,
		"email": "jd@mail.com",
		"createdAt": "2018-07-10T04:14:29.717Z",
		"updatedAt": "2018-07-10T04:14:29.717Z"
	}
}
```

This endpoint fetches and returns a specific ride offer.

<aside class="warning">You can only access this endpoint if you provide a token in the <code>Authorization</code> Header of your request.</aside>

### HTTP Request

* Method: `GET`
* Endpoint: `${baseUrl}/rides/<:rideId>`

### URL Parameters

Parameter | Description
--------- | -----------
rideId    | The ID of the ride offer to retrieve

### HTTP Response

* statusCode: `200 - OK`
* Body: `application/json`

## Create a Ride Offer

> Request body:

```json
{
  "origin": "Some ride origin",
  "destination": "Where we are headed",
  "date": "2018-07-09",
  "time": "11:30",
  "seats": 2,
}
```

> The above command returns JSON structured like this:

```json
{
	"status": "success",
	"ride": {
		"origin": "Some ride origin",
		"destination": "Where we are headed",
		"departureDate": "2018-07-09T23:00:00.000Z",
		"departureTime": "11:30:00+00",
		"seats": 2,
		"userId": 1
	}
}
```

This endpoint creates a new ride offer.

<aside class="warning">You can only access this endpoint if you provide a token in the <code>Authorization</code> Header of your request.</aside>

### HTTP Request

* Method: `POST`
* Endpoint: `${baseUrl}/rides`
* Body: `application/json`

### HTTP Response

* statusCode: `201 - Created`
* Body: `application/json`
