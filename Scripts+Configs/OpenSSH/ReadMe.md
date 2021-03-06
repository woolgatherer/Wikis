### Information Directory ###
---

###### Configs are configured for security & may need to have less secure ciphers/exchanges added for certain SSH servers _(DropBear for instance)_ ###### 


### [BSD/Linux](BSD-Linux) ###
  ###### [_config_](BSD-Linux/config) ######
  - Custom user specific OpenSSH client config, which should be placed at _~/.ssh/config_
  
  - There are three specific sections to this custom config
    - ###### Custom ######
      - Contains user specific options which should be placed in _config_, but not the system wide _/etc/ssh/ssh_config_
    - ###### Hosts ######
      - Contains individual host configurations, allowing user to connect via `ssh <host variable>`, such as `ssh FNr`
    - ###### Options ######
      - Contains options that override the system default ssh_config located at _/etc/ssh/ssh_config_

  ###### [_ssh_config_](BSD-Linux/ssh_config) ######
  - System wide OpenSSH client config, which should be placed at _/etc/ssh/ssh_config_

  ###### [_sshd_config_](BSD-Linux/sshd_config) ######
  - System wide OpenSSH server config, which should be placed at _/etc/ssh/sshd_config_


### [Windows](Windows) ###
###### [_config (Win32-OpenSSH)_](Windows/config%20(Win32-OpenSSH)) ######
- Custom user specific Windows OpenSSH client config, which should be placed at _%USERPROFILE%\\.ssh\config_
  - As of August 2017, this **_must_** be utilized since the Windows binary does not recognize _C:\Program Files\OpenSSH\ssh_config_ (See issue [#847](https://github.com/PowerShell/Win32-OpenSSH/issues/847))

###### [_ssh_config (Win32-OpenSSH)_](Windows/ssh_config%20(Win32-OpenSSH)) ######
- System wide Windows OpenSSH client config, which should be placed at _C:\Program Files\OpenSSH\ssh_config_
  - As of August 2017, the Windows binary does not recognize _C:\Program Files\OpenSSH\ssh_config_ (See issue [#847](https://github.com/PowerShell/Win32-OpenSSH/issues/847))
    - Instead, [config](Windows/config%20(Win32-OpenSSH)) should be utilized and placed at _%USERPROFILE%\\.ssh\config_

###### [_sshd_config (Win32-OpenSSH)_](Windows/sshd_config%20(Win32-OpenSSH)) ######
- System wide Windows OpenSSH server config, which should be placed at _C:\Program Files\OpenSSH\sshd_config_
