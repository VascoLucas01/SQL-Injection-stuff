# **Lab 01 - SQL injection vulnerability in WHERE clause allowing retrieval of hidden data**

## Scenario
***
**SQL injection vulnerability** -> product category filter

**End Goal**                              -> display one or more unreleased products
***
## Analysis

### **(1)  Find if the application is vulnerable to SQL injection**

```
'
```

**Conclusion:** The quote is one of the most common used. Indeed, it breaks the query and it originates  an internal server error. So, it is vulnerable to SQLi.

### **(2) Output unrealeased products**

```
' OR 1=1 --
```

https://docs.google.com/document/d/1o26e7lw0IQAjK_cab6A3ZLAOJu1La5rmqTzwoAlfwfA/edit?usp=sharing
