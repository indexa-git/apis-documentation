## Dominican Currency Rates - Usage

### /rates

###### Allowed HTTP requests: **GET**

**ENDPOINT**

`https://api.indexa.do/api/rates`

**Authentication**
For this API usage you must pass a token for authentication. A token is a tool which allow us to obtain usage metrics and security features in order to keep this service up and running.

**How do you pass your token?**

Just include `{'x-access-token': '<your_token>'}` in your request headers.

**How do I get my token?**

You can obtain a **free tier token** in the API gallery by selecting an API and creating an application to suscribe the API.

For **standard and premium tier** you must request a subscription which is subject to approval after you contact INDEXA team and submit your payment.

**AVALIABLE BANKS**

| BANK NAME                | BANK CODE | BUY RATE NAME                                                                       | SELL RATE NAME                                                                           |
| ------------------------ | --------- | ----------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| Banco Popular Dominicano | bpd       | dollarbuyrate, eurobuyrate                                                          | dollarsellrate, eurosellrate                                                             |
| Banco de Reservas        | bnr       | dollarbuyrate, eurobuyrate                                                          | dollarsellrate, eurosellrate                                                             |
| Scotia Bank              | bns       | dollarbuyrate, eurobuyrate, cdollarbuyrate                                          | dollarsellrate, eurosellrate, cdollarsellrate                                            |
| Banco Santa Cruz         | bsc       | dollarbuyrate, eurobuyrate, swissfrancbuyrate, poundsterlingbuyrate, cdollarbuyrate | dollarsellrate, eurosellrate, swissfrancsellrate, poundsterlingsellrate, cdollarsellrate |
| Banco BDI                | bdi       | dollarbuyrate, eurobuyrate                                                          | dollarsellrate, eurosellrate                                                             |
| Banco Central de RD      | bcd       | dollarbuyrate                                                                       | dollarsellrate                                                                           |
| Banco Promerica          | bpm       | dollarbuyrate, eurobuyrate                                                          | dollarsellrate, eurosellrate                                                             |
| Banco Vimenca            | bvm       | dollarbuyrate, eurobuyrate                                                          | dollarsellrate, eurosellrate                                                             |

## FREE TIER

**QUERY PARAMETERS RESTRICTIONS**

| QUERY PARAMETER | VALID OPTIONS | QUERY SAMPLE                               |
| --------------- | ------------- | ------------------------------------------ |
| bank            | bpd, bcd      | `https://api.indexa.do/api/rates?bank=bpd` |

### **Sample Response**

```
{
   "status": "success",
   "data": [
      {
         "bank": "bpd",
         "rate": 53.63,
         "date": "2020-03-09",
         "name": "dollarsellrate"
      }
   ]
}
```

## STANDARD TIER

**QUERY PARAMETERS RESTRICTIONS**

DATE FORMAT: YYYY-MM-DD

| QUERY PARAMETER | VALID OPTIONS                                            | QUERY SAMPLE                                                                       |
| --------------- | -------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| bank            | all banks                                                | `https://api.indexa.do/api/rates?bank=bpd`                                         |
| name            | dollarsellrate, dollarbuyrate, eurosellrate, eurobuyrate | `https://api.indexa.do/api/rates?bank=bpd&name=dollarbuyrate`                      |
| date            | any date no more than 7 days ago                         | `https://api.indexa.do/api/rates?bank=bpd&date=2020-03-09`                         |
| date_from       | any date no more than 7 days ago                         | `https://api.indexa.do/api/rates?bank=bpd&date_from=2020-03-09`                    |
| date_to         | any date no more than 7 days ago                         | `https://api.indexa.do/api/rates?bank=bpd&date_from=2020-03-09&date_to=2020-03-11` |

### **Sample Response**

```
{
   "status": "success",
   "data": [
      {
         "bank": "bpd",
         "rate": 53.63,
         "date": "2020-03-09",
         "name": "dollarbuyrate"
      },
      ...,
      {
         "bank": "bpd",
         "rate": 53.41,
         "date": "2020-03-02",
         "name": "dollarbuyrate"
      },
   ]
}
```

## PREMIUM TIER

**QUERY PARAMETERS RESTRICTIONS**

DATE FORMAT: YYYY-MM-DD

| QUERY PARAMETER | VALID OPTIONS                     | QUERY SAMPLE                                                                       |
| --------------- | --------------------------------- | ---------------------------------------------------------------------------------- |
| bank            | all banks                         | `https://api.indexa.do/api/rates?bank=bpd`                                         |
| name            | all currencies                    | `https://api.indexa.do/api/rates?bank=bsc&name=poundsterlingbuyrate`               |
| date            | any date no more than 30 days ago | `https://api.indexa.do/api/rates?bank=bpd&date=2020-02-15`                         |
| date_from       | any date no more than 30 days ago | `https://api.indexa.do/api/rates?bank=bpd&date_from=2020-03-09`                    |
| date_to         | any date no more than 30 days ago | `https://api.indexa.do/api/rates?bank=bpd&date_from=2020-02-18&date_to=2020-03-11` |

### **Sample Response**

```
{
   "status": "success",
   "data": [
      {
         "bank": "bsc",
         "rate": 67.45,
         "date": "2020-03-09",
         "name": "poundsterlingbuyrate"
      },
      ...,
       {
         "bank": "bsc",
         "rate": 67.42,
         "date": "2020-02-07",
         "name": "poundsterlingbuyrate"
      }
   ]
}
```

**Terms of Use**
Refer to this link to read the Terms of Use:
https://indexa.do/api-terms-of-use
