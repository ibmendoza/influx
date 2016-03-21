### InfluxDB Basics

Source: InfluxData Documentation

<img src="https://itjumpstart.files.wordpress.com/2016/03/influxdb.png">

**Relational to Time Series Analogy**

| Relational    | Time Series   | Notes                |
| ------------- |:-------------:| --------------------:|
| table         | measurement   | census               |
| primary index | time          | RFC3339 UTC          |
| column        | field         | not indexed          |
| column        | tag           | indexed metadata     |
| NULL          | N/A           | null is not stored |
| column name   | field key     | Ex. butterflies, honeybees   |
| column name   | tag key       | Ex. location, scientist   |
| column value  | field value   | Ex. 3 for butterflies           |
| column value  | tag value     | Ex. 1 for location, perpetual for scientist |
| row           | fieldset     | Ex. butterflies = 12 honeybees = 23 |

In the above example, there are 8 rows or field sets


