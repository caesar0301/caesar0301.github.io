---
title: Python Programs with External Modules to Spark
date: 2015-11-22
comments: true
tags:
    - Spark
    - Python
---

It is a common scenario that we need external modules in a PySpark program. Three alternatives could be employed here:

1. Distribute the third-party modules across your spark cluster. This is the easiest way, but needs the administrative right of the cluster;
2. Write your own functions in a single module and append it to the search path of SparkContext. Two utility functions are available: PySpark [sc.addFile](http://spark.apache.org/docs/latest/api/python/pyspark.html#pyspark.SparkContext.addFile) and [sc.addPyFile](http://spark.apache.org/docs/latest/api/python/pyspark.html#pyspark.SparkContext.addPyFile).
3. Package the module with multiple python files into a single .zip or .egg file. Refer to these answers elsewhere:

## References

* [How to create a zip archive of a directory](http://stackoverflow.com/questions/1855095/how-to-create-a-zip-archive-of-a-directory/)
* [Loading Python libraries into Spark](http://apache-spark-user-list.1001560.n3.nabble.com/Loading-Python-libraries-into-Spark-td7059.html)