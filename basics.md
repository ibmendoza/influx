### InfluxDB Basics

Source: InfluxData Documentation

<img src="https://itjumpstart.files.wordpress.com/2016/03/influxdb.png">

**Relational to Time Series Analogy**

| Relational    | Time Series   | Notes                |
| ------------- |:-------------:| :-------------------:|
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

Remember:

- Field values are your data; they can be strings, floats, integers, or booleans, and, because InfluxDB is a time series database, a field value is always associated with a timestamp. 
- time stores timestamps, and the timestamp shows the date and time, in RFC3339 UTC, associated with particular data.
- Fields are a required piece of InfluxDB’s data structure - you cannot have data in InfluxDB without fields. It’s also important to note that fields are not indexed.
- In general, fields should not contain commonly-queried metadata.
- Tags are optional. You don’t need to have tags in your data structure, but it’s generally a good idea to make use of them because, unlike fields, tags are indexed. This means that queries on tags are faster and that tags are ideal for storing commonly-queried metadata.

- Avoid table scan by storing the fields that matter to your queries as tags.

So the above example should be re-designed as follows:

<img src="https://itjumpstart.files.wordpress.com/2016/03/influxdb2.png">




