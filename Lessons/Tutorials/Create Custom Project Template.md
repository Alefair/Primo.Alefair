# Create Custom Project Template for Primo RPA Platform
------------

```
Hi network!

Today we will make a custom project template for Primo RPA Platform
```

**One, two, three...**

<br><br>

## 1. Start 
- Create new Framework Project 
- Add your favorite Dependencies
- Add your favorite Namespaces
- Test this
- And save

## 2. Preparatory steps
Ok? Next... Template consist from:
- **icon.png** - only this name
- **manifest.xml** - only this name
- **project.zip** - only this name

![Template Folder](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Template/1.PNG)

Open folder with your project
<br>
- Copy your dependencies.xml file to Data Folder for Example(Absolutely!)

![dependencies file](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Template/2.PNG)

- Open project.ltr with Notepad and clean this file, as below
![project.ltr](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Template/3.PNG)

- Open project.ltp with Notepad and clean this file, as below
![project.ltp](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Template/4.PNG)

- Select all files and zip to project.zip

![zip](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Template/5.PNG)

- **icon.png**([Example]()). Only size 48x48 px. You can create, for example, here https://online-fotoshop.ru/


- **manifest.xml**([Example]()). Create file, as below:
![manifest](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Template/6.PNG)


- Go to C:\Program Files\Primo\Primo Studio x64\ProjectTemplates and create folder with your template name
![Template Folder](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Template/7.PNG)
<br>
- Put in this folder your files: icon.png, manifest.xml, project.zip
<br>
- Open your Primo RPA Platfor Studio and find your project template: File -> Project

![Template Studio](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Template/8.PNG)


## 3. Using
- Create your new project. 
- After Building We see that after creating the project there are no dependencies. Close Studio.
- Next Copy dependencies.xml from Data Folder to root folder of project and replace this file.

![replace dependencies](https://raw.githubusercontent.com/Alefair/Primo.Alefair/main/Lessons/Images/Custom_Template/9.PNG)
- Start studio and open your new project from custom template
- **ENJOY**


<br><br>

### Thanks for listening :-)
