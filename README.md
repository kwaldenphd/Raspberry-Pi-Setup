# Lab: Introduction to Raspberry Pi

In this lab, you’ll tackle your first project with the Raspberry Pi. Unlike most computers, the Raspberry Pi does not have an operating system installed on its hard drive. You’ll have to do this yourself.

## Lab Objectives:

By the end of this lab, you will be able to:
- Install and configure a Linux Operating System
- Define the functions of an Operating System
- Navigate the computer's file system at the command line

# Raspbian OS

Without an operating system, the Raspberry Pi is a blank machine. Computers require an operating system like the Mac OS or Windows to run the hardware of the machine. You can explore the various pieces of the Raspberry Pi hardware at http://vanillawebdiet.com/demos/raspberry.html. 

The operating system (or OS) that will drive the hardware is called Raspbian. Raspbian is a version of the Debian Linux OS (https://www.debian.org/) that has been configured specifically for the Raspberry Pi. 

<blockquote>Q1: What operating systems are you most familiar with? What aspects of the OS do you find to be most useful? What differences have you noticed between operating systems, if any?</blockquote>

You will start with a SD card preloaded with NOOBS (New Out of the Box Software), an installer for the Raspbian OS. Raspbian is based on the Debian Linux OS https://www.debian.org/.

<blockquote>If you do not have NOOBS and Raspbian pre-installed on your SD card, follow these instructions: “Installing Raspbian Using NOOBS” https://www.raspberrypi.org/learning/noobs-install/worksheet/.</blockquote>

If you run into problems along the way, try consulting:
-	Raspberry Pi Troubleshooting Guide https://www.raspberrypi.org/learning/troubleshooting-guide/
-	Raspberry Pi Documentation https://www.raspberrypi.org/documentation/

# Install the Heatsinks

These small pieces of metal help to dissipate the heat generated by the CPU (central processing unit)  and the GPU (graphics processing unit).

Laptop or desktop computers use a fan for this purpose. 

Watch the video at https://youtu.be/PiG-jyDq1po for install instructions.

[IMAGE]
Image from: http://images.nsioutlet.com/product/nt_020804-0006j_c2a.jpg

# Installing Raspbian With NOOBS

<blockquote>NOOBS: new out-of-the-box software</blockquote>

If you have a SD card pre-loaded with NOOBS and Raspbian, then you are ready to turn on your Pi. Before plugging in your Pi, be sure to insert your SD card into your Pi and connect your monitor, keyboard, and mouse.

[IMAGE]

The first time you turn on your Raspbery Pi, you will be greeted with a prompt from NOOBS. Select the Raspbian OS by clicking on the box next to the Raspbian Icon. 

Select the language and keyboard you want to use for the installation.

Click INSTALL at the top of the screen to start the installation process.

[IMAGE]

Click Yes in the pop-up window to proceed.

This Warning is simply a failsafe in case you have already installed an OS on your Pi. It is simply warning you that anything on your Pi will be erased and replaced by this installation of Raspbian. As you do not have anything installed on your Pi, it is ok to click YES to proceed.

[IMAGE]

When the installation is complete, a dialog box will appear announcing the successful installation of the OS.

Click Ok on the pop-up window.

[IMAGE]

Watch your Pi run through its first Boot Sequence.

The Boot Sequence is the process that takes place when a PC is turned on and performs the routines necessary to get all the components functioning properly and the operating system loaded.  You’ll see this screen every time you turn on your Pi.

## Configuring Raspbian

[IMAGE]

Click on the Menu button, then scroll down to Preferences, and click on Raspberry Pi Configuration.

### System Tab

Set up a password for your Pi. This is the password you will use to log in when your Pi boots up.

Click Change Password.

Enter the password you would like to use, and confirm.

Click Ok.

Your default username is "Pi."

### Localisation Tab

Now we need to set our time zone and a few other details. The Pi is a British computer, so all of the defaults are set to British English.

#### Click Set Locale.

Change the country to USA.

Leave the character set at UTF-8.

Click Ok.

#### Click Set Timezone.

Set the Area to US. Set the location to Central.

Click OK.

#### Click Set Keyboard

The Keyboard layout should be set to the United States in the left column.

Select your keyboard type.

Click the X at the top of the WIndow to close the keyboard options.

<blockquote>Q2: Why would it be important to ensure your keyboard is set to the correct type?</blockquote>

#### Set WiFi Country

Select US from the Wifi Country Codes.

<blockquote>WiFi networks use radio waves to transmit information across wireless networks. However, Wi-Fi isn’t the same in every country. International regulatory agencies limit Wi-Fi to different parts of the radio frequency spectrum. In the US, the Radio Frequency Management Division of the National Oceanic and Atmospheric Administration manages the RF spectrum. http://www.cio.noaa.gov/rfm/index.html</blockquote>

[IMAGE]

You will now be prompted to reboot your Pi. Select Yes.

## Connecting to WiFi

<blockquote>If you prefer to connect via Ethernet, simply insert the cable into the port on the side of the Pi. This is often the more reliable way to connect to the Internet when on campus.</blockquote>

[IMAGE]

Click the network icon on the Desktop (located in the top right-hand corner).

Select your preferred WiFi network.

Enter your password if prompted.

# Exploring Raspbian

The Rasbian Graphical User Interface (GUI) will now launch. The desktop should look familiar. The GUI is a method of controlling software using onscreen icons, menus, dialog boxes, and objects that can be moved or resized, usually with a pointing device such as a mouse.  The GUI is usually contrasted with the Command Line Interface (CLI).

Now you can take some time to explore Raspbian and the default software package. You will find many standard applications that are included with operating systems.

<blockquote>Q3: How is Raspbian similar to the operating system on your PC or Mac? How is it different? What software is pre-packaged with the OS? How do you navigate the system and applications?</blockquote>

# Updating Software and Working at the Command Line

[IMAGE]

Open a Terminal session to work at the command line. To access the Terminal, click on the icon at the menu bar. You can also click Menu > Accessories > Terminal.

[IMAGE]

This is the command-line interface.

From here, you can access all of the files and applications in the computer, without the limitations of the graphical interface (GUI) that you usually interact with. 

This interface also referred to as the shell. 

<blockquote>SHELL: shell is the user interface for accessing all of the operating system’s services and applications. The shell is the layer of code surrounding the operating system kernel. The Unix shell is referred to as BASH or “Bourne-again shell,” replacing the Bourne shell. BASH is the command processor that typically runs in the CLI (command-line interface) as opposed to the GUI interface that we used earlier.</blockquote>

## The Anatomy of the Terminal

The console is the system as a whole. This includes both the command line and the output from pervious commands. The command line is the line where you enter commands. The prompt is the beginning of the command line. It usually provides some contextual information about where you are in the system (e.g. the file path). The prompt typically ends in an $. The prompt will also include your user name (Pi, in this case) @ root or the top most directory in the system (also, Pi). 

The terminal is the interface to the consol. This program is a “terminal emulator,” simulating the experience of typing into an ‘old school’ terminal from our contemporary GUI. 

<blockquote>Q4: Open a Terminal on your laptop or desktop. How does the prompt compare? What is your user name? What is the root?</blockquote>

## Update the OS

At the Terminal, type the command `sudo apt-get update` and press the enter key.

<blockquote>You cannot use the mouse to navigate on this screen. Use the keyboard to type the commands and the ENTER key to execute commands. You can scroll using the mouse and scroll bar on the right side of the Terminal window.</blockquote>

<blockquote>You may also use the COPY and PASTE functions to copy code, but use caution when copying code from unknown sources on the web. This code may contain errors and bugs that can crash or corrupt your system. It is good practice to type in the code yourself.</blockquote>

After the system is done working, type the command `sudo apt-get upgrade`.

When asked if you would like to continue hit Enter or type Y and Enter. 

In this case the Y is capitalized indicating that it is the default response if you just press the <Enter> key.
  
Your Raspbian software is now updated. 

You can and should perform this series of commands on a regular basis to ensure that your software is up-to-date. (We will automate this process in the upcoming weeks).

## Navigating the Command Line

Using `sudo` allows us to act as the super user and access to the entire operating system. 

We use `sudo` so that we do not navigate the OS as a super user all of the time, adding a layer of security and preventing unexpected and accidental fatal errors. 

For more on why sudo is used see http://www.techrepublic.com/blog/linux-and-open-source/do-you-sudo-learn-the-basics/.

<blockquote>Q5: Consider the first command that we ran `sudo apt-get update`, try running the command without the leading sudo. What happens? Why?</blockquote>

We will revisit `apt-get update` and `apt-get upgrade` in future projects. 

These two commands in tandem download the update the OS files and then install the downloaded updates.

### Other Commands

Let’s try a few other commands. We will also revisit these commands over the next few weeks as we continue to work with the Pi. If you have questions about the commands and what they do, visit https://explainshell.com/.

You can also learn more about working at the command line through Julia Evans' "Bite Size Command Line" zine.

Many commands follow a similar pattern with 3 parts: 
1- the program
2- the options,
3- the arguments. 

Let's use `ls -l ~` as an example.

Think of the program as the verb in a sentence. 

In this case, `ls` is the program. It is short for list and will show you a list of files in the current directory. 

Try running this program now.

Think of options as adverbs in a sentence. They will modify the way the program runs.

In this example `–l` is the option; it is short for “long.” 

This displays the same list of files with additional information. 

For a full list of all of the options for the `ls` command see http://linuxcommand.org/man_pages/ls1.html

<blockuote>Q6: Can you decipher the information that is displayed? Watch https://youtu.be/LAwmynJHU24 to help decode the information.</blockquote>

The final part of the command (the argument) can be thought of as the object of the sentence. 

In this case, `~` represents the home directory.

Try the same command substituting `Desktop` for the `~`. 

You will now see the contents of the Desktop directory. Nothing is here yet, because you haven’t created any new files on your desktop.

<blockquote>Q7: Try using the same command with desktop. What happens?</blockquote>

<blockquote>Q8: Open the word processing program on the Pi, create a new file, and save it to the Desktop. Now re-run the command ls -l Desktop at the Terminal.
What do you see?</blockquote>

Now let’s change the directory. 

The `cd` command allows you to move through the file system. 

This is comparable to moving through the files and folders in the GUI. You can run the `cd` command from anywhere in the file system.

Run the `cd` command. 

Now run the `ls` command. 

Have you moved anywhere? 

Running `cd` without an argument takes you to the home directory by default. This is the same as running the command `cd ~`.

Now, let’s add an argument to the command. 

Try `cd Desktop`. 

Now run the `ls command`. 

What do you see now? You are now looking at the files and folders within the `Desktop` directory.

<blockquote>Q9: Your command prompt has changed. What information is in the prompt now? Is this useful?</blockquote>

Now, try `cd ..` (that is a double period). 

The `..` is a shortcut to the directory “above” the current directory or the parent directory. 

You should now be back in your home directory. 

The `..` moves you one step up the folder hierarchy. 

It just so happens that the home directory is the parent directory of the Desktop.

<blockquote>Q10: How does this method of navigation compare to how you usually access the files and folders on your computer?</blockquote>

### Where am I? 

Now that we know how to move around the file system, we need a way to check where we are. 

The `pwd` command will “print the working directory,” or show you the file path to your current directory.

<blockquote>Is your command line too cluttered? Use the `clear` command to clear the screen.</blockquote>

### Command Line Troubleshooting

While there are many places to turn for help (your classmates, your instructor, the all-knowing Google), the Terminal is also equipped with a help manual. 

The manual is accessed using the `man` command.

Use the `man` command by itself. What happens?

The command is searching for an argument. 

Try `man ls`. 

The command will return a full description of the command, the available options and its use. 

Use the up and down arrow keys to navigate the manual page.

Type `q` to quit.

The `man` command can be used for any command. 

The command `man man` will provide the help page for the `man` command.

We will continue to learn more commands as we work through future projects. 

If you’d like some more practice, try the exercises at:

-	The Programming Historian: Introduction to the Bash Command Line http://programminghistorian.org/lessons/intro-to-bash
-	Learn Code the Hard Way: The Command Line Crash Course http://cli.learncodethehardway.org/book/

<blockquote>Q11: Take a few moments to reflect on your experience. How does your navigation of the computer at the command line compare other ways of navigating a computer’s user interface?</blockquote>

# Lab Questions

All of the required questions are listed here for you to reference. Be sure to answer each question completely, including an explanation of how you arrived at your answer.

- Q1: What operating systems are you most familiar with? What aspects of the OS do you find to be most useful? What differences have you noticed between operating systems, if any?

- Q2: Why would it be important to ensure that your keyboard is set to the correct type?

- Q3: How is Raspbian similar to the operating system on your PC or Mac? How is it different? What software is pre-packaged with the OS? How do you navigate the system and applications?

- Q4: Open a Terminal on your laptop or desktop. How does the prompt compare? What is your user name? What is the root?

- Q5: Consider the first command that we ran `sudo apt-get` update, try running the command without the leading sudo. What happens? Why?

- Q6: Can you decipher the information that is displayed? Watch https://youtu.be/LAwmynJHU24 to help decode the information.

- Q7: Try using the same command with `desktop`. What happens?

- Q8: Open the word processing program on the Pi, create a new file, and save it to the Desktop. Now re-run the command `ls -l Desktop` at the Terminal. What do you see?

- Q9: Your command prompt has changed. What information is in the prompt now? Is this useful?

- Q10: How does this method of navigation compare to how you usually access the files and folders on your computer?

- Q11: How does your navigation of the computer at the command line compare other ways of navigating a computer’s user interface?
