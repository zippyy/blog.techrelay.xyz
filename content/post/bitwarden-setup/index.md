+++
author = "Nicholas Bennett"
date = 2022-02-10T02:58:03Z
description = ""
draft = false
slug = "bitwarden-setup"
title = "Bitwarden Setup"
series = "Hosting Bitwarden"
+++

Alright so lets get started. You will need a few prerequisites as follows:

+ Github Account.
+ Heroku Account. (this can be done with a free account but you need to be verify your free account.)
+ A Free service like Freshping. (or some other pingdom alternative to send continuous pings to the herko instance to keep it from sleeping.)

First you will need to fork the repo and make some edits, Follow these steps:

1. Fork this [Repo](https://github.com/davidjameshowell/vaultwarden_heroku "Vaultwarden Heroku") on github.
2. Edit the file the file in the code block below to enable/disable Duo Auth.
```
.github/workflows/deploy.yml

DUO_ENABLE: 1 
```

3. Go to your forked repo and click Settings > Secrets and add secrets for:


+     HEROKU_API_KEY (yoru Heroku API key - can be found in Account Setings -> APi Keys)
+     HEROKU_APP_NAME (the name of the Heroku application, this must be unqiue across Heroku and will fail if it is not) [Value alphanumerical]
+     HEROKU_VERIFIED (required regardless, if you have added a credit card on, your account will be verified to use built in addons, if not please see "NON VERIFIED ACCOUNTS" section) [Value 0/1]


4. 

