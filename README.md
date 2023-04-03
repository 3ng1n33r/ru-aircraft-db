## Russian Federation Aircraft Database

This database contains information about civil aircraft registered in the Russian Federation

### Requirements
* sqlite3

## Database structure

| Column | Type | Description                                | Example  |
|--------|------|--------------------------------------------|----------|
|  icao  | TEXT | The ICAO 24-bit address of the aircraft.   | 14660A   |
|  reg   | TEXT UNIQUE| The registration of the aircraft.    | RA-26122 |
|  typeac| TEXT | The type of the aircraft, as an ICAO code. |  AN26    |
|aircraft| TEXT | The model of the aircraft.                 |Antonov An-26B-100|
|airline | TEXT | The name of the airline.                   |Petropavlovsk-Kamchatsky Air|
|oper    | TEXT | The airline which operates the aircraft.   |Petropavlovsk-Kamchatsky Air|
|timestamp| TEXT | Date the record was added to the database.|2022-10-24 14:01:55|         


## How to use

Open the database with ```sqlite3 aircraft.db``` and run the query:

```
sqlite> SELECT * FROM aircraftdb WHERE icao ='15065F';
15065F|RA-67167|CL60|Bombardier Challenger 604|Private owner|-|2022-10-25 10:03:10
```
```
sqlite> SELECT * FROM aircraftdb WHERE airline LIKE 'Abakan%';
152ABC|RA-76476|IL76|Ilyushin Il-76TD|Abakan Air|Abakan Air|2022-12-02 23:04:06
152AA9|RA-76457|IL76|Ilyushin Il-76T|Abakan Air|-|2020-09-27 09:03:20
152BEC|RA-76780|IL76|Ilyushin Il-76T|Abakan Air|-|2020-09-27 09:05:39
152AAF|RA-76463|IL76|Ilyushin Il-76TD|Abakan Air|Abakan Air|2023-01-16 21:16:02
```
```
sqlite> SELECT * FROM aircraftdb WHERE reg LIKE 'RA-8915%';
155C43|RA-89155|SU95|Sukhoi Superjet 100-95B|Red Wings|Red Wings|2022-10-25 09:59:16
155C44|RA-89156|SU95|Sukhoi Superjet 100-95B|Red Wings|Red Wings|2022-10-25 10:03:44
155C45|RA-89157|SU95|Sukhoi Superjet 100-95B|Red Wings|Red Wings|2022-10-25 10:03:48
155C46|RA-89158|SU95|Sukhoi Superjet 100-95B|Red Wings|Red Wings|2022-10-25 10:04:53
155C42|RA-89154|SU95|Sukhoi Superjet 100-95B|Red Wings|Red Wings|2022-06-18 09:54:36
```
## Disclaimer
The data is provided without any form of guarantee regarding its accuracy or correctness. The data should not be used for any purposes where the safety of persons or property would be put at risk.