  ______                 _                   ______                               _   
 |  ____|               (_)                 |  ____|                             | |  
 | |__     _   _   ___   _    ___    _ __   | |__      ___    _ __    ___   ___  | |_ 
 |  __|   | | | | / __| | |  / _ \  | '_ \  |  __|    / _ \  | '__|  / _ \ / __| | __|
 | |      | |_| | \__ \ | | | (_) | | | | | | |      | (_) | | |    |  __/ \__ \ | |_ 
 |_|       \__,_| |___/ |_|  \___/  |_| |_| |_|       \___/  |_|     \___| |___/  \__|





Thank you for downloading the FusionForest_Server File! With this you can create your own custom FusionForest Servers. It includes both a Mac and Windows Startup.



Universal Information:

- Customize the server.properties file to change many options.
- Customize ore generation in mod specific config files.
- Customize ToolKit MOTD in the config folder.

- Customize the Amount of RAM you are dedicating to the server inside the user_jvm_args.txt. The default I have set is 6-10gb, but anything over 5 should be okay if you only have a few players.



Windows Startup:

- Run the Windows_StartServer.bat

- It should just boot up on most windows machines. If you need to learn about port forwarding, please watch a "How to make a Minecraft server" video on YouTube.




Mac Startup:

- Run the MacLinux_StartServer.sh

- On some Mac Machines this will boot, on others you may need to give it a proper location (which I will cover in a moment).

- If it is telling you to verify "zsh" then you will likely need to update your MacOS to a semi-modern version and then go through the steps to change the default coding language from "bash" (which is what MacOS used to run as its shell), to "zsh" (which new versions of MacOS have switched to. There are plenty of online tutorials on how to do this).

- If you have zsh working and the MacLinux_StartServer.sh still won't boot, we have to edit the script to tell it where to look.

- Open the MacLinux_StartServer.sh inside of a text editing program, instead of running it. 

- There you will see a line that says "java @user_jvm_args.txt @libraries/net/minecraftforge/forge/1.18.1-39.0.5/unix_args.txt"

- We are going to put some new code lines in BEFORE this java command.

- First find where your FusionForest_Server Folder is located. Choosing an easy to reach location like your desktop will make the next step easier and quicker.

- Once you know where the Server folder is, we need to add lines to point terminal where to look.

- Let's say your folder is located on your desktop, then you would add these lines of code IN FRONT/BEFORE the java line. And it would look like this.

cd desktop
cd FusionForest_Serverx.x.x (folder that user_jvm_args.txt is in)
java @user_jvm_args.txt @libraries/net/minecraftforge/forge/1.18.1-39.0.5/unix_args.txt "$@"

- If you do it like that, it should boot up. If you have any questions feel free to swing by the Discord: https://discord.gg/jn8cwHN9TS
