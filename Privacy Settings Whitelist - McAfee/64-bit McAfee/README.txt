The command below will use tccprofile.py to generate a whitelist profile with the following characteristics:

Full Disk Access:

/Library/Application Support/McAfee/MSS/Applications/Menulet.app
/usr/local/McAfee/fmp/bin64/fmpd

Note: /usr/local/McAfee/fmp/bin64/fmpd is the 64-bit McAfee file scanner.

Able to send restricted AppleEvents:

/Library/Application Support/McAfee/MSS/Applications/Menulet.app - Send AppleEvents to SystemEvents, SystemUIServer and Finder

Command used with tccprofile.py to generate the profile:

/path/to/tccprofile.py --allfiles "/Library/Application Support/McAfee/MSS/Applications/Menulet.app" /usr/local/McAfee/fmp/bin64/fmpd --apple-event "/Library/Application Support/McAfee/MSS/Applications/Menulet.app","/System/Library/CoreServices/System Events.app" "/Library/Application Support/McAfee/MSS/Applications/Menulet.app","/System/Library/CoreServices/SystemUIServer.app" "/Library/Application Support/McAfee/MSS/Applications/Menulet.app","/System/Library/CoreServices/Finder.app" --allow --payload-description="This profile allows specified applications to display information to the logged-in user." --payload-identifier="com.company.mcafee.tcc.privacy.whitelist" --payload-name="Privacy Settings Whitelist - McAfee" --payload-org="Company Name" -o McAfee_All_Files_and_Notifications_v2.mobileconfig
