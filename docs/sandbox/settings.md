---
hide:
  - tags
tags:
  - sandbox
  - settings
---

# The Settings File

The configuration file for Saltbox Sandbox settings is called settings.yml and is located at `/opt/sandbox/settings.yml`

settings.yml

``` yaml
---
alternatrrx:
  roles: ["1080webdl", "1080remux"]
a_train:
  remotes: [""]
cloudflared:
  token:
delugevpn:
  vpn_endpoint: netherlands.ovpn
  vpn_pass: your_vpn_password
  vpn_prov: pia
  vpn_user: your_vpn_username
  vpn_client: wireguard # 'wireguard' or 'openvpn'
doplarr:
  discord_token: your_discord_bot_token # MUST BE SET
  #you must define below overseer credential OR (Radarr AND Sonarr) credentials
  #Overseer:
  overseerr_url: "http://overseerr:5055" #set to empty and define radarr and sonarr parameters if you want to use radarr/sonarr rather than overserr.
  overseerr_api: #to be defined if you want to use overseer
  #Radarr AND Sonarr:
  radarr_api: #not defined by default. set it if you want to use sonarr and radarr.
  radarr_url: #not defined by default. set it if you want to use sonarr and radarr.
  sonarr_api: #not defined by default. set it if you want to use sonarr and radarr.
  sonarr_url: #not defined by default. set it if you want to use sonarr and radarr.
  #Optional settings:
  discord_max_results: 25
  discord_role_id: #optional: role id of users allowed to talk to the bot. Empty=all
  discord_requested_msg_style: ":plain" #optional: Sets the style of the request alert message. One of :plain :embed :none
  sonarr_quality_profile: #optional
  radarr_quality_profile: #optional
  sonarr_language_profile: #optional
  overseer_default_id: #optional - The Overseerr user id to use by default if there is no associated discord account for the requester
  partial_seasons: "true" #optional - Sets whether users can request partial seasons.
  log_level: ":info" #optional -  One of :trace :debug :info :warn :error :fatal :report
goplaxt:
  trakt_id: ~
  trakt_secret: ~
handbrake:
  handbrake_pass: saltbox # must be less than eight characters
invoiceninja:
  app_key: 'base64:O1S3kAJEDgo92gPkXtxfdCJpoGShgKloUSdcaHMXmoY=' # Generate your own with: docker run --rm -it invoiceninja/invoiceninja php artisan key:generate --show
moviematch:
  libraries: Movies
  plex_url: http://plex:32400
notifiarr:
  api_key: "api-key-from-notifiarr.com"
  ui_password: "username:password" # Password needs to be at least 16 characters long.
ombix:
  roles: ["4k"]
qbit_manage:
  qbt_run: "false" # Default is "false"
  qbt_schedule: "30" # Default is "30"
  qbt_config: "config.yml" # Default is "config.yml"
  qbt_logfile: "activity.log" # Default is "activity.log"
  qbt_cross_seed: "false" # Default is "false"
  qbt_recheck: "false" # Default is "false"
  qbt_cat_update: "false" # Default is "false"
  qbt_tag_update: "false" # Default is "false"
  qbt_rem_unregistered: "false" # Default is "false"
  qbt_rem_orphaned: "false" # Default is "false"
  qbt_tag_nohardlinks: "false" # Default is "false"
  qbt_skip_recycle: "false" # Default is "false"
  qbt_dry_run: "true" # Default is "false"
  qbt_log_level: "INFO" # Default is "INFO"
  qbt_divider: "=" # Default is "="
  qbt_width: "100" # Default is "100"
  qbt_debug: "false"
  qbt_trace: "false"
recyclarr:
  cron_schedule: "@daily" # Standard cron syntax for how often you want Recyclarr to run
requestrrx:
  roles: ["1080p", "4k"]
rfloodx:
  roles: [""]
sarotate:
  remotes: [""]
  sa_path: "your_sa_folder_path"
  sleeptime:  #optional: Delay between service account rotation (Default is 300)
  rc_port:    #optional: The port used by rc (Default is saltbox default of 5572)
  rc_user:    #optional: The user used by rc if authentication is enabled (Default is no authentication)
  rc_pass:    #optional: The password used by rc if autentication is enabled (Default is no authentication)
  apprise:    #optional: apprise notifications (Default is blank)
tandoor:
  secret_key: #Required: You can generate one with 'base64 /dev/urandom | head -c50'
transmissionvpn:
  vpn_user:
  vpn_pass:
  vpn_prov:
transmissionx:
  roles: [""]
```
