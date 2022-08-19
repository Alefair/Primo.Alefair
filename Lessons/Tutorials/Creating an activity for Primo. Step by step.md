# Creating an activity for Primo. Step by step
------------

**Hi guys!** 

>Today we will write a new activity for the RPA - **#Primo** platform. Step by step. 

I will use Visual Studio Community. Download it if you haven't done it yet :) 

**And let's go...**

## 1. Start  

Create new Project  
![Start](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Start.PNG)

<br><br>

Choice Project Template, need **Class Library (.NET Framework)**  
![New Class](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/NewClass.PNG)
 
<br><br>
 
Create new Project  
![New Project](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/ProjectName.PNG)  

<br><br>

**Warning! The library name must begin with Primo...** - Primo.My.Activity
 
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
  
## 3. Great, let's write our first activity design!  

- Right Click on **Activities** -> Add -> New Item... -> Choose **C# Class** -> Name: **MyFirstActivity.cs** -> Add

- Next, Right Click on **Design** -> Add -> New Item... -> Choose **User Control (WPF)** -> Name: **MyFirstActivity_Form.xaml** -> Add
  
> Okay, Now let's do a little design and a little creativity
  
![Chema](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Chema.PNG)

![Position](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Position.PNG)


Double Click On **MyFirstActivity_Form.xaml** and let's create 2 columns and 2 rows. Let's display the grid -> Grid property -> **ShowGridLines="True"**

Just replace new Grid this code:

```html
  <Grid x:Name="MyFirstActivity_Form_grd" 
            VerticalAlignment="Center" 
            HorizontalAlignment="Center" 
            ShowGridLines="True"
            Background="White"
            
  >
    <Grid.ColumnDefinitions>
        <ColumnDefinition></ColumnDefinition>
        <ColumnDefinition></ColumnDefinition>
    </Grid.ColumnDefinitions>
    <Grid.RowDefinitions>
        <RowDefinition></RowDefinition>
        <RowDefinition></RowDefinition>
    </Grid.RowDefinitions>
  </Grid>
```
<br><br>

Okay, Column Definitions and Row Definitions Exists, then under **</Grid.RowDefinitions>** add a picture:

```html
<Grid Grid.Row="0" Grid.Column="0">
  <Image HorizontalAlignment="Left" 
         Source="pack://application:,,/User.My.Activity;component/Images/eye_logo.png"
         Height="40"
         Width="40"
         Margin="5,5,5,5"
  />
</Grid>
```

<br><br>

**What's here?**

```javascript
Grid.Row="0" Grid.Column="0"
```
> We have created a grid for the first column of the first row and we want to insert a picture here.

<br><br>

