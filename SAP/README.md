![logo](https://raw.githubusercontent.com/Alefair/C-Nugets/main/Alefair.SAP.API/Images/saplogo_nuget.png)
# Primo.Alefair.SAP

```
SAP Activities For Primo RPA Platform , used by API [Alefair.SAP.API](https://github.com/Alefair/C-Nugets/tree/main/Alefair.SAP.API)
```

>Current version **[1.0.3](https://github.com/Alefair/Primo.Alefair/blob/main/SAP/Packages/Primo.Alefair.SAP.1.0.3.nupkg)**
>

>[nuget](https://www.nuget.org/packages/Alefair.SAP.API/1.0.4) on https://www.nuget.org

------------
# 1.0.1

- **SAP API Object**
- 
![SAP API Object](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20API%20Object%20Form.PNG)

![SAP API Object](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20API%20Object%20Properties.PNG)

```
Get instance of SAP API Object

[Properties]
Path*: Path to SAP Logon
Timeout*: Timeout while SAP is loading

[Output]
SAP GUI object*: SAPAPI Object
```


- **SAP Get Connection**
![SAP Get Connection](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Get%20Connection%20Form.PNG)
![SAP Get Connection](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Get%20Connection%20Properties.PNG)

```
Get SAP Connection by Id or connection number

[Properties]
Connection Id/number, by default - con[0]*: Number or Id of GuiConnection

[Output]
Connection*: Connection as GuiConnection
```


- **SAP Get Session**
![SAP Get Session](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Get%20Session%20Form.PNG)
![SAP Get Session](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Get%20Session%20Properties.PNG)

```
Get SAP Session by Id or connection number

[Properties]
Connection*: Connection as GuiConnection
Session Id/number, by default - ses[0]*: Number or Id Of GuiSession

[Output]
Session*: Session as GuiSession
```












- **SAP Connect**
![SAP Connect](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Connect%20Form.PNG)
![SAP Connect](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Connect%20Properties.PNG)

```
Connect to SAP with Login and Password

[Properties]
User*: SAP Account
Password*: Password of SAP Account
Base Name*: Base name of Connection. From Main Page

[Output]
Connection*: Connection as GuiConnection
```



- SAP Get Connection
- SAP Get Session



- SAP Extract Table
- SAP Open Transaction
- SAP Click
- SAP Enter
