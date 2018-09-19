The command below will use tccprofile.py to generate a whitelist profile with the following characteristics:

Full Disk Access:

/Library/Application Support/JAMF/Jamf.app
/usr/local/jamf/bin/jamfAgent
/usr/local/jamf/bin/jamf

Command used with tccprofile.py to generate the profile:

/path/to/tccprofile.py --allfiles "/Library/Application Support/JAMF/Jamf.app" /usr/local/jamf/bin/jamfAgent /usr/local/jamf/bin/jamf --allow --payload-description="This profile allows specified applications access to specified filesystem locations." --payload-identifier="com.company.jamf.fileaccess.tcc.privacy.whitelist" --payload-name="Privacy Settings Whitelist - Jamf" --payload-org="Company Name" --payload-version="1" -o Jamf_All_Files_v1.mobileconfig