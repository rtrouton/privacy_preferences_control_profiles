The command below will use tccprofile.py to generate a whitelist profile with the following characteristics:

Full Disk Access:

/Applications/Enterprise Connect.app
/usr/bin/osascript

Able to send restricted AppleEvents:

/Applications/Enterprise Connect.app - Send AppleEvents to SystemEvents, SystemUIServer and Finder
/usr/bin/osascript - Send AppleEvents to SystemEvents, SystemUIServer and Finder

Command used with tccprofile.py to generate the profile:

/path/to/tccprofile.py --allfiles "/Applications/Enterprise Connect.app" /usr/bin/osascript --apple-event "/Applications/Enterprise Connect.app","/System/Library/CoreServices/System Events.app" "/Applications/Enterprise Connect.app","/System/Library/CoreServices/SystemUIServer.app" /usr/bin/osascript,"/System/Library/CoreServices/System Events.app" /usr/bin/osascript,"/System/Library/CoreServices/SystemUIServer.app" /usr/bin/osascript,"/System/Library/CoreServices/Finder.app" --allow --payload-description="This profile allows specified applications to display information to the logged-in user." --payload-identifier="com.company.apple.tcc.privacy.whitelist" --payload-name="Privacy Settings Whitelist - Apple" --payload-org="Company Name" --payload-version="1" -o Apple_All_Files_and_Notifications_v1.mobileconfig
