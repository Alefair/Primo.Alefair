# Creating an activity for Primo. Step by step
------------

**Hi guys!** 

>Today we will write a new activity for the RPA - **#Primo** platform. Step by step. 

I will use Visual Studio Community. Download it if you haven't done it yet :) 

**And let's go...**

## 1. Start  

Create new Project  
![Start](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Start.PNG)
  
Choice Project Template, need **Class Library (.NET Framework)**  
![New Class](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/NewClass.PNG)
  
Create new Project  
![New Project](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/ProjectName.PNG)  
 
 File Class1.cs needs to be deleted!

------------

## 2. Project preparation

window **Solution Explorer**

- ### Add References:
  - LTools.Common
  - LTools.DTO
  - LTools.Enums
  - LTools.Scripting
  - LTools.SDK

Usually they can be found in the folder where Primo installed

![References](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/References.PNG)
  
  
  
- ### Create Folders:
  - **Activities**
  - **Design**
  - **Images**
  - Resources(optional)

![References](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Folders.PNG)

- ### Downloads images:
  - [This](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Tutorials/Files/eye_ico.png)
  - [This](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Tutorials/Files/eye_logo.png)
  - [And This](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Tutorials/Files/eye_nuget.png)


- ### Upload images To Project:
  - Right mouse click on Images Folder
  - -> Add
  - -> Existing Item...
  - -> File Choice change to "All Files"
  - -> Сhoose downloaded images
  - Every file -> Click -> Properties Window: in Advanced Category choose "Resource" in **Buld Action**

![Images](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Images.PNG)


- ### Package naming preparation:
  - Expand Properties and double click on AssemblyInfo.cs
  - Fill in the fields as in the picture:
  ![Assembly ](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Assembly.PNG)

------------
  
## Great, let's write our first activity!  

- Right Click on **Activities** -> Add -> New Item... -> Choose **C# Class** -> Name: **MyFirstActivity.cs** -> Add

- Next, Right Click on **Design** -> Add -> New Item... -> Choose **User Control (WPF)** -> Name: **MyFirstActivity_Form.xaml** -> Add
  
> Okay, Now let's do a little design and a little creativity
  
![Chema](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Chema.PNG)

![Position](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Position.PNG)
