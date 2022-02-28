---
title: "List business calendarView"
description: "Get the collection of bookingAppointment objects for a bookingBusiness, that occurs in the specified date range."
ms.localizationpriority: medium
author: "arvindmicrosoft"
ms.prod: "bookings"
doc_type: apiPageType
---

# List business calendarView

Namespace: microsoft.graph

Get the collection of [bookingAppointment](../resources/bookingappointment.md) objects for a [bookingBusiness](../resources/bookingbusiness.md), that occurs in the specified date range.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) |  Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All   |
|Delegated (personal Microsoft account) | Not supported.   |
|Application | Not supported.  |

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /solutions/bookingBusinesses/{id}/calendarView?start={start-value}&end={end-value}
```

## Query parameters

In the request URL, provide the following required query parameters with values.

| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|end|DateTimeOffset|The end date and time of a time range, represented in ISO 8601 format, as UTC or an offset from UTC. For example, 3am UTC on Jan 1, 2018 would look like this: '2018-01-01T03:00:00Z', and the same time in PST would look like this: '2017-12-31T19:00:00-08:00'.|
|start|DateTimeOffset|The start date and time of a time range, represented in ISO 8601 format, as UTC or an offset from UTC. For example, midnight UTC on Jan 1, 2018 would look like this: '2018-01-01T00:00:00Z', and the same time in PST would look like this: '2017-12-31T16:00:00-08:00'.|

The values of `start` and `end` are interpreted using the timezone offset specified in their corresponding values and are not impacted by the value of the `Prefer: outlook.timezone` header if present.

This method also supports some of the $count and $expand [OData query parameters](/graph/query-parameters) to help customize the response.

## Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer {code}|

## Request body
Do not supply a request body for this method.

## Response
If successful, this method returns a `200 OK` response code and a collection of [bookingAppointment](../resources/bookingappointment.md) objects in the response body.

## Example

### Request
The following is an example of the request.

<!-- {
  "blockType": "request"
}-->
```http
GET https://graph.microsoft.com/v1.0/solutions/bookingBusinesses/Contosolunchdelivery@contoso.onmicrosoft.com/calendarView?start=2022-02-06T00:00:00Z&end=2022-02-10T00:00:00Z
```

### Response
The following is an example of the response. 

>**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingAppointment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#solutions/bookingBusinesses('Contosolunchdelivery%40contoso.onmicrosoft.com')/calendarView",
    "value": [
        {
            "id": "AAMkADKpAAA=",
            "selfServiceAppointmentId": "00000000-0000-0000-0000-000000000000",
            "additionalInformation": "",
            "isLocationOnline": false,
            "joinWebUrl": null,
            "customerTimeZone": null,
            "serviceId": "d1e3db10-e679-4aac-aad4-1a6dccc77777",
            "serviceName": "Catered bento",
            "duration": "PT1H",
            "preBuffer": "PT0S",
            "postBuffer": "PT0S",
            "priceType": "FixedPrice",
            "price": 10,
            "serviceNotes": null,
            "optOutOfCustomerEmail": false,
            "staffMemberIds": [
                "da52457d-a74d-4df1-a190-225fe1dffrr4"
            ],
            "smsNotificationsEnabled": false,
            "maximumAttendeesCount": 1,
            "filledAttendeesCount": 1,
            "startDateTime": {
                "dateTime": "2022-02-08T14:30:00-06:00",
                "timeZone": "America/Chicago"
            },
            "endDateTime": {
                "dateTime": "2022-02-08T15:30:00-06:00",
                "timeZone": "America/Chicago"
            },
            "serviceLocation": {
                "displayName": "Customer location (123 First Avenue, Buffalo, NY 98052, USA)",
                "locationEmailAddress": null,
                "locationUri": "",
                "locationType": null,
                "uniqueId": null,
                "uniqueIdType": null,
                "address": {
                    "street": "",
                    "city": "",
                    "state": "",
                    "countryOrRegion": "",
                    "postalCode": ""
                },
                "coordinates": {
                    "altitude": null,
                    "latitude": null,
                    "longitude": null,
                    "accuracy": null,
                    "altitudeAccuracy": null
                }
            },
            "reminders": [],
            "customers": []
        },
        {
            "id": "AAMkADKnAAA=",
            "selfServiceAppointmentId": "00000000-0000-0000-0000-000000000000",
            "additionalInformation": "",
            "isLocationOnline": false,
            "joinWebUrl": null,
            "customerTimeZone": null,
            "serviceId": "d1e3db10-e679-4aac-aad4-1a6dccc77777",
            "serviceName": "Catered bento",
            "duration": "PT1H",
            "preBuffer": "PT0S",
            "postBuffer": "PT0S",
            "priceType": "FixedPrice",
            "price": 10,
            "serviceNotes": null,
            "optOutOfCustomerEmail": false,
            "staffMemberIds": [
                "1707ec9b-8028-49bd-88a7-2096781ccec"
            ],
            "smsNotificationsEnabled": false,
            "maximumAttendeesCount": 1,
            "filledAttendeesCount": 1,
            "startDateTime": {
                "dateTime": "2022-02-09T14:30:00-06:00",
                "timeZone": "America/Chicago"
            },
            "endDateTime": {
                "dateTime": "2022-02-09T15:30:00-06:00",
                "timeZone": "America/Chicago"
            },
            "serviceLocation": {
                "displayName": "Customer location (876 Tenth Avenue, Buffalo, NY 98052, USA)",
                "locationEmailAddress": null,
                "locationUri": "",
                "locationType": null,
                "uniqueId": null,
                "uniqueIdType": null,
                "address": {
                    "street": "",
                    "city": "",
                    "state": "",
                    "countryOrRegion": "",
                    "postalCode": ""
                },
                "coordinates": {
                    "altitude": null,
                    "latitude": null,
                    "longitude": null,
                    "accuracy": null,
                    "altitudeAccuracy": null
                }
            },
            "reminders": [],
            "customers": []
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "bookingBusiness: getCalendarView",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
