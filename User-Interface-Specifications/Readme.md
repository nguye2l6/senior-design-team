

## User Interface Specification
### Overview:
In this project we focused more on solving the problems we are trying to approach, hence Complexity and Readability; therefore, the User Interface at this moment is fairly simple as it contains the following:
- Buttons:
	- Decompilation Button
	- Malware Detection Button
- Text Area:
	- Decompilation results text area
	- Malware Detection results text area

### User Flow:
Upon choosing a file to analyze and opening the MalAI plugin via the tool bar in Ghidra, the user will have an interface open as figure 1 shows. The interface in figure 1 show to the user two options, either Decompile ASM or Detect Malware. 

1) **Decompile ASM button** requires the user placing the cursor at the disassembled code of the original file. By placing the cursor at certain location and clicking the decompilation, the plugin will take the disassembled code of the function the cursor is located at and pass it to the integrated LLM which will return the results a response to be shown at the Decombilation results text area as figure 2 shows.

2) **Malware Detection button** (Not Functional Yet) takes the raw bytes of the analyzed file and pass it to the Malware Detection model integrated. Malware Detection model integrated is a binary classification model that can take raw bytes to be processed and outputs either benign or malicious in the Malware Detect. If the file is benign the Malware Detection text area will be green otherwise it would be red.

Via the Decompilation button, the user could browse the disassembled code and decompile each function and compare Ghidra's and MalAI. Whereas the Malware Detection button will take the whole bytes of the file and pass them to Malware Detection model, so if it was to be pressed again it would, presumably, the same results.


![[MalAI_Ghidra_Plugin_1.png]]
Figure 1: User Interface before clicking "Decompilation ASM" button


![[MalAI_Ghidra_Plugin_2.png|697]]
Figure 2: User Interface after clicking "Decompilation ASM" button

