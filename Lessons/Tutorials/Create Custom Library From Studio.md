# Create Custom Library from studio of the Primo RPA Platform
------------

```
Hi guys!

Today we will make a mini library from the studio of the Primo RPA platform
```

**Let's go**

<br><br>

## 1. Start  

Create new Project  
![Start](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Lib/1.PNG)

<br>

Create new Method(Process)

![New process](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Lib/2.PNG)


<br>

For example Method **Kill**

![Method Kill](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Lib/3.PNG)

------------

## 2. Process

Create Process

For Example I added C# activity

Created Arguments **ProcessName** and **Result**

![Add Activity](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Lib/4.PNG)

------------

## 3. Code

![Code](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Lib/7.PNG)

------------

## 4. Publish

- Remove Process **Main.ltw**

![Remove Main File](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Lib/8.PNG)

- Save File
- Click **File** -> **Export** -> **Create library**
- Input Data

![Remove Main File](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Lib/9.PNG)

- Find Your .NETFramework version and file mscorlib.dll

![.NETFramework](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Lib/11.PNG)

- Save dll to Folder of Project

![Save dll](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Lib/10.PNG)

![Success](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Lib/12.PNG)


And every method need build dll.

------------

## 5. Nuget

Generate nuget package

![Nuget](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Lib/13.PNG)

------------

## 6. Upload to new Project and test result
- Install pacckage

![Install](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Lib/14.PNG)

<br>

- Add Namespace

![Namespace](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Lib/15.PNG)

<br>

- Check Activity in Elements Window and add to project

![Activity](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Lib/16.PNG)

<br>

- Input data to activity and debug project

