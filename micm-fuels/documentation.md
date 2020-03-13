## MICM Fuels Prices - Usage
### /fuels
###### Allowed HTTP requests: **GET**

**ENDPOINT**

`https://api.indexa.do/api/fuels`

**Authentication**
For this API usage you must pass a token for authentication. A token is a tool which allow us to obtain usage metrics and security features in order to keep this service up and running.

**How do you pass your token?**

Just include `{'x-access-token': '<your_token>'} ` in your request headers.

**How do I get my token?**

You can obtain a **free tier token** in the API gallery by selecting an API and creating an application to suscribe the API.

For **standard and premium tier** you must request a subscription which is subject to approval after you contact INDEXA team and submit your payment.

## FREE TIER 

**QUERY PARAMETERS RESTRICTIONS**

| QUERY PARAMETER | VALID OPTIONS  | QUERY SAMPLE |
| --- | --- | --- |
| name | all fuels | `https://api.indexa.do/api/fuels?name=GasolinaPremium`|

### **Sample Response**

```
{
   "status": "success",
   "data": [
      {
        
      }
   ]
}
```

## STANDARD TIER

**QUERY PARAMETERS RESTRICTIONS**

DATE FORMAT: YYYY-MM-DD

| QUERY PARAMETER | VALID OPTIONS  | QUERY SAMPLE |
| --- | --- | --- |
| name | all fuels | `https://api.indexa.do/api/fuels?name=GasolinaPremium`|
| date | any date within current month | `https://api.indexa.do/api/fuels?date=2020-03-09`|
| date_from | any date within current month | `https://api.indexa.do/api/fuels?date_from=2020-03-09`|
| date_to | any date within current month | `https://api.indexa.do/api/fuels?date_from=2020-03-09&date_to=2020-03-11`|

### **Sample Response**

```
{
   "status": "success",
   "data": [
     
   ]
}
```

## PREMIUM TIER

**QUERY PARAMETERS RESTRICTIONS**

DATE FORMAT: YYYY-MM-DD

| QUERY PARAMETER | VALID OPTIONS  | QUERY SAMPLE |
| --- | --- | --- |
| date | any date within current year | `https://api.indexa.do/api/fuels?date=2020-03-09`|
| date_from | any date within current year | `https://api.indexa.do/api/fuels?date_from=2020-03-09`|
| date_to | any date within current month | `https://api.indexa.do/api/fuels?date_from=2020-01-01&date_to=2020-03-09`|

### **Sample Response**

```
{
   "status": "success",
   "data": [
   
    ]
 }
```

