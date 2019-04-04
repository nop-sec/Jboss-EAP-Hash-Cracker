# Jboss-EAP-Hash-Cracker
Hash cracking tool for Jboss EAP 6.4


Will crack hashes for JBoss management realm and application realm stored in the format of hex(md5(user:realm:password))
eg: TestUser=6933117f41efe0c58092ae8d09eb8488

To begin cracking passwords run the script with the -H flag for the property file, -P for the Password List and -r for the realm.
eg: ./Jbos_cracker -P /opt/SecLists/Passwords/10_million_password_list_top_100.txt -r ManagementRealm -H properties

Output:

#########################################################
113 Hashes Loaded
Loading passwords into memory...
215 Passwords Loaded
#########################################################

-----------------------------------
Cracking Started
-----------------------------------
Cracking Passwords for user: TestUser
Password Found: TestUser:jw92y2X^

Due to the format of the hashes it's not that quick to run. Rockyou password list will take about 5 minutes per user to run. The password lists are loaded into memory to increase speed and limit drive IO so make sure you have enough memory for the dictionary used.

