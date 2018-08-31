The command below will use tccprofile.py to generate a whitelist profile with the following characteristics:

Full Disk Access:

/Library/Application Support/JAMF/Jamf.app
/usr/local/jamf/bin/jamfAgent
/usr/local/jamf/bin/jamf

Able to send restricted AppleEvents:

/Library/Application Support/JAMF/Jamf.app - Send AppleEvents to SystemEvents, SystemUIServer and Finder
/usr/local/jamf/bin/jamfAgent - Send AppleEvents to SystemEvents, SystemUIServer and Finder
/usr/local/jamf/bin/jamf - Send AppleEvents to SystemEvents, SystemUIServer and Finder

Command used with tccprofile.py to generate the profile:

/path/to/tccprofile.py --allfiles "/Library/Application Support/JAMF/Jamf.app" /usr/local/jamf/bin/jamfAgent /usr/local/jamf/bin/jamf --appleevents "/Library/Application Support/JAMF/Jamf.app","/System/Library/CoreServices/System Events.app" "/Library/Application Support/JAMF/Jamf.app","/System/Library/CoreServices/SystemUIServer.app" "/Library/Application Support/JAMF/Jamf.app","/System/Library/CoreServices/Finder.app" /usr/local/jamf/bin/jamfAgent,"/System/Library/CoreServices/System Events.app" /usr/local/jamf/bin/jamfAgent,"/System/Library/CoreServices/SystemUIServer.app" /usr/local/jamf/bin/jamfAgent,"/System/Library/CoreServices/Finder.app" /usr/local/jamf/bin/jamf,"/System/Library/CoreServices/System Events.app" /usr/local/jamf/bin/jamf,"/System/Library/CoreServices/SystemUIServer.app" /usr/local/jamf/bin/jamf,"/System/Library/CoreServices/Finder.app" --allow --payload-description="This profile allows specified applications to display information to the logged-in user." --payload-identifier="com.company.jamf.tcc.privacy.whitelist" --payload-name="Privacy Settings Whitelist - Jamf" --payload-org="Company Name" --payload-version="1" -o Jamf_All_Files_and_Notifications_v1.mobileconfig