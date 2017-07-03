# SuchZNC - ZNC Bot
A ZNC bot capable of handling registeration requests of new ZNC accounts, and more.

## Features
* The ability to request for a ZNC account (!request)
* The ability to approve or deny new ZNC account requests (!approve or !deny)
* The ability to delete ZNC accounts in the IRC channel (using the -delznc argument in !deluser)
* Muti-language support, including the ability to set the specified language for each indiviual user (!userlang for indiviual language)

## Requirements
* Python 3.4 or newer
* Admin access to a working ZNC server

## Configuration help
**zncuser** - The username of the ZNC account for the bot to use.
<br>
**server** - The ZNC server the bot will be connecting to.
<br>
**port** - The IRC port the ZNC server is using (Add a + for SSL, something like +6697, as an example.)
<br>
**admins** - The list of user@host that are granted admin privileges on the bot, such as ["example@foobar.net", "quack@ducks.net"]
<br>
**network** - Used for specifying which network will the bot use, when it authenticates itself to the ZNC.
<br>
**zncpass** - The ZNC Bot's account password.
<br>
**language** - The default language the bot will speak in, on IRC. (Select "en" for English, LOOKING FOR TRANSLATORS FOR MORE LANGUAGES)
<br>
**webpanel** - Where the ZNC webpanel is located, so they will know when they request for an account.
<br>
**znchost** - The ZNC bindhost to set when the user gets approved, set it to an asterisk if you don't have a specific IP or host to use, or if you are not sure.
<br>
**torhs** - The ZNC's Tor Hidden Service Address, leave blank if you don't have one.
<br>
**zncircserver** - The ZNC address your users will connect to, this will be given to them when they register.
<br>
**zncssl** - The SSL IRC port for ZNC, incase you have a configuration where you splitted the SSL and non-SSL ports (like how 6667 isn't SSL, but 6697 is), otherwise, leave blank.
<br>
**zncstandard** - Same thing as the zncssl config, but this time, for the standard ZNC irc port, without SSL. If you left zncssl blank, then you probably should have this blank too.
<br>
**zncircport** - The ZNC IRC port that your users will be using, do not use this if you have SSL and non-SSL seperated, but instead, instead use zncssl and zncstandard.
<br>
**zncircportisssl** - States if the port supports SSL connections, Put in "True" if so, "False" if not (Make sure you keep the quotes with it too.)
<br>
**use_identify-msg** - (Requires the IRC network to support it, and the bot to have send_raw module enabled) If set to "True" (Including the quotes), the bot will require users to be identified to services.

## Setup requirements
* Make sure to create a "cloneuser" account, this account will be used for the bot to clone for each new user, that way, you can specify certain stuff for each new user, like a custom realname, or quit message, or whatever the case may be.
* Make sure every ZNC user have "DenySetBindHost" enabled, otherwise approving would be useless.
* Make sure the ZNC bot have Admin privileges on the ZNC server (Duh)
* In order for the bot to even work...at all, it requires the controlpanel module to be enabled. This will be used to basically do everything it needs to do, like create new accounts, set bindhosts, etc.

## Still need help? Need to contact?
Join the IRC channel #SuchZNC @ freenode for help, bug reporting, or contributions, or whatever the case may be.