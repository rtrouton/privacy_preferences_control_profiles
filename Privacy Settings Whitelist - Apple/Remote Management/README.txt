The command below will use tccprofile.py to generate a whitelist profile with the following characteristics:

Allow Post Event control:

/System/Library/CoreServices/RemoteManagement/ScreensharingAgent.bundle

Used with the kickstart command-line utility on macOS Mojave to allow remote observation and control:

https://support.apple.com/HT209161


Command used with tccprofile.py to generate the profile:

/path/to/tccprofile.py --post-event "/System/Library/CoreServices/RemoteManagement/ScreensharingAgent.bundle" --allow --payload-description="This profile allows Allow Control mode when starting Apple Remote Management via kickstart" --payload-identifier="com.company.appleremotemanagement.tcc.privacy.whitelist" --payload-name="Privacy Settings Whitelist - Apple Remote Management" --payload-org="Company Name" -o Apple_Remote_Management_Control_And_Observe_v1.mobileconfig


