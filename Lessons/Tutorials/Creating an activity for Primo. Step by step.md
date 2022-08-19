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
  
## Great, let's write our first activity design!  

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

Okay, Column Definitions and Row Definitions Exists, then under **</Grid.RowDefinitions>** add a picture:

```html
<Grid Grid.Row="0" Grid.Column="0">
  <Image HorizontalAlignment="Left" 
         Source="pack://application:,,/User.My.Activity;component/Images/eye_logo.png"
         Height="80"
         Width="80"
         Margin="5,5,5,5"
  />
</Grid>
```

**What's here?**

```
Grid Grid.Row="0" Grid.Column="0"
```
> We have created a grid for the first column of the first row and we want to insert a picture here.


```
Source="pack://application:,,/User.My.Activity;component/Images/eye_logo.png"
```
> Path to image, It consists of the name of the library(**User.My.Activity**) and the path inside the library(**Images/eye_logo.png"**)


```
Height="80" and Width="80"
```
> New size of Picture


```
Margin="5,5,5,5"
```
> This is margin from the border of the grid(Left, Top, Right, Bottom)
