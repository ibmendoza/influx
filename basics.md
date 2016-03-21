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
| NULL          | N/A             | null is not stored |
| column name   | field/tag key   |    |
| column value  | field/tag value |    |