```javascript
Source="pack://application:,,/Primo.My.Activity;component/Images/eye_logo.png"
```
> Path to image, It consists of the name of the library(**Primo.My.Activity**) and the path inside the library(**Images/eye_logo.png"**)

<br><br>

```javascript
Height="40" and Width="40"
```
> New size of Picture

<br><br>

```javascript
Margin="5,5,5,5"
```
> This is margin from the border of the grid(Left, Top, Right, Bottom)

<br><br>

Next the second column of the first row, where we will have the name of our activity:

```javascript
<Grid rid.Row="0" Grid.Column="1">
    <!-- Activity Name -->
    <Label Content="My First Activity"/>
</Grid>
```

<br><br>

Next First Column and Second Row. Grid is Empty

```javascript
<Grid Grid.Row="1" Grid.Column="0">
  <!-- Row 1 -->
</Grid>
```

<br><br>

And at the end, in the second column of the second row, we will add a grid and a button to it

```javascript
<Grid  Grid.Row="1" Grid.Column="1">
  <Button x:Name="Form_btn" Content="Open" />
</Grid>
```

<br><br>

And Full grid:

```javascript
<Grid x:Name="MyFirstActivity_Form_grd" 
      VerticalAlignment="Center" 
      HorizontalAlignment="Center" 
      ShowGridLines="True"
      Background="White"
>
    <Grid.ColumnDefinitions>
        <ColumnDefinition></ColumnDefinition>
        <ColumnDefinition></ColumnDefinition>
    </Grid.ColumnDefinitions>
    <Grid.RowDefinitions>
        <RowDefinition></RowDefinition>
        <RowDefinition></RowDefinition>
    </Grid.RowDefinitions>
    <Grid Grid.Row="0" Grid.Column="0">
        <Image HorizontalAlignment="Left" 
             Source="pack://application:,,/Primo.My.Activity;component/Images/eye_logo.png"
             Height="40"
             Width="40"
             Margin="5,5,5,5"
        />
    </Grid>
    <Grid Grid.Row="0" Grid.Column="1">
        <!-- Activity Name -->
        <Label Content="My First Activity"/>
    </Grid>
    <Grid Grid.Row="1" Grid.Column="0">
        <!-- Row 1 -->
    </Grid>
    <Grid  Grid.Row="1" Grid.Column="1">
        <Button x:Name="Form_btn" Content="Open" />
    </Grid>
</Grid>
```

![DesignActivity](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/DesignActivitys.PNG)

<br><br>

**And First Build!**
-> Solution Explorer
-> Right Click **"Solution 'Primo.My.Activity'"**
-> Clean Solution
-> Build Solution

![Build](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Build.PNG)

<br><br>

*Check in output 1 Successed!*

![BuildSuccess](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/BuildSuccesss.PNG)

<br><br>

And Result:

![RenderActivity](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/RenderActivity.PNG)

------------

## 4. Lets codding!

> Well, it's going to be very interesting now! :)

Open **MyFirstActivity.cs** and and create an activity structure:

- ### Add Namespaces

```csharp
using LTools.Common.Helpers;
using LTools.Common.Model;
using LTools.Common.UIElements;
using LTools.Common.WFItems;
using LTools.SDK;
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;
```

<br><br>

Change class to **public class MyFirstActivity : PrimoComponentSimple<Design.MyFirstActivity_Form>**

<br><br>

And create an activity structure:
- GROUP NAME
- GLOBAL VARIABLE
- PROPERTIES
- PROPERTIES TYPE
- EXECUTION
- VALIDATE
- ADVANCED

<br><br>

Full code:

```csharp
using LTools.Common.Helpers;
using LTools.Common.Model;
using LTools.Common.UIElements;
using LTools.Common.WFItems;
using LTools.SDK;
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;

namespace Primo.My.Activity.Activities
{
    public class MyFirstActivity : PrimoComponentSimple<Design.MyFirstActivity_Form>
    {
        #region [GROUP NAME]
        ///----------------------------------------------
        /// GROUP NAME
        #endregion


        #region [GLOBAL VARIABLE]
        ///----------------------------------------------
        /// GLOBAL VARIABLE
        #endregion


        #region [PROPERTIES]
        ///----------------------------------------------
        /// PROPERTIES
        #endregion


        #region [PROPERTIES][TYPES]
        ///----------------------------------------------
        /// PROPERTIES TYPES
        #endregion


        #region [EXECUTION]
        ///----------------------------------------------
        /// EXECUTION
        #endregion


        #region [VALIDATE]
        ///----------------------------------------------
        /// VALIDATE
        #endregion


        #region [ADVANCED]
        ///----------------------------------------------
        /// ADVANCED
        #endregion
    }
}

```

![CleanCode](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/CleanCode.PNG)

<br><br>

- ### [GROUP NAME]
> The name of the group that will be displayed in the Primo Studio activity tree

```csharp
public override string GroupName
{
    get => "My{\\}MyFirstActivity";
    protected set { }
}

```

<br><br>

- ### [GROUP NAME]
> The name of the group that will be displayed in the Primo Studio activity tree

```csharp
public override string GroupName
{
    get => "My{\\}MyFirstActivity";
    protected set { }
}

```

<br><br>
