
# Introduction 
This PowerShell module is intended to interact with data within ImmyBot. To pull information from computers, such as inventory data to load into other systems such as ImmyBot.
# Installing Module
- Copy SPSImmyBot directory to one of your local powershell module directories to have it load automagically into your powershell sessions
OR
- From SPSImmyBot directory run Import-Module .\SPSImmyBot.psd1

# Getting Started
- If running from a Windows machine, you can create and save a new config by running:

```New-SPSImmyBotWindowsConfiguration```

- Follow the instructions in powershell terminal to setup.
- This will save some config files in ```%localappdata%\powershell\SPSImmyBot\$configName\```
- Sensitive info will be encrypted in the secret.xml under the context of the user that created the file.
- You can then run ```Set-SPSImmyBotWindowsConfiguration -Name $ConfigName``` to load your config. This will generate a new token that should be good for somewhere between 60-90 minutes. Everytime you run this command you will get a fresh token that's good for 60-90 minutes.
- You can now run ```Invoke-ImmyApi``` leveraging the Endpoint parameter. Example: ```Invoke-ImmyApi -Endpoint Computers```
- You can use Network tab under Developer Tools in Chrome to find the API calls for anythin within ImmyBot
