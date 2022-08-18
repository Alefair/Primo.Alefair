![logo](https://raw.githubusercontent.com/Alefair/C-Nugets/main/Alefair.SAP.API/Images/saplogo_nuget.png)
# Primo.Alefair.SAP

```
SAP Activities For Primo RPA Platform , used by API [Alefair.SAP.API](https://github.com/Alefair/C-Nugets/tree/main/Alefair.SAP.API)
```

>Current version **[1.0.3](https://github.com/Alefair/Primo.Alefair/blob/main/SAP/Packages/Primo.Alefair.SAP.1.0.3.nupkg)**
>

>[nuget](https://www.nuget.org/packages/Alefair.SAP.API/1.0.4) on https://www.nuget.org

- [x] SAP API Object
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

>- **SAP API Object**  
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

>- **SAP Get Connection**  
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

>- **SAP Get Session**  
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
