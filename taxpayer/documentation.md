## DGII Taxpayer Information - Usage
### /rnc
###### Allowed HTTP requests: *GET*

**ENDPOINT**

`https://api.indexa.do/api/rnc`

**Authentication**
For this API usage you must pass a token for authentication. A token is a tool which allow us to obtain usage metrics and security features in order to keep this service up and running.

**How do you pass your token?**

Just include `{'x-access-token': '<your_token>'} ` in your request headers.

**How do I get my token?**

You can obtain a **free tier token** in the API gallery by selecting an API and creating an application to suscribe the API.

For **standard and premium tier** you must request a subscription which is subject to approval after you contact INDEXA team and submit your payment.

## FREE TIER 

**THERE ARE NO QUERY PARAMETERS RESTRICTIONS**

### **Sample Response**

```
{
   "status": "success",
   "data": [
      {
         "rnc": "131793916",
         "business_name": "INDEXA SRL",
         "state": "ACTIVO"
      }
   ]
}
```

## STANDARD TIER

**THERE ARE NO QUERY PARAMETERS RESTRICTIONS**

### **Sample Response**

```
{
   "status": "success",
   "data": [
      {
         "rnc": "131793916",
         "business_name": "INDEXA SRL",
         "tradename": "INDEXA",
         "state": "ACTIVO",
         "payment_regime": "NORMAL",
         "sector": "LOS RESTAURADORES",
         "street": "4",
         "street_number": "18"
      }
   ]
}
```

## PREMIUM TIER

**THERE ARE NO QUERY PARAMETERS RESTRICTIONS**

### **Sample Response**

```
{
   "status": "success",
   "data": [
      {
         "rnc": "131793916",
         "business_name": "INDEXA SRL",
         "tradename": "INDEXA",
         "economic_activity": "VENTA AL POR MAYOR DE SOFTWARE",
         "state": "ACTIVO",
         "payment_regime": "NORMAL",
         "constitution_date": "2018-07-20",
         "sector": "LOS RESTAURADORES",
         "street": "4",
         "street_number": "18"
      }
   ]
}
```
