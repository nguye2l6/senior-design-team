# Getting Started
## Quick Overview
MalAI is an AI-powered Ghidra Plugin that aims to reduce the time taken in reverse engineering a program. Some features that MalAI provides are: decompilation through LLMs, malicious file classifications, and malware injection.

### Decompilation Through LLMs

Decompilation is the process of converting assembly code to a higher human-readable programming language like C/C++. Ghidra provides a built in decompiler which allows users to accurately perform this process; however, the higher level code provided by Ghidra is often difficult to understand due to optimizations performed on the inspected programs original c-code.

MalAI serves as a tool to bridge this gap by integrating a LLM finetuned on decompilation tasks in order to generate a more user-friendly decompilation output.

### Malicious File Classifications

In order to aid reverse engineers, MalAI integrates a model for malicious file classifications. By inspecting the patterns and structures of millions of malicious file samples, the model can accept a file from a user and determine whether it is malicious or not.

### Malware Injection

Lastly, MalAI provides the ability to insert malicious code into existing code. This feature is less functional and more of a proof of concept that showcases the malicious code structures the model learned from its training dataset.

## How to use  MalAI - Plugin?
### Installation
To install MalAI plugin in Ghidra:

1) Go to MalAI's Github repository ( [MalAI](https://github.com/nguye2l6/senior-design-team) - MalAI repository link) and download the zip folder containg the MalAI plugin to be installed in Ghidra.
2) Make sure you have Ghidra installed, if not please refer to the Ghidra Repository link at the end of the document.
3) If you have Ghidra installed in your machine, please open the Ghidra application.
4) From the tool bar, click on "file" and then click on "Install Extensions".
5) After clicking on "Install Extensions", a new window will pop up showing the currently installed Extensions. Click on the green plus sign.
6) After clicking on the plus sign, a new window will open allowing you to select the zip folder to be installed in Ghidra.
7) After choosing the zip folder to be installed, restart Ghidra.
8) After restarting Ghidra, click on "file" from the tool bar again and then click on "Install Extensions". You should see MalAI plugin installed as the below image showcase. 


![image](https://hackmd.io/_uploads/ry6KNNYPbe.png)



### Steps to use MalAI
#### Choosing the project to be tested

To start using Ghidra you need first to create a project to be used or use an existing project.

#### Creating a new project

To Create a new project, click on file from the tool bar then choose a "New Project" option, after choosing that option you will be asked to choose wheather the project is shared or not, choose one and a window as below will be displayed. Type the name of the project and choose the location of the folder to be used.

![image](https://hackmd.io/_uploads/Hyjy6fYPWl.png)
#### Using existing project

If you have an existing project, click on file from the tool bar then choose "Open Project". After choosing that option, locate the project folder. After choosing the project, you will be directed to the below window which is under the project name.

**Note**: Project folder should end with .gpr extension.

![image](https://hackmd.io/_uploads/B1dzTztvbl.png)

#### Choosing the file to be decompiled

Once a project is selected, the project folder tree will displayed as below, browse the folder and choose the file to be decompiled.
![image](https://hackmd.io/_uploads/rJVVTfFPZl.png)

#### Selecting MalAI plugin

By clicking in the window option from the tool bar, a number of tools will be displayed, Choose MalAI_Plugin
![image](https://hackmd.io/_uploads/Hyf7FmtvZx.png)

The pluign window would look like as below. In this window the decompiled code will be shown.
![image](https://hackmd.io/_uploads/BySUY7tPWe.png)

#### Detecting Malware
To detect Malware click on the "Malware Detection" button at the tool bar of the MalAI_Plugin window. Once the button is clicked, a message will be invoked returning wheather the file is malicious or not. 

**Note**: The user interface for this feature is not finalized yet.

#### Injecting Malware
To inject malware, click on the "Malware Injection" button located in the toolbar of the MalAI_Plugin window. Once the button is clicked, the interface will be redirected to the generated malware sample in the existing code.

**Note**: The user interface for this feature is not finalized yet.


## Beneficial Resources 
- [Ghidra Repository](https://github.com/NationalSecurityAgency/ghidra)
