# Simplified auth
This is server sided babric modification for Better Than Adventure that allows for authorization using ingame commands, such as /register or /login
<br/>
In current form only possible to use JSON file based "database". Sessions are supported.
## Licenses
Libraries used in this project are using:
- jBcrypt (MIT): https://github.com/jeremyh/jBCrypt
- halplibe (CC0): https://github.com/Turnip-Labs/bta-halplibe
## Setup
1. Mod to work would require working server instance of Babric BTA server ([available here](https://github.com/Turnip-Labs/babric-instance-repo/releases)) with halplibe version at least 3.2.1 (which was by default included in BTA instance) installed.<br/>
2. Don't forget about read/write privileges on server directory and any other directory specified by config (by default should be available for server but still, this can sometime happen)

## Config
Currently config allows for setting only 
- DatabaseManager -specifies which database engine would be used for storing player data (currently only JSON file).
- Address - when specified json dbmanager, Address would point to directory where "database" file would reside.
- Schema - when specified json dbmanager, it would point at name of json file that would store usernames and encrypted passwords.
- SessionLife - session lifetime in hours (default is 48). Available as an integer. If you specify -1, the session time will be unlimited (not recommended).
Modification in json manager mode should by default create required paths and files. 
