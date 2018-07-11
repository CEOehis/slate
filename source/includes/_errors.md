# Errors

The RideMyWay API uses the following error codes:


Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request is invalid.
401 | Unauthorized -- Your token or user password is wrong.
403 | Forbidden -- The requested resource is for a different user.
404 | Not Found -- The specified resource could not be found.
409 | Conflict -- The resource being created is a possible duplicate.
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
