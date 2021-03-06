

# DELETE /Customer/{CustNo}/Card

#### Description

- Requires API Key: Yes
- Requires System Administrator: No
- Requires Counterpoint Registration option: Yes
- Requires Company Administrator: Yes

#### Sample Request

**URI**

`DELETE https://localhost:81/Customer/{CustNo}/CARD?CardSeqNo={CardSeqNo}`

**Headers**
- `Authorization : Basic UUFUZXN0R29sZi5NR1I6cGFzc3dvcmQx`
- `Accept : application/json`

#### Parameters
Name | Parameter Type | Data Type | Required | Description
---- | -------------- | --------- | -------- | -----------
custNo | path | string | true | The CUST_NO of the customer to delete.
CardSeqNo | query | string | true | The AR_CUST_CARD.CARD_SEQ_NO of the card to delete.

#### Response Codes
- **<code>200 OK</code>** The request was successful, the result of the call will be in the response body.
- **<code>401 Unauthorized</code>** The request could not be fulfilled. Likely due to a missing or invalid authorization header.
- **<code>404 Not Found</code>** The role name provided was not found for this company.
- **<code>500 Internal Server Error</code>** The request could not be fulfilled due to an unexpected internal error. This could be caused by a bug in the system, an unavailable database, or any other unexpected internal problem processing the request.
 
#### Error Codes
The following error codes may be returned from requests to this endpoint:
- `SUCCESS`: The role provided was successfully deleted.

#### Sample Response Body

```
{
  "CUST_NO": "1000",
  "reference": "Customer",
  "Link": {
    "uri": "https://wusmj185111-t75:52000/CUSTOMER/1000",
    "method": "get"
  },
  "ErrorCode": "SUCCESS"
}
```

#### Response Body
