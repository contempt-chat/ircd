# Changelog
* SASL authentication with or without cloaked hostname; SASL account name is distributed in UNICK and shown in WHOIS
* New channel mode 'r' which allows only SASL authenticated users to join (old reop mode for !channels has been removed)
* New user mode 'R' which allows only SASL authenticated users to message an user
* New command "FORCENICK" which allows services to change the nick of users, even if the nick is already in use or temporary unavailable
* New service flag to prepend IRCv3 message tags @account=<SASL-account-name> and @uid=<UID-nick> to SQUERY messages
* New service flag to allow to TKLINE / UNTKLINE via ENCAP

* hide idle time for opers (requested by doni)
* global &clients channel (requested by mxl)
