# MobileTesting_Appium
Information on Setup Appium for Mobile Automation-
1. Install Java (JDK), Node JS, Eclipse IDE and Android Studio (Note: I have installed everything in E drive instead of C drive due to disk space constraints).
For specific instructions on how to install the tools use ChatGPT or Claude.
Prompt: I want to install (name of the tool) for the first time in my system in C drive/E drive. Guide me through the entire process step by step. Also show me the steps to confirm if the tool is installed in my system 
2.Set the below System Variables in Environment Variables-
a. Name: JAVA_HOME
   Ex for Value:- E:\Java\jdk-27
   Note: To check that it is installed correctly open command prompt and type in below command
   java -v
b. Name:NODE_HOME
     Ex for Value:-  E:\Programs\Nodejs-Appium
   Note: To check that it is installed correctly open command prompt and type in below commands
   npm -v
   node -v
c. Name: ANDROID_HOME (Note: while installing this I created a folder Sdk separately)
     Ex for Value:- E:\Programs\AndroidStudio\Android\Sdk
d. Name:ANDROID_SDK_ROOT
   Ex for Value: E:\Programs\AndroidStudio\Android\Sdk
   Note: You will need to provide this path when you open Android Studio for the first time.
3.Press Win, search cmd or command prompt
4.Usually, the C drive path will appear, to change to E drive type in E:
You can navigate to folders in E drive using cd command like so - cd E:\Programs\
To navigate back use cd..
5.If tools are installed in C drive already, continue to type in below commands to create folders. Replace E with C depending on where your npm is installed, mine was in E drive, so I gave the path to it.
mkdir E:\npm-global
mkdir E:\npm-cache
mkdir E:\appium-home
6.Press Windows, search “Edit the system environment variables”, click Environment Variables
Under System variables, select Path → Edit → New, and add these two:
E:\Programs\Nodejs-Appium
E:\npm-global
You can also add this in User variables-Path as well
7.Under System variables, click New and add:
Name: APPIUM_HOME
Value: E:\appium-home
Note: Replace E with C depending on where your npm is installed
Click OK on all windows.
8.For C Drive appium installation-
a.Re-open command prompt and and type in below commands
   npm -v
   node -v
b.If node versions are available that means node is installed correctly. Otherwise re-install and check.
c.Then type in-
npm install -g appium  
9.For installation of appium in another drive-
a.Point npm to the E drive(Do this only if using npm is installed in another drive-E, Otherwise by default it will get installed in C drive)
b.Type in commands one by one-
npm config set prefix E:\npm-global
npm config set cache E:\npm-cache
cd E:\
npm install -g appium
Note:To uninstall this command used is -npm uninstall -g appium
10.Verify Installation complete-
   appium -v
11.Then confirm where it lives type in below:
  dir E:\npm-global
12.Install driver-
   For Android type in below:
appium driver install uiautomator2
13.Start appium by typing command-
   appium


