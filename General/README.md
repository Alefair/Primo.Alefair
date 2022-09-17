![logo](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/General/Images/alefair.png)
# Primo.Alefair.General

```
Activities For Primo RPA Platform Powered by Alefair
```

>Current version **[1.0.6](https://github.com/Alefair/Primo.Alefair/blob/main/General/Packages/Primo.Alefair.General.1.0.6.nupkg)**
>

>[nuget](https://www.nuget.org/packages/Primo.Alefair.General/1.0.6) on https://www.nuget.org

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


# 1.0.5

> **Read Config From Excel(updated)**  
![Read Config From Excel](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/General/Images/ReadConfig_Form.PNG)

```
Read data from excel to Dictionary

[Properties]
Assets Sheet is Assets*: If Sheet Assets is Exist then Varables as Assets
NumberFormat*: NumberFormat as type in VBA
Column Variable Name*: Column name of Variable Name
Column Variable Value*: Column name of Variable Value
Column Asset Name*: Column name of Asset Name
List of Sheets Names*: List of Sheets Names where varables exist
Json Asset To Dictionary*: Json value of asset put to dictionary
Path*: Path

[Output]
Config*: Config as Dictionary<string, object>
```
![Read Config From Excel](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/General/Images/ReadConfig_Properties3.PNG)

------------


# 1.0.6

> **HTML Table Creator**  
![HTML Table Creator](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/General/Images/HTML%20Table%20Creator%20Form.PNG)

```
Create HTML Table from DataTable with style. Uses css styles

[Properties]
Data Table*: DataTable Object
Use Number Row Column*: Add to table column "#"
Container Style*: Style of the container in which the table will be added
Table Title*: Add <span> html element with title of table
Table Title Style*: Style for <span> html element with title of table
Table Style*: Style for <table> element
Header Border Style*: Style  for border of <table> element
Header Style*: Style for <thead> element
Header Row Style*: Style for <thead><th> element
Body Row Style*: Style for <tr> element of <tbody> element

[Output]
HTML Table*: HTML Table use as html element <table></table>
```
![HTML Table Creator](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/General/Images/HTML%20Table%20Creator%20Properties.PNG)

In out -> html code:

```
<div style="width:1300px;padding:10px;">
  <span style="padding: 10px;border: 1px solid #ffcdd2;color: #f44336;font-size: 11pt;font-family: Tahoma;width:200px;display: block;">Table 1</span>
  <table border="1" cellpadding="10" cellspacing="10" bordercolor="#ffcdd2" width="100%" style="margin: 0;text-decoration: none;color: #979797;font-size: 11pt;font-family: Tahoma;border-collapse: collapse;"> 
    <thead style="background: #00bcd4;text-align: center;color: white;font-weight: bold;font-size: 13pt;height: 40px;border:1px solid #ffcdd2;"><tr style="margin: 0; padding: 0px;">
      <th>#</th>
      <th>ABC</th>
      <th>QWE</th>
      </tr>
    </thead>
    <tbody>
      <tr style="text-align: center; margin: 0px; padding: 0px; border: 1px solid #ccc;background: #f06292;color: white;">
        <td>0</td><td>123</td><td>zxcv</td>
      </tr>
      <tr style="text-align: center; margin: 0px; padding: 0px; border: 1px solid #ccc;background: #f06292;color: white;">
        <td>1</td><td>adf</td><td>rty</td>
      </tr>
      <tr style="text-align: center; margin: 0px; padding: 0px; border: 1px solid #ccc;background: #f06292;color: white;">
        <td>2</td><td></td><td></td>
      </tr>
      <tr style="text-align: center; margin: 0px; padding: 0px; border: 1px solid #ccc;background: #f06292;color: white;">
        <td>3</td><td>36</td><td>xvx</td>
      </tr>
    </tbody>
  </table>
</div>
```

![HTML Table Creator](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/General/Images/HTML%20Table%20Creator%20Example.PNG)

------------
