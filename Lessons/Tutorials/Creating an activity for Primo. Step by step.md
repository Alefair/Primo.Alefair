![Activity](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Activity.PNG)


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

![DesignActivity](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/DesignActivity.PNG)

<br><br>

**And First Build!**
-> Solution Explorer
-> Right Click **"Solution 'Primo.My.Activity'"**
-> Clean Solution
-> Build Solution

![Build](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Build.PNG)

<br><br>

*Check in output 1 Successed!*

![BuildSuccess](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/BuildSuccess.PNG)

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

![Tree](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Tree.PNG)

<br><br>

- ### [GLOBAL VARIABLE]
> We will need 3 variables: a reference to an instance of the MyFirstActivity_Form, a variable for input and a variable for output

```csharp
private Design.MyFirstActivity_Form cbase;
private string in_argument;
private string out_argument;

```

<br><br>


- ### [PROPERTIES]
> These properties will be displayed in the properties window in Primo Studio

```csharp
///In_Argument
/// 
[LTools.Common.Model.Serialization.StoringProperty]
[LTools.Common.Model.Studio.ValidateReturnScript(DataType = typeof(string))]
[Category("In_Argument"), DisplayName("In_Argument")]
[DefaultValue(0)]
public string In_Argument
{
    get { return this.in_argument; }
    set { this.in_argument = value; this.InvokePropertyChanged(this, nameof(In_Argument)); }
}


/// Out_Argument
/// 
[LTools.Common.Model.Serialization.StoringProperty]
[LTools.Common.Model.Studio.ValidateReturnScript(DataType = typeof(string))]
[Category("Out_Argument"), DisplayName("Out_Argument")]
[DefaultValue(0)]
public string Out_Argument
{
    get { return this.out_argument; }
    set { this.out_argument = value; this.InvokePropertyChanged(this, nameof(Out_Argument)); }
}

```

<br><br>

**What's here?**

```javascript
[LTools.Common.Model.Studio.ValidateReturnScript(DataType = typeof(string))]
```
**DataType = typeof(string)**
> The Primo Studio will check what type of value you are trying to enter

<br><br>

```javascript
[Category("Out_Argument"), DisplayName("Out_Argument")]
```
**Category("Out_Argument")**
> The category of the variable in which the argument will be displayed in the properties window
**DisplayName("Out_Argument")**
> The name of the argument to be displayed in the properties window

<br><br>


- ### [PROPERTIES][TYPES]
> Here we describe all the activity in full: what will be the name, what will be the icon, the Activity Help, what type of editor will the arguments have, etc...

```csharp
public MyFirstActivity(IWFContainer container) : base(container)
{
    sdkComponentIcon = "pack://application:,,/Primo.My.Activity;component/Images/eye_ico.png";

    sdkComponentName = "My First Activity";
    sdkComponentHelp = "In the activity, you can specify a path and it will be filled into a string variable";


    ///[PROPERTIES]
    ///
    sdkComponentHelp += "\r\n" + "\r\n" + "[Properties]";


    sdkComponentHelp += "\r\n"
                     + nameof(In_Argument) + "*: "
                     + "The Path";


    ///[Output]
    sdkComponentHelp += "\r\n" + "\r\n" + "[Output]";

    sdkComponentHelp += "\r\n"
                     + nameof(Out_Argument) + "*: "
                     + "Variable for Set";



    sdkProperties = new List<LTools.Common.Helpers.WFHelper.PropertiesItem>()
    {
        new LTools.Common.Helpers.WFHelper.PropertiesItem()
        {
            PropName = nameof(In_Argument),
            PropertyType = LTools.Common.Helpers.WFHelper.PropertiesItem.PropertyTypes.SCRIPT,
            EditorType = ScriptEditorTypes.NONE,
            DataType = typeof(string),
            ToolTip = nameof(In_Argument),
            IsReadOnly = false
        },


        new LTools.Common.Helpers.WFHelper.PropertiesItem()
        {
            PropName = nameof(Out_Argument),
            PropertyType = LTools.Common.Helpers.WFHelper.PropertiesItem.PropertyTypes.VARIABLE,
            EditorType = ScriptEditorTypes.NONE,
            DataType = typeof(string),
            ToolTip = nameof(Out_Argument),
            IsReadOnly = false
        }
    };

    InitClass(container);



    ///Create Instance of MyFirstActivity_Form
    try
    {
        Design.MyFirstActivity_Form inputform = new Design.MyFirstActivity_Form();


        this.cbase = inputform;
        this.cbase.DataContext = (object)this;
        WFElement wfElement = new WFElement((IWFElement)this, container);
        this.element = wfElement;
        
        ///Create Event if Buttons is clicked
        ///
        this.cbase.Form_btn.Click += new RoutedEventHandler(this.MyFirstActivity_Form_btn_Click);
        
        this.element.Container = (FrameworkElement)this.cbase;

    }
    catch
    {
    }

    ///Value by Default of "In_argument" argument
    this.In_Argument = "\"Choose path...\"";
}
```
> **this.MyFirstActivity_Form_btn_Click** - method in **[ADVANCED]** block

<br><br>



- ### [EXECUTION]
> The main block where all activity and executions take place

```csharp
public override ExecutionResult SimpleAction(ScriptingData sd)
{
    try
    {
        #region [VARIABLES][INIT]
        string property_In_Argument = GetPropertyValue<string>(this.In_Argument, nameof(In_Argument), sd);

        #endregion

        #region [PROCESS]



        #endregion

        #region [OUTPUT]

        WFHelper.AssignToVariable(
            this.out_argument,
            property_In_Argument,
            property_In_Argument.GetType(),
            sd.Variables
        );

        #endregion

        ExecutionResult executionResult = new ExecutionResult();
        executionResult.SuccessMessage = "Done";
        executionResult.IsSuccess = true;

        return executionResult;
    }
    catch (Exception ex)
    {
        ExecutionResult executionResult = new ExecutionResult();
        executionResult.ErrorMessage = ex?.Message;
        executionResult.IsSuccess = false;

        return executionResult;
    }
}
```

<br><br>


- ### [VALIDATE]
> Here we check that all or part of our arguments are filled in or have a certain type

```csharp
public override ValidationResult Validate()
{
    ValidationResult ret = new ValidationResult();
    if (System.String.IsNullOrEmpty(this.In_Argument)) ret.Items.Add(new ValidationResult.ValidationItem() { PropertyName = nameof(Out_Argument), Error = "It should not be empty!" });
    return ret;
}
```

<br><br>

- ### [ADVANCED]
> Here we create auxiliary functions necessary for work

```csharp
private void MyFirstActivity_Form_btn_Click(object sender, RoutedEventArgs e)
{
    Microsoft.Win32.OpenFileDialog openFileDlg = new Microsoft.Win32.OpenFileDialog();
    openFileDlg.Filter = "Excel files (*.xls; *.xlsx)|*.xls;*.xlsx";
    if (openFileDlg.ShowDialog() == true) this.In_Argument = "@\"" + openFileDlg.FileName + "\"";
}
```

<br><br>

## 5. Final Building and nuget Package

- Click Bulding
- If Building is success, then go to Folder of Project
- Open Primo.My.Activity\bin\Debug
- Looking for a file Primo.My.Activity.dll and copy to Desktop
- Open Nuget Package Explorer
- Add lib Folder
- Add to lib file Primo.My.Activity.dll and eye_nuget.png(from Images)
- Fill in the fields

<br><br>

![Nuget](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Nuget.PNG)

- Save Nuget
- Upload To Studio
- And Use

You are welcome! :-)

