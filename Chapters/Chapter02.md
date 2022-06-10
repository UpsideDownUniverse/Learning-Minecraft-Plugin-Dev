---
Title: 'Initializing Pre-requisites'
published: true
description: Learning Minecraft Plugin Dev - Pre-requisites
id: LMPD012
date: '2022-06-10 14:18 IST'
---
## Initializing Pre-requisites :shipit:

Now that we know what we are going to do, lets start off making things, to begin with, we need to download and install all the pre-requisites that were mentioned in [Chapter 1] that includes Java, IntelliJ IDEA, and the Test Minecraft server.

- - -

## Installing Java

We will be making plugins for Minecraft version 1.19 (The latest version of minecraft available on the date this was written.) which required Java version 17 minimum to run, therefore we need to install Java version 17.

But before we do so, we need to know that some devices come with java pre-installed, to check wether java is installed on your machine, you can head on over to the `Command Prompt` or `terminal` and run the following command.

```
java --version
```

you should get an output like this:  
![ss1](https://insert_link_here.)

we have Java version `17.0.1 2021-10-19 LTS` on our device but,    
NOTE: this may or may not be the same thing for you, in that case, we need to go and install java version 17 from the oracle website.

If you encountered an error such as the one below:  
![ss2](https://insert_link_here.)

Then do not worry, it also means java is not installed on your machine.

> **Warning**  
> If you got an error or have a different version of java on your machine, follow the next section, if not feel free to skip ahead!

- - - 

### Downloading java from the oracle website

If you got an error like the one above, or have a different version of java, then follow this section.

First, head on over to the **[Oracle downloads site](https://www.oracle.com/java/technologies/downloads/#java17)** and choose your operating system and download with your preferred method. Java is currently made for Windows, Linux and MacOS, after that, the installation is pretty straight forward and simple, you just need to click a few "Next" or "agree" buttons and you are set! 🎊 you now have Java installed on your device!

After we are done downloading and installing Java on your device, we need to make sure if java has installed and set the version correctly, to assess this, lets do the `java --version` command in the Command prompt or Terminal one more time.

NOTE: When you do the command given above it might still show the same error as before. This is because Installing Java isn't the only thing we need to do, we have to even set a few environment variables on our device so that windows knows how to use "java" commands.

> **Warning**  
> If you are one of the people who got an error at this point, follow the next section, if not skip to the next section!

- - -

### Setting java Environment Variables

If you got a similar error in the last section after installing java, read this section, if not, feel free to skip ahead!

Now let us find out how to set up the environment variables on our machine,

NOTE: We are setting environment variables on a Windows machine, but the links on how to do the same on Linux and MacOS is given at the end of this section!

Setting Environment Variables:  
First open windows search and search for "Environment Variables" you should see an option called "Edit the system Environment Variables" there, click on that.

![ss3](https://insert_link_here.)

Then click on the "Environment Variables..." button,

![ss4](https://insert_link_here.)

Here you should see 2 windows "User variables for user" and "System variables", we need to focus on system variables for now. Here, click on "New..." and enter the following details:

```
Variable name: JAVA_HOME
Variable value: {Path to your java folder.}
```

A quick tip here is to use the "Browse directory" button to choose your path.  
The most common path that java will be installed at is `"C:/Program Files/Java/jdk-17.0.1"` so we would suggest you check and select the correct folder.

after you are done selecting, you should have something like this:  

![ss6](https://insert_link_here.)

once you are done, click "Ok: and then double click on the "Path" item in the list.  

![ss7](https://insert_link_here.)

over here click "New" and type the following `"%JAVA_HOME%\bin"`, after you are done, find an item on the same list which is along the lines of `"C:\Program Files\Common Files\Oracle\Java\javapath"` click on it and press "Delete".

You don't need to worry about that, as sometimes when that variable is the same, it might use a different version of java instead of the latest one.

after you are done with the above, click "Ok" and exit out of everything by clicking "Ok" two more times 😂

Now we are all set!

Once again, let us check if everything is working by typing `java --version` in the Command prompt, you should see the version of java you have on your machine now.

If not, feel free to DM me the error message and I will get back to you on it!

- - - 

Links for setting environment variables on Linux and MacOS:
- **[Linux](https://www.ibm.com/docs/sl/b2b-integrator/5.2?topic=installation-setting-java-variables-in-linux)**
- **[MacOS](https://mkyong.com/java/how-to-set-java_home-environment-variable-on-mac-os-x/)**

- - -

Now that we have java installed, we can go on to the next task, that is to create a spigot minecraft test server on our device! 🌟

- - -
## Making a **Spigot Minecraft server**

We will be setting up a `spigot` minecraft server, but what is spigot?  

The most popular Minecraft server software is called Spigot. Spigot is an open-source Java project that lets users run their own Minecraft server and add plugins to extend the possibilities of their server. There are over 100,000 Spigot servers in existence today.

But what about the other versions of server software?

Most of the other server softwares are Forked repositories of the original Spigot repo, hence the plugin you make for a Spigot server, will mostly work on all other versions of servers.

### Now lets get back to making the server!

To make a spigot server we need to get the latest spigot.jar file, spigot provides their latest version of jar file on their CI/CD server, which is called Jenkins, we can download the latest patch of build tools from here.
to download spigot head on over to **[spigotmc.org - Buildtools](https://hub.spigotmc.org/jenkins/job/BuildTools/)** and click on "BuildTools.jar" which is right under "Last Successful Artifacts" as soon as you click on it, it will download a buildtools.jar file.

(I have downloaded a previous version of buildtools, hence it is showing me BuildTools (1).jar, but do not worry, it is the same thing!)  
![ss8](https://insert_link_here.)

After you download this, your browser might flag this file as "potentially harmful" just click on options and select "Keep" because I assure you, this file is not at all harmful to your machine!

After you have downloaded the file successfully, you can go ahead and make a directory/folder on your drive and drag and drop this .jar file into it.
NOTE: We will be using this file a lot from now on, so I suggest you select a calm corner place on your device to put the file in! 😆

Now lets open Command prompt or terminal again and then get into this directory 👍

```
If you do not know how to change directories on Command prompt or terminal just do the following:

> cd {Path to the directory you want to get into.}
```

after you are in that folder, run the following command:
```
> java -jar .\BuildTools.jar --rev latest 
```

Now the spigot installer  will run, and this will take a while like a long while because it has to download all the files from the online spigot repository and unpack it.

Go on now, take a break, get some coffee ☕ and let the file do its thing...

- - -

Once the file is downloaded, feel free to close the Command Prompt or terminal and head on over to the file.

NOTE: sometimes the jar may not install because the machine might be using the wrong version of jar. And sometimes the jar file might install a different version of spigot, if that is the case, then in the command we used above change `latest` to `{version}` in our current case `1.19`.

```
> java -jar .\BuildTools.jar --rev 1.19
```

Once you have checked and verified that the correct version is installed.
make a new folder called "mc_server", this is where we will launch the server.

- - - 

### Launching the Minecraft server

to launch the server we need to take the `spigot-1.19.jar` file and put into the newly created folder.

once we do this, we need to run it, but instead of directly clicking on the jar, we have a different way of running it.

### Windows:
1. Paste the following text into a text document. Save it as start.bat in the same directory as spigot.jar:

```
@echo off
java -Xms#G -Xmx#G -XX:+UseG1GC -jar spigot.jar nogui
pause
```
**NOTE: # is your allocated server memory in GB**

2. Double click the batch file.

- - -

### Linux:
1. Create a new startup script (start.sh) in the server directory to launch the JAR:
```
#!/bin/sh

java -Xms#G -Xmx#G -XX:+UseG1GC -jar spigot.jar nogui
``` 
**NOTE: # is your allocated server memory in GB**

2. Open your terminal and execute the following in the directory:
```
chmod +x start.sh
```
3. Run your start up script:
```
./start.sh
```

- - -

### Mac OS X
1. Create a new startup script (start.command) to launch the JAR in the server directory:
```
Code (example (Unknown Language)):
#!/bin/sh

cd "$( dirname "$0" )"
java -Xms#G -Xmx#G -XX:+UseG1GC -jar spigot.jar nogui
```
 **NOTE: # is your allocated server memory in GB**

2. Open Terminal and type into it: (Don't hit enter!)
```
chmod a+x
```
3. Drag your startup script file into the Terminal window. (Be sure to put a space between chmod a+x and your startup script!)
4. Double click your startup script.

- - -

Once we are done with this much, we have reached a good point! ☕ We now have java installed, and a working minecraft server to use, But how to use it?

to run your minecraft server, just double click the `start.bat` file that we created and java will do the rest of the magic by itself! but one thing to note is if you start the minecraft server for the first time, you need to go to a pre-generated text file that is `eula.txt` and change `eula=false` to `eula=true`, this process repeats only if you are launching a new server. after you change false to true, save the file and exit out, and run `start.bat` again!

- - -

You are all set!, the only thing remaining is an IDE, you can use any IDE to edit java, but we suggest using IntelliJ IDEA as it is now crowned the best java editor out there 👑

To install IntelliJ IDEA head on over to **[IntelliJ IDEA download](https://www.jetbrains.com/idea/download/)** and download your preferred installation. the installation of IntelliJ is also quite straight forward, just a bunch of "Next" and you will be ready to use intelliJ in no time!

- - -

## Useful Links:
- ### **[Setting Environment vars in other OS](https://www.codejava.net/java-core/set-java-home-in-macos-linux)**
- ### **[Starting a spigot server](https://www.spigotmc.org/wiki/spigot-installation/)** 
