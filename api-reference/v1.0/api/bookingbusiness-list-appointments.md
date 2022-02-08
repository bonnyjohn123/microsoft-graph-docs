---
title: "List appointments"
description: "Get a list of bookingAppointment objects for the specified bookingbusiness."
ms.localizationpriority: medium
author: "arvindmicrosoft"
ms.prod: "bookings"
doc_type: apiPageType
---

# List appointments

Namespace: microsoft.graph

Get a list of [bookingAppointment](../resources/bookingappointment.md) objects for the specified [bookingBusiness](../resources/bookingbusiness.md).
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
GET /solutions/bookingBusinesses/{id}/appointments
```
## Optional query parameters
This method supports the $count and $expand [OData query parameters](/graph/query-parameters) to help customize the response.

To get the set of appointments of a Microsoft Bookings business within a date range, instead of `$filter`, [get the calendarView](bookingbusiness-list-calendarview.md) for that date range.

## Request headers
| Name      |Description|
|:----------|:----------|
| Authorization  | Bearer {code}. Required.|

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
GET https://graph.microsoft.com/v1.0/solutions/bookingBusinesses/Contosolunchdelivery@contoso.onmicrosoft.com/appointments
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
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#solutions/bookingBusinesses('Contosolunchdelivery%40contoso.onmicrosoft.com')/appointments",
    "value": [
        {
            "id": "AAMkADKoAAA=",
            "selfServiceAppointmentId": "00000000-0000-0000-0000-000000000000",
            "additionalInformation": "",
            "isLocationOnline": false,
            "joinWebUrl": null,
            "customerTimeZone": null,
            "serviceId": "d1e3db10-e679-4aac-aad4-1a6dccc77371",
            "serviceName": "Initial consult",
            "duration": "PT30M",
            "preBuffer": "PT0S",
            "postBuffer": "PT0S",
            "priceType": "notSet",
            "price": 0.0,
            "serviceNotes": null,
            "optOutOfCustomerEmail": false,
            "staffMemberIds": [
                "da52457d-a74d-4df1-a190-225fe1d9b976"
            ],
            "smsNotificationsEnabled": false,
            "maximumAttendeesCount": 1,
            "filledAttendeesCount": 1,
            "startDateTime": {
                "dateTime": "2022-01-27T21:30:00-06:00",
                "timeZone": "America/Chicago"
            },
            "endDateTime": {
                "dateTime": "2022-01-27T22:00:00-06:00",
                "timeZone": "America/Chicago"
            },
            "serviceLocation": {
                "displayName": "Our office address",
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
            "serviceId": "d1e3db10-e679-4aac-aad4-1a6dccc77371",
            "serviceName": "Initial consult",
            "duration": "PT30M",
            "preBuffer": "PT0S",
            "postBuffer": "PT0S",
            "priceType": "notSet",
            "price": 0.0,
            "serviceNotes": null,
            "optOutOfCustomerEmail": false,
            "staffMemberIds": [
                "da52457d-a74d-4df1-a190-225fe1d9b976"
            ],
            "smsNotificationsEnabled": false,
            "maximumAttendeesCount": 1,
            "filledAttendeesCount": 1,
            "startDateTime": {
                "dateTime": "2022-01-27T23:00:00-06:00",
                "timeZone": "America/Chicago"
            },
            "endDateTime": {
                "dateTime": "2022-01-27T23:30:00-06:00",
                "timeZone": "America/Chicago"
            },
            "serviceLocation": {
                "displayName": "Our office address",
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
  "description": "List appointments",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
