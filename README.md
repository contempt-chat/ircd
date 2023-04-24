# Changelog
* [SASL authentication](doc/sasl.md) with or without cloaked hostname; SASL account name is distributed in UNICK and shown in WHOIS
* New channel mode 'r' which allows only SASL authenticated users to join (old reop mode for !channels has been removed, exception for +I and manually invited users)
* New user mode 'R' which allows only SASL authenticated users to message this user
* New service flag to prepend IRCv3 message tags @account=&lt;SASL-account-name&gt; and @uid=&lt;UID-nick&gt; to SQUERY messages
* [WHOX](doc/whox.md)
* [Extban](doc/extban.md)
* New command "FORCENICK" which allows services to change the nick of users, even if the nick is already in use or temporarily unavailable
* Allow services to TKLINE / UNTKLINE via ENCAP
* S-Line can be used to grant permissions to remote services, example:
  
  if an IRC server wants to allow "OperServ" on hub.server to (UN)TKLINE remotely, the following S-Line must be added: S|x||OperServ@hub.server|0x00100000|

  SERVLIST shows those permissions in a new field  
<br>

* Hide idle time for opers (requested by doni)
