## Russian Federation Aircraft Database

This database contains information about civil aircraft registered in the Russian Federation

### Requirements
* sqlite3

## Database structure

| Column | Type | Description                                | Example  |
|--------|------|--------------------------------------------|----------|
| ```icao_24bit_address```  | TEXT | The ICAO 24-bit address of the aircraft.   | 151FD1   |
|  ```registration```   | TEXT UNIQUE| The registration of the aircraft.    | RA-73681 |
|  ```aircraft_type```| TEXT | The type of the aircraft, as an ICAO code. |  A319    |
|```model```| TEXT | The model of the aircraft.                 |Airbus A319-114|
|```serial_number```| TEXT| The manufacturer serial number of the aircraft.|2618|
|```airline```  | TEXT | The name of the airline.                   |S7 Airlines|
|```operator```   | TEXT | The airline which operates the aircraft.   |Citrus|
|```airline_code```| TEXT | The IATA/ICAO code of the airline. |S7 / SBI|
|```operator_code```| TEXT| The IATA/ICAO code of the operator. |XT / CTU|
|```timestamp```| TEXT | Date the record was added to the database.|2023-08-13 09:12:03|         


## How to use

Open the database with ```sqlite3 aircraft.db``` and run the query:

```
sqlite> SELECT * FROM aircraftdb WHERE icao_24bit_address ='141ED9';
141ED9|RA-07897|AEST|Piper Aerostar 601P|61P07958063407|Private owner|-|-|-|2023-08-20 16:45:59
```
```
sqlite> SELECT * FROM aircraftdb WHERE airline LIKE 'Abakan%';
152A52|RA-76370|IL76|Ilyushin Il-76MD|1033414458|Abakan Air|Abakan Air|S5 / NKP|S5 / NKP|2023-08-13 09:43:38
152AA9|RA-76457|IL76|Ilyushin Il-76T|93421621|Abakan Air|Abakan Air|S5 / NKP|S5 / NKP|2023-08-13 09:45:08
152AAF|RA-76463|IL76|Ilyushin Il-76TD|53464934|Abakan Air|Abakan Air|S5 / NKP|S5 / NKP|2023-08-13 09:45:15
152ABC|RA-76476|IL76|Ilyushin Il-76TD|43451528|Abakan Air|Abakan Air|S5 / NKP|S5 / NKP|2023-08-13 09:45:18
152AC9|RA-76489|IL76|Ilyushin Il-76TD|-|Abakan Air|Abakan Air|S5 / NKP|S5 / NKP|2023-08-13 09:45:25
```
```
sqlite> SELECT * FROM aircraftdb WHERE registration LIKE 'RA-8915%';
155C42|RA-89154|SU95|Sukhoi Superjet 100-95LR|95122|Red Wings|Red Wings|WZ / RWZ|WZ / RWZ|2023-08-13 10:43:01
155C43|RA-89155|SU95|Sukhoi Superjet 100-95LR|95164|Red Wings|Red Wings|WZ / RWZ|WZ / RWZ|2023-08-13 10:43:04
155C44|RA-89156|SU95|Sukhoi Superjet 100-95LR|95168|Red Wings|Red Wings|WZ / RWZ|WZ / RWZ|2023-08-13 10:43:08
155C45|RA-89157|SU95|Sukhoi Superjet 100-95LR|95170|Red Wings|Red Wings|WZ / RWZ|WZ / RWZ|2023-08-13 10:44:13
155C46|RA-89158|SU95|Sukhoi Superjet 100-95LR|95171|Red Wings|Red Wings|WZ / RWZ|WZ / RWZ|2023-08-13 10:44:16
```
## Disclaimer
The data is provided without any form of guarantee regarding its accuracy or correctness. The data should not be used for any purposes where the safety of persons or property would be put at risk.