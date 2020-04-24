## NCF Validation - Usage

### /validate-ncf

###### Allowed HTTP requests: **GET**

**ENDPOINT**

`https://api.indexa.do/api/validate-ncf`

**Authentication**
For this API usage you must pass a token for authentication. A token is a tool which allow us to obtain usage metrics and security features in order to keep this service up and running.

**How do you pass your token?**

Just include `{'x-access-token': '<your_token>'}` in your request headers.

**How do I get my token?**

You can obtain a **free tier token** in the API gallery by selecting an API and creating an application to suscribe the API.

## FREE TIER

**QUERY PARAMETERS RESTRICTIONS**

| QUERY PARAMETERS | QUERY SAMPLE                                                           |
| ---------------- | ---------------------------------------------------------------------- |
| ncf, rnc         | `https://api.indexa.do/api/validate-ncf?ncf=B0100000005&rnc=130216748` |

### **Sample Response**

```
{
   "status": "success",
   "message": "according to DGII, this NCF is not valid for this RNC.",
   "valid": false
}
```

**ERROR RESPONSE**

### **Sample Response**

```
{
   "status": "error",
   "message": "You submitted a 'ncf' with invalid format"
}
```
