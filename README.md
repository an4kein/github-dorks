# github-dorks

[Top 4 ways to scan GitHub repos for credentials](https://securitytrails.com/blog/github-dorks)


| Dork                                            | Description                                                                                 |
|-------------------------------------------------|---------------------------------------------------------------------------------------------|
| filename:.npmrc _auth                           | npm registry authentication data                                                            |
| filename:.dockercfg auth                        | docker registry authentication data                                                         |
| extension:pem private                           | private keys                                                                                |
| extension:ppk private                           | puttygen private keys                                                                       |
| filename:id_rsa or filename:id_dsa              | private ssh keys                                                                            |
| extension:sql mysql dump                        | mysql dump                                                                                  |
| extension:sql mysql dump password               | mysql dump look for password; you can try varieties                                         |
| filename:credentials aws_access_key_id          | might return false negatives with dummy values                                              |
| filename:.s3cfg                                 | might return false negatives with dummy values                                              |
| filename:wp-config.php                          | wordpress config files                                                                      |
| filename:.htpasswd                              | htpasswd files                                                                              |
| filename:.env DB_USERNAME NOT homestead         | laravel .env (CI, various ruby based frameworks too)                                        |
| filename:.env MAIL_HOST=smtp.gmail.com          | gmail smtp configuration (try different smtp services too)                                  |
| filename:.git-credentials                       | git credentials store, add NOT username for more valid results                              |
| PT_TOKEN language:bash                          | pivotaltracker tokens                                                                       |
| filename:.bashrc password                       | search for passwords, etc. in .bashrc (try with .bash_profile too)                          |
| filename:.bashrc mailchimp                      | variation of above (try more variations)                                                    |
| filename:.bash_profile aws                      | aws access and secret keys                                                                  |
| rds.amazonaws.com password                      | Amazon RDS possible credentials                                                             |
| extension:json api.forecast.io                  | try variations, find api keys/secrets                                                       |
| extension:json mongolab.com                     | mongolab credentials in json configs                                                        |
| extension:yaml mongolab.com                     | mongolab credentials in yaml configs (try with yml)                                         |
| jsforce extension:js conn.login                 | possible salesforce credentials in nodejs projects                                          |
| SF_USERNAME salesforce                          | possible salesforce credentials                                                             |
| filename:.tugboat NOT _tugboat                  | Digital Ocean tugboat config                                                                |
| HEROKU_API_KEY language:shell                   | Heroku api keys                                                                             |
| HEROKU_API_KEY language:json                    | Heroku api keys in json files                                                               |
| filename:.netrc password                        | netrc that possibly holds sensitive credentials                                             |
| filename:_netrc password                        | netrc that possibly holds sensitive credentials                                             |
| filename:hub oauth_token                        | hub config that stores github tokens                                                        |
| filename:robomongo.json                         | mongodb credentials file used by robomongo                                                  |
| filename:filezilla.xml Pass                     | filezilla config file with possible user/pass to ftp                                        |
| filename:recentservers.xml Pass                 | filezilla config file with possible user/pass to ftp                                        |
| filename:config.json auths                      | docker registry authentication data                                                         |
| filename:idea14.key                             | IntelliJ Idea 14 key, try variations for other versions                                     |
| filename:config irc_pass                        | possible IRC config                                                                         |
| filename:connections.xml                        | possible db connections configuration, try variations to be specific                        |
| filename:express.conf path:.openshift           | openshift config, only email and server thou                                                |
| filename:.pgpass                                | PostgreSQL file which can contain passwords                                                 |
| filename:proftpdpasswd                          | Usernames and passwords of proftpd created by cpanel                                        |
| filename:ventrilo_srv.ini                       | Ventrilo configuration                                                                      |
| [WFClient] Password= extension:ica              | WinFrame-Client infos needed by users to connect toCitrix Application Servers               |
| filename:server.cfg rcon password               | Counter Strike RCON Passwords                                                               |
| JEKYLL_GITHUB_TOKEN                             | Github tokens used for jekyll                                                               |
| filename:.bash_history                          | Bash history file                                                                           |
| filename:.cshrc                                 | RC file for csh shell                                                                       |
| filename:.history                               | history file (often used by many tools)                                                     |
| filename:.sh_history                            | korn shell history                                                                          |
| filename:sshd_config                            | OpenSSH server config                                                                       |
| filename:dhcpd.conf                             | DHCP service config                                                                         |
| filename:prod.exs NOT prod.secret.exs           | Phoenix prod configuration file                                                             |
| filename:prod.secret.exs                        | Phoenix prod secret                                                                         |
| filename:configuration.php JConfig password     | Joomla configuration file                                                                   |
| filename:config.php dbpasswd                    | PHP application database password (e.g., phpBB forum software)                              |
| path:sites databases password                   | Drupal website database credentials                                                         |
| shodan_api_key language:python                  | Shodan API keys (try other languages too)                                                   |
| filename:shadow path:etc                        | Contains encrypted passwords and account information of new unix systems                    |
| filename:passwd path:etc                        | Contains user account information including encrypted passwords of traditional unix systems |
| extension:avastlic                              | Contains license keys for Avast! Antivirus                                                  |
| extension:dbeaver-data-sources.xml              | DBeaver config containing MySQL Credentials                                                 |
| filename:.esmtprc password                      | esmtp configuration                                                                         |
| extension:json googleusercontent client_secret  | OAuth credentials for accessing Google APIs                                                 |
| HOMEBREW_GITHUB_API_TOKEN language:shell        | Github token usually set by homebrew users                                                  |
| xoxp OR xoxb                                    | Slack bot and private tokens                                                                |
| .mlab.com password                              | MLAB Hosted MongoDB Credentials                                                             |
| filename:logins.json                            | Firefox saved password collection (key3.db usually in same repo)                            |
| filename:CCCam.cfg                              | CCCam Server config file                                                                    |
| msg nickserv identify filename:config           | Possible IRC login passwords                                                                |
| filename:settings.py SECRET_KEY                 | Django secret keys (usually allows for session hijacking, RCE, etc)                         |


## GitHub Dork List :

### GitHub Dorks for Finding Files

```
filename:manifest.xml
filename:travis.yml
filename:vim_settings.xml
filename:database
filename:prod.exs NOT prod.secret.exs
filename:prod.secret.exs
filename:.npmrc _auth
filename:.dockercfg auth
filename:WebServers.xml
filename:.bash_history <Domain name>
filename:sftp-config.json
filename:sftp.json path:.vscode
filename:secrets.yml password
filename:.esmtprc password
filename:passwd path:etc
filename:dbeaver-data-sources.xml
path:sites databases password
filename:config.php dbpasswd
filename:prod.secret.exs
filename:configuration.php JConfig password
filename:.sh_history
shodan_api_key language:python
filename:shadow path:etc
JEKYLL_GITHUB_TOKEN
filename:proftpdpasswd
filename:.pgpass
filename:idea14.key
filename:hub oauth_token
HEROKU_API_KEY language:json
HEROKU_API_KEY language:shell
SF_USERNAME salesforce
filename:.bash_profile aws
extension:json api.forecast.io
filename:.env MAIL_HOST=smtp.gmail.com
filename:wp-config.php
extension:sql mysql dump
filename:credentials aws_access_key_id
filename:id_rsa or filename:id_dsa
```

### GitHub Dorks for Finding Languages

```
language:python username
language:php username
language:sql username
language:html password
language:perl password
language:shell username
language:java api
HOMEBREW_GITHUB_API_TOKEN language:shell
```

### GiHub Dorks for Finding API Keys, Tokens and Passwords

```
api_key
???api keys???
authorization_bearer:
oauth
auth
authentication
client_secret
api_token:
???api token???
client_id
password
user_password
user_pass
passcode
client_secret
secret
password hash
OTP
user auth
```

### GitHub Dorks for Finding Usernames

```
user:name (user:admin)
org:name (org:google type:users)
in:login (<username> in:login)
in:name (<username> in:name)
fullname:firstname lastname (fullname:<name> <surname>)
in:email (data in:email)
```

### GitHub Dorks for Finding Information using Dates

```
created:<2012???04???05
created:>=2011???06???12
created:2016???02???07 location:iceland
created:2011???04???06..2013???01???14 <user> in:username
```

### GitHub Dorks for Finding Information using Extension

```
extension:pem private
extension:ppk private
extension:sql mysql dump
extension:sql mysql dump password
extension:json api.forecast.io
extension:json mongolab.com
extension:yaml mongolab.com
[WFClient] Password= extension:ica
extension:avastlic ???support.avast.com???
extension:json googleusercontent client_secret
```


## Tools

[truffleHog](https://github.com/dxa4481/truffleHog) // Searches through git repositories for secrets, digging deep into commit history and branches. This is effective at finding secrets accidentally committed.

[Watchtower](https://radar.nightfall.ai/)

Credit:

[securityonline](https://securityonline.info/github-dorks/)

[techgaun](https://raw.githubusercontent.com/techgaun/github-dorks/master/github-dorks.txt)

[shahjerry33](https://shahjerry33.medium.com/github-recon-its-really-deep-6553d6dfbb1f)

