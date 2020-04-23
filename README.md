
# ADFSpray

ADFSpray is a python3 tool to perform password spray attack against Microsoft ADFS.
ALWAYS VERIFY THE LOCKOUT POLICY TO PREVENT LOCKING USERS.

Currently this has been tested against autodiscover host (under NTLM authentication):

https://autodiscover.[COMPANY].com/autodiscover/autodiscover.xml

## How to use it
First, install the needed dependencies:
```
pip3 install -r requirements.txt
```
Run the tool with the needed flags:
```
python3 ADFSpray.py -u [USERNAME] -p [PASSWORD] -t [TARGET URL] [METHOD]
```

## Options to consider
* adfs|autodiscover|basicauth
  * the method of authentication to use, autodiscover uses NTLM, adfs is MicrosoftForm and basic auth is well...basic authentication
* -p\\-P
  * single password or file with passwords (one each line)
* -t\\-T
  * single target or file with targets (one each line)
* -u\\-U
  * single username or file with usernames (one each line)  
* -o
  * output file name (csv)
* -s
  * throttling time (in seconds) between attempts
* -r
  * random throttling time between attempts (based on user input for min and max values)

### Credit
Inspired by https://github.com/Mr-Un1k0d3r/RedTeamScripts/blob/master/adfs-spray.py

### Issues, bugs and other code-issues
Yeah, I know, this code isn't the best. I'm fine with it as I'm not a developer and this is part of my learning process.
If there is an option to do some of it better, please, let me know.

_Not how many, but where._
