

# Request to Generic Order 

The objective of this request is to  .

 
### TYPE = C_GENERIC_FR_1
 
<br>
<br>
###  Structure of the `properties` section
<br>


| id         | Type     | Description |
|--------------|:-----------:|------------|
| `domain`| `string`     |Offer Domain of the the request.       |
| `requestedAt`      |  `date-time`  |The Customer installation wish date for the installation.      |
| `offer.name`      |  `string`  | Name of the offer, product or service relating to this request.       |
| `billingAccount.id`      |  `string`  | Orange Identifier of the Billing Account.       |
| `location.id`      |  `string`  | Orange Identifier of the Billing Account.       |



###  Example of a request
In this example, we will send an order included in an XLS file.

```
{
    "requestAt": "25",
    ...
}

```


###  Constraints

You can use the servicePoint.customerReference, only if it is assigned to one service. 


###  Errors

The HTTP status code is 422 for all these errors

| code         | message     | Description |
|--------------|:-----------:|------------|
| -| -    | ----  |
| -| -    | ----  |
| -| -    | ----  |
