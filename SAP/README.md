![logo](https://raw.githubusercontent.com/Alefair/C-Nugets/main/Alefair.SAP.API/Images/saplogo_nuget.png)
# Primo.Alefair.SAP

```
SAP Activities For Primo RPA Platform , used by API Alefair.SAP.API - https://github.com/Alefair/C-Nugets/tree/main/Alefair.SAP.API
```

>Current version **[1.0.6](https://github.com/Alefair/Primo.Alefair/blob/main/SAP/Packages/Primo.Alefair.SAP.1.0.6.nupkg)**
>

>[nuget](https://www.nuget.org/packages/Primo.Alefair.SAP/1.0.6) on https://www.nuget.org

- [x] SAP API Object
- [x] SAP Get Connection
- [x] SAP Get Session
- [x] SAP Connect
- [x] SAP Extract Table
- [x] SAP Click
- [x] SAP Element Focus
- [x] SAP Get Text
- [x] SAP Set Text
- [x] SAP Open Transaction
- [x] SAP Get Title
- [x] SAP Get Status
- [x] SAP Kill Saplogon
- [ ] SAP Get Cell Value
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

------------

# 1.0.4

> **SAP Click**  
![SAP Click](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Click%20Form.PNG)

```
Generate Click or Double Click. Avaible: button, current row, check box, radio button

[Properties]
Session*: If only Number of session, then connection by default - con[0]. If empty by default ses[0]
Selector*: "wnd[0]/tbar[1]/btn[8]"
Click Type*: Click or DoubleClick
```
![SAP Click](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Click%20Properties.PNG)

------------

> **SAP Element Focus**  
![SAP Element Focus](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Element%20Focus%20Form.PNG)

```
Generate Focus State For Element

[Properties]
Session*: If only Number of session, then connection by default - con[0]. If empty by default ses[0]
Selector*: "wnd[0]/usr/txtENAME-LOW"
Extended*: Extended
Table Select Type*: 
 - SelectRows: Extended: "12, 13..." 
 - SelectColumns: Extended: "COLUMN_NAME" 
 - SelectCell: Extended: "13, COLUMN_NAME" 
 - SelectAll: Extended: ""
```
![SAP Element Focus](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Element%20Focus%20Properties.PNG)

------------

> **SAP Get Text**  
![SAP Get Text](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Get%20Text%20Form.PNG)

```
Get text from GuiComponent 
 Avaible GuiShell get text from cell

[Properties]
Session*: If only Number of session, then connection by default - con[0]. If empty by default ses[0]
Selector*: "wnd[0]/usr/ctxtS_VBELN-LOW"
Extended*: Extended for GuiShell. For Example: ~ "12, COLUMN_NAME"

[Output]
Result*: Result
```
![SAP Get Text](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Get%20Text%20Properties.PNG)

------------

> **SAP Set Text**  
![SAP Set Text](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Set%20Text%20Form.PNG)

```
Set text of GuiComponent 
 Avaible GuiShell set text into cell

[Properties]
Session*: If only Number of session, then connection by default - con[0]. If empty by default ses[0]
Selector*: "wnd[0]/usr/ctxtS_VBELN-LOW"
Value*: Value
Extended*: Extended for GuiShell. For Example: ~ "12, COLUMN_NAME"
```
![SAP Set Text](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Set%20Text%20Properties.PNG)

------------


# 1.0.5

> **SAP Open Transaction**  
![SAP Open Transaction](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Open%20Transaction%20Form.PNG)

```
Open SAP Transaction by name

[Properties]
Session*: If only Number of session, then connection by default - con[0]. If empty by default ses[0]

Transaction*: Open SAP Transaction by name
```
![SAP Open Transaction](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Open%20Transaction%20Properties.PNG)

------------


> **SAP Get Status**  
![SAP Get Status](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Get%20Status%20Form.PNG)

```
Get text from status bar of session window

[Properties]
Session*: If only Number of session, then connection by default - con[0]. If empty by default ses[0]

[Output]
Result*: Result
```
![SAP Get Status](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Get%20Status%20Properties.PNG)

------------


> **SAP Get Title**  
![SAP Get Title](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Get%20Title%20Form.PNG)

```
Get text from title of session window

[Properties]
Session*: If only Number of session, then connection by default - con[0]. If empty by default ses[0]

[Output]
Result*: Result
```
![SAP Get Title](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Get%20Title%20Properties.PNG)

------------


# 1.0.6

> **SAP Kill Saplogon**  
![SAP Kill Saplogon](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Kill%20Form.PNG)

```
Kill Saplogon

[Properties]
SAP GUI object*: SAP GUI as Instance of SAP GUI Object
```
![SAP Kill Saplogon](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/SAP/Images/SAP%20Kill%20Properties.PNG)

------------
