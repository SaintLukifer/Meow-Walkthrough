# Meow-Walkthrough
Meow Walkthrough
#Log in
    *Put in UserName and Password

#Connect to vpn Step 1
    *Click Connections in top right
    *Click Starting Point under Machines   
    *Select VPN ACCESS location you are in (US)
    *Select VPN SERVER - US StartingPoint1, 2, or 3 whichever has the least number of users
    *Select TCP443 
    *Click "Download VPN"

#Connect to vpn Step 2
    *Open downloads file
    *Right click in folder in any open space and select _open terminal here_
    *once terminal opens, type Sudo su and put in your password
    *Then type 'ls' to verify file is present
    *Then type 'openvpn (file name of downloaded file from Hack the Box)'
    *Hit Enter

#Hacking the box
    *Open another terminal
        _Click File in the upper left side of the screen and open another terminal_
    *Go to Hack the Box website you already have open and make sure the "Connections" button is green
    *On the Home page of Hack The Box(click the house on the left of the screen if you need to go back from another page on the site) and click on _Starting Point_
    *On the "Learn the basics of Penetration Testing", click on _Tier 0_ and click on the cat image with "Meow" listed under the picture
    *Once the drop down expands, click on "Start Machine" button, can take up to a minute to start up

    *Steps to hack the box
        Task 1 - VM - Stands for Vitual Machine
            _You use a Virtual Machine to open Kali Linux_

        Task 2 - you interact with a Terminal
            _You use a Terminal to put in code to interact_

        Task 3 - Openvpn
            _You used Openvpn to connect to HTB_

        Task 4 - Ping
            _type ping (IP address given by HTB after clicking start Machine)_ in the terminal
            _after 4 connections, hit ctrl "C" to end the running script
            **_Please note, if you are still under your Downloads folder, type 'CD' in the command line to go back to the main folder, if you do not do this it will not work from this point forward_**

        Task 5 - NMap
            _type sudo NMap -sV (IP address given earlier) allow for 2-5 minutes for it to pull information
            _Results in:

            PORT    STATE  SERVICE VERSION
            23/tcp  open   telnet  Linux

            *Because telnet is open use telnet
            _type telnet (IP address given earlier)_ then hit enter

            You will see:
             █  █         ▐▌     ▄█▄ █          ▄▄▄▄
  █▄▄█ ▀▀█ █▀▀ ▐▌▄▀    █  █▀█ █▀█    █▌▄█ ▄▀▀▄ ▀▄▀
  █  █ █▄█ █▄▄ ▐█▀▄    █  █ █ █▄▄    █▌▄█ ▀▄▄▀ █▀█

    Meow login:
        Now type in possible usernames:
            *Administrator
            *Admin
            *root
        Hit enter for password for each one and see it any of those
             this gives the you answer to Task 6   

        Task 6 - root
            _you use root
            *next, once in root, type 'ls' and search for the files under root
            *NOTE you find files that says "flag.txt" and Snap
            _type Cat flag.txt
            _*You are rewarded with a flag:
        
        Task 7 - b40abdfe23665f766f9c61ecba8a4c19
