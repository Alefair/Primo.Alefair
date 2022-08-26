![logo](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/General/Images/alefair.png)
# Primo.Alefair.General

```
Activities For Primo RPA Platform Powered by Alefair
```

>Current version **[1.0.2](https://github.com/Alefair/Primo.Alefair/blob/main/General/Packages/Primo.Alefair.General.1.0.2.nupkg)**
>

>[nuget](https://www.nuget.org/packages/Primo.Alefair.General/1.0.1) on https://www.nuget.org

- [x] Get Asset
- [x] Read Config From Excel

------------
# 1.0.1

> **Get Asset**  
![Get Asset](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/General/Images/GetAsset_Activity.PNG)


```
Get Asset With Object

[Properties]
Asset Name*: Asset Name

[Output]
Asset Value*: Asset Value as Object
```
![Get Asset](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/General/Images/GetAsset_Properties.PNG)

------------

> **Read Config From Excel**  
![Read Config From Excel](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/General/Images/ReadConfig_Activity.PNG)


```
Read data from excel to Dictionary

[Properties]
Assets Sheet is Assets*: If Sheet Assets is Exist then Varables as Assets
Column Variable Name*: Column name of Variable Name
Column Variable Value*: Column name of Variable Value
List of Sheets Names*: List of Sheets Names where varables exist
Path*: Path

[Output]
Config*: Config as Dictionary<string, object>
```
![Read Config From Excel](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/General/Images/ReadConfig_Properties.PNG)

------------

# 1.0.2

> **Read Config From Excel(updated)**  
![Read Config From Excel](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/General/Images/ReadConfig_Activity.PNG)

```
Read data from excel to Dictionary

[Properties]
Assets Sheet is Assets*: If Sheet Assets is Exist then Varables as Assets
NumberFormat*: NumberFormat as type in VBA
Column Variable Name*: Column name of Variable Name
Column Variable Value*: Column name of Variable Value
Column Asset Name*: Column name of Asset Name
List of Sheets Names*: List of Sheets Names where varables exist
Path*: Path

[Output]
Config*: Config as Dictionary<string, object>
```
![Read Config From Excel](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/General/Images/ReadConfig_Properties2.PNG)

------------
