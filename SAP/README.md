![logo](https://raw.githubusercontent.com/Alefair/C-Nugets/main/Alefair.SAP.API/Images/saplogo_nuget.png)
# Primo.Alefair.SAP

```
SAP Activities For Primo RPA Platform , used by API Alefair.SAP.API - https://github.com/Alefair/C-Nugets/tree/main/Alefair.SAP.API
```

>Current version **[1.0.3](https://github.com/Alefair/Primo.Alefair/blob/main/SAP/Packages/Primo.Alefair.SAP.1.0.3.nupkg)**
>

>[nuget](https://www.nuget.org/packages/Primo.Alefair.SAP/1.0.3) on https://www.nuget.org

- [x] ![logo](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/saplogo_ico.png =20x40) SAP API Object
- [x] SAP Get Connection
- [x] SAP Get Session
- [x] SAP Connect
- [x] SAP Extract Table
- [ ] SAP Open Transaction
- [ ] SAP Get Cell Value
- [ ] SAP Get Title
- [ ] SAP Get Status
- [ ] SAP Click
- [ ] SAP Close Session
- [ ] SAP Close Connection

------------
# 1.0.1

> **SAP API Object**  
![SAP API Object](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20API%20Object%20Form.PNG)

```
Get instance of SAP API Object

[Properties]
Path*: Path to SAP Logon
Timeout*: Timeout while SAP is loading

[Output]
SAP GUI object*: SAPAPI Object
```
![SAP API Object](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20API%20Object%20Properties.PNG)

------------

> **SAP Get Connection**  
![SAP Get Connection](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Get%20Connection%20Form.PNG)

```
Get SAP Connection by Id or connection number

[Properties]
Connection Id/number, by default - con[0]*: Number or Id of GuiConnection

[Output]
Connection*: Connection as GuiConnection
```
![SAP Get Connection](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Get%20Connection%20Properties.PNG)

------------

> **SAP Get Session**  
![SAP Get Session](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Get%20Session%20Form.PNG)

```
Get SAP Session by Id or connection number

[Properties]
Connection*: Connection as GuiConnection
Session Id/number, by default - ses[0]*: Number or Id Of GuiSession

[Output]
Session*: Session as GuiSession
```
![SAP Get Session](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Get%20Session%20Properties.PNG)

------------

# 1.0.2

> **SAP Connect**  
![SAP Connect](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Connect%20Form.PNG)

```
Connect to SAP with Login and Password

[Properties]
User*: SAP Account
Password*: Password of SAP Account
Base Name*: Base name of Connection. From Main Page

[Output]
Connection*: Connection as GuiConnection
```
![SAP Connect](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Connect%20Properties.PNG)

------------

# 1.0.3

> **SAP Extract Table**  
![SAP Extract Table](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Extract%20Table%20Form.PNG)

```
Get a table in a datatable from a loaded transaction report

[Properties]
Session*: If only Number of session, then connection by default - con[0]. If empty by default ses[0]
Selector*: "/app/con[0]/ses[0]/wnd[0]/usr/cntlGRID1/shellcont/shell"
Auto Double*: Parse text of cell to Double
Column Type*: Depending on the selected column type, the column names will change. Available: FULLNAME, DISPLAYNAME, TOOLTIP, TECH NAMES, DEFAULT. Default: DEFAULT

[Output]
Result*: Result
```
![SAP Extract Table](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Extract%20Table%20Properties.PNG)
