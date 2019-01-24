The command below will use tccprofile.py to generate a whitelist profile with the following characteristics:

Able to send restricted AppleEvents:

Microsoft Outlook.app - Send AppleEvents to Skype for Business.app
Skype for Business.app - Send AppleEvents to Microsoft Outlook.app

Command used with tccprofile.py to generate the profile:

/path/to/tccprofile.py --apple-event "/Applications/Microsoft Outlook.app","/Applications/Skype for Business.app" "/Applications/Skype for Business.app","/Applications/Microsoft Outlook.app" --allow --payload-description="This profile allows Microsoft Outlook and Skype for Business to send notifications to each other." --payload-identifier="com.company.microsoft.outlook.skype.tcc.privacy.whitelist" --payload-name="Privacy Settings Whitelist - Microsoft Outlook and Skype for Business" --payload-org="Company Name" --payload-version="1" -o Microsoft_Outlook_and_Skype_for_Business_Notifications_v1.mobileconfig
