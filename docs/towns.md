# BFS Town Data
## Introduction
The “Bundesamt für Statistik” provides information on the structure of Switzerland. This prepared data set contains the geographical positions of all Swiss towns.
## Scope
Switzerland is devided into postcode regions. The Swiss **Post** internally uses a 6-digit postcode instead of the widley used 4-digit version. While most small towns have exactly one postcode, big cities like zurich can have up to 24.
The data contains one entry for each 6-digit postcode including a canton reference and the geographical position. There are 4068 regions in total.
## Files
We provide you you the data as csv file and as json file. Both versions contain the same information.
### towns.json
#### Example
```
{
  "official_name" : "Aeugst am Albis",
  "post_code4" : 8914,
  "post_code6" : 891400,
  "canton_label_short" : "ZH",
  "latitude" : 47.266998773234,
  "longitude" : 8.4883027148933
}
```