# minix_source_code_modifiaction

Modifying the Minix boot process involves several steps, and the specifics may vary depending on the version of Minix you are working with.

 

1. Set Up Minix Development Environment:
Download the MInix from here '''(http://lms2.cse.saveetha.in/mod/url/view.php?id=718)'''. Ensure that you have a Minix development environment set up '''( See Video http://lms2.cse.saveetha.in/mod/url/view.php?id=735 )'''. You can follow the instructions provided in the Minix documentation for setting up a build environment '''(See Video http://lms2.cse.saveetha.in/mod/url/view.php?id=737 ).'''
this abouve source was given by : dr.gowri ganesh

 
3. Locate Boot Code:
Identify the relevant source code files for the Minix boot process. Common files include boot/boot.asm, boot/boot.h, and /src/kernel/main.c.

4. Insert Your Code:
Modify Kernel Initialization (kernel/main.c):
Insert code to print a message during kernel initialization. In the following code replace the message "Modified by <<your name>>".  Here In place of your name please replace your name.

// kernel/main.c

#include <stdio.h>

void main(void) {
    // Existing kernel initialization code..
    printf("modified  by karthick\n");
}
4. Compile and Build:
Use the Minix build system to compile your modified code.

bash
# Assuming you are in the Minix source code directory
make build
5. Test Your Changes:
Transfer the new bootable image to a test environment, such as a virtual machine or a physical system, and observe the behavior during the boot process.

// Ensure that you are in the directory /usr/src/releasetools
make hdboot
Copy the code that you made changes in the MINIX

Attach the screen shot of the MINIX booting process with the new modifications.

1. Changes done in the main.c under /usr/src/kernel as below:

Source code modification:

![Screenshot 2024-04-21 202851](https://github.com/gorghs/minix_source_code-_modifiaction/assets/149037461/06da9fb9-3899-4228-93f3-d335e8ce58c0)

Observe the MINIX booting process with the new modifications as below:
![image_2024-04-21_203224795](https://github.com/gorghs/minix_source_code-_modifiaction/assets/149037461/0befa272-3f3a-4940-bc9b-5ee5175771ba)

