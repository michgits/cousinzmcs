### Server Specs:
- **OS:** Debian GNU/Linux 10 (buster) x86_64
- **RAM:** 8GB to 16GB
- **Location:** Based on your physical location.
- **Storage:** Approx 5GB
- **CPU:**  AMD EPYC (2) 7B12 @ 2.249GHz or Intel Xeon (4) @ 2.199GHz

You can view your exact specs by doing `./specinfo`

### Service Used:
- [playit.gg](https://playit.gg)
- [console.cloud.google.com](https://console.cloud.google.com)

## Installation 
* Activate a [Google Cloud Shell](https://console.cloud.google.com/) on Google cloud.
* Clone this GitHub Project into the Console:
```
git clone https://github.com/michgits/cousinzmcs
```
* Go into `mcserver` directory:
```
cd cousinzmcs
```
* Allow all commands executable:
```
chmod +x *
```
* Run the Installation Script:
```
./install
```
Follow the installation step shown in the console
* Run the Start Server Script:
``` 
./startserver
```
(You only need to do this if you chose `No`.)

## Java Server Additional Setup (You can skip this part)
*(This only applies to Java Servers including Nukkit or the EULA script didn't work for you.)*

If you first start up your server, it will fail to start because you need to accept the **EULA** to run properly.

* Go to the server directory and accept the [EULA](https://www.minecraft.net/en-us/eula)
```
cd server
```
```
nano eula.txt
```
* Be sure that `eula.txt` contains the following text below:
```
eula=true
```
Do `Ctrl + W` then press `Y` to save and press `Enter` exit the text editor.
* Go back to the main directory:
```
cd ..
```
- And Restart the Server.
* Now everything should be functional and ready. You can check if your server is up and running by doing `screen -r server`.
## Joining your Server
* To join your server, start your server by doing `./startserver` *(If you haven't started it yet)* and do this command:
``` 
screen -r playit
```
- Now click the **Claim URL** and it should show you your host IP and Tunnel Server.
- Once your in that page, scroll down and click **Add Tunnel** on Minecraft Java/Bedrock and next to the **Local server address**, click **Add**.
- Now copy the generated dedicated IP something along with `auto.playit.gg` and copy it into the Server Address in Minecraft and now you can play the server.

*(Note: If you want to change the Claim URL, you need to Stop the Server. This will reset your server IP.)*

## Accessing Server Console
* To access your server console, open this following session:
```
screen -r server
```
To completly stop the server, you can do `./stopserver` on the Linux console or do `exit` or `stop` on the Minecraft console

## Detaching Screen/Session
* To Detach the session you can do it using the following keyboard shortcuts 
`CTRL + A` then press `D`

## Third-Party Launcher
* If you are using like a cracked version of **Minecraft Java Edition**

Example: [Tlauncher](https://tlauncher.org/en/)

- Go to `server.properties` and find the properties `online-mode`:
```
nano server.properties
```
- Change it from `true` to `false`
```
online-mode=false
```
Do `Ctrl + W` then press `Y` to save and press `Enter` exit the text editor.

- Restart your server after you apply these changes.
