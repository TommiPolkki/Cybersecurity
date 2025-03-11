 ZAP by Checkmarx Scanning Report

ZAP by [Checkmarx](https://checkmarx.com/).


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 0 |
| Low | 1 |
| Informational | 2 |




## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- |
|  | Low | 1 |
|  | Informational | 2 |
| Abuse of Functionality | Informational | 1 |




## Alert Detail




### 


##### Low (Medium)

### Description



* URL: http://localhost:8000/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``

Instances: 1

### Solution



### Reference




#### Source ID: 2


### 


##### Informational (Medium)

### Description



* URL: http://localhost:8000/robots.txt
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://localhost:8000/register
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``

Instances: 2

### Solution



### Reference




#### Source ID: 2


### Abuse of Functionality


##### Informational (Medium)

### Description

Abuse of Functionality is an attack technique that uses a web site's own features and functionality to attack itself or others. Abuse of Functionality can be described as the abuse of an application's intended functionality to perform an undesirable outcome. These attacks have varied results such as consuming resources, circumventing access controls, or leaking information. The potential and level of abuse will vary from web site to web site and application to application. Abuse of functionality attacks are often a combination of other attack types and/or utilize other attack vectors.

* URL: http://localhost:8000/register
  * Method: `POST`
  * Parameter: ``
  * Attack: `scan`
  * Evidence: ``
  * Other Info: ``

Instances: 1

### Solution

Always utilize APIs in the specified manner.

### Reference


* [ https://cheatsheetseries.owasp.org/cheatsheets/Abuse_Case_Cheat_Sheet.html ](https://cheatsheetseries.owasp.org/cheatsheets/Abuse_Case_Cheat_Sheet.html)
* [ https://cwe.mitre.org/data/definitions/227.html ](https://cwe.mitre.org/data/definitions/227.html)



#### WASC Id: 42

#### Source ID: 2
