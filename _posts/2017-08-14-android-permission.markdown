---
layout: post
title:  "Android权限"
date:   2017-08-14 00:00 +0800
categories: jekyll update
---

### 危险的权限
adb shell pm list permissions -d -g
```
C:\Users\asus>adb shell pm list permissions -d -g
* daemon not running. starting it now on port 5037 *
* daemon started successfully *
Dangerous Permissions:

group:android.permission-group.STATUS_BAR

group:android.permission-group.USER_DICTIONARY
  permission:android.permission.READ_USER_DICTIONARY

group:android.permission-group.SYSTEM_TOOLS
  permission:com.android.launcher.permission.UNINSTALL_SHORTCUT
  permission:android.permission.CLEAR_APP_CACHE
  permission:com.android.launcher.permission.INSTALL_SHORTCUT
  permission:android.permission.ACCESS_MOCK_LOCATION
  permission:android.permission.SUBSCRIBED_FEEDS_WRITE

group:android.permission-group.WRITE_USER_DICTIONARY

group:android.permission-group.MICROPHONE
  permission:android.permission.RECORD_AUDIO

group:android.permission-group.AFFECTS_BATTERY
  permission:android.permission.CHANGE_WIFI_MULTICAST_STATE

group:android.permission-group.BOOKMARKS
  permission:com.android.browser.permission.WRITE_HISTORY_BOOKMARKS
  permission:com.android.browser.permission.READ_HISTORY_BOOKMARKS

group:android.permission-group.STORAGE
  permission:android.permission.WRITE_EXTERNAL_STORAGE

group:android.permission-group.ACCOUNTS
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.mobile
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.speechpersonalization
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.OTHER_SERVICES
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.sierraqa
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.notebook
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.writely
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.speech
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.mail
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.local
  permission:android.permission.AUTHENTICATE_ACCOUNTS
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.print
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.wifi
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.knol
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.ah
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.blogger
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.orkut
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.lh2
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.news
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.sierrasandbox
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.groups2
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.adwords
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.cp
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.YouTubeUser
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.ig
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.android
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.gbase
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.dodgeball
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.finance
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.grandcentral
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.sierra
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.jotspot
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.youtube
  permission:android.permission.MANAGE_ACCOUNTS
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.sitemaps
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.health
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.androidsecure
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.cl
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.talk
  permission:android.permission.USE_CREDENTIALS
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.wise
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.adsense

group:android.permission-group.AUDIO_SETTINGS

group:android.permission-group.WALLPAPER

group:android.permission-group.ACCESSIBILITY_FEATURES

group:android.permission-group.COST_MONEY

group:android.permission-group.SYSTEM_CLOCK

group:android.permission-group.SOCIAL_INFO
  permission:android.permission.WRITE_CONTACTS
  permission:android.permission.WRITE_SOCIAL_STREAM
  permission:android.permission.READ_CALL_LOG
  permission:android.permission.READ_CONTACTS
  permission:android.permission.READ_SOCIAL_STREAM
  permission:android.permission.WRITE_CALL_LOG

group:android.permission-group.PERSONAL_INFO
  permission:android.permission.WRITE_CALENDAR
  permission:android.permission.READ_PROFILE
  permission:android.permission.READ_CALENDAR
  permission:android.permission.WRITE_PROFILE

group:android.permission-group.BLUETOOTH_NETWORK
  permission:android.permission.BLUETOOTH_ADMIN
  permission:android.permission.BLUETOOTH

group:android.permission-group.SCREENLOCK
  permission:android.permission.DISABLE_KEYGUARD

group:android.permission-group.DEVELOPMENT_TOOLS

group:android.permission-group.PHONE_CALLS
  permission:android.permission.CALL_PHONE
  permission:android.permission.PROCESS_OUTGOING_CALLS
  permission:android.permission.READ_PHONE_STATE
  permission:android.permission.USE_SIP

group:android.permission-group.LOCATION
  permission:android.permission.ACCESS_COARSE_LOCATION
  permission:android.permission.ACCESS_FINE_LOCATION

group:android.permission-group.VOICEMAIL
  permission:com.android.voicemail.permission.ADD_VOICEMAIL

group:android.permission-group.DISPLAY
  permission:android.permission.SYSTEM_ALERT_WINDOW

group:android.permission-group.CAMERA
  permission:android.permission.CAMERA

group:android.permission-group.SYNC_SETTINGS

group:android.permission-group.HARDWARE_CONTROLS

group:android.permission-group.CALENDAR

group:android.permission-group.APP_INFO

group:android.permission-group.NETWORK
  permission:android.permission.NFC
  permission:android.permission.CHANGE_WIFI_STATE
  permission:android.permission.INTERNET
  permission:android.permission.CHANGE_WIMAX_STATE

group:android.permission-group.DEVICE_ALARMS

group:android.permission-group.MESSAGES
  permission:cn.cj.pe.permission.DELETE_MESSAGES
  permission:cn.cj.pe.permission.READ_ATTACHMENT
  permission:android.permission.SEND_SMS
  permission:com.android.email.permission.READ_ATTACHMENT
  permission:com.google.android.providers.talk.permission.WRITE_ONLY
  permission:android.permission.READ_SMS
  permission:android.permission.RECEIVE_MMS
  permission:cn.cj.pe.permission.REMOTE_CONTROL
  permission:cn.cj.pe.permission.READ_MESSAGES
  permission:android.permission.RECEIVE_SMS
  permission:android.permission.READ_CELL_BROADCASTS
  permission:com.google.android.providers.talk.permission.READ_ONLY
  permission:android.permission.WRITE_SMS
  permission:android.permission.RECEIVE_WAP_PUSH

ungrouped:
  permission:com.google.android.gms.permission.CAR_SPEED
  permission:com.google.android.gms.permission.CAR_FUEL
  permission:com.huawei.phoneservice.permission.CENTER_SERVICE_ACCESS
  permission:com.android.permission.ENABLE_HWQRCODEDISPATCHER
  permission:com.huawei.camera.permission.QRCODE_SCAN
  permission:com.huawei.phoneservice.permission.SMART_FAQS_ACCESS
  permission:com.google.android.gms.permission.CAR_MILEAGE
  permission:org.simalliance.openmobileapi.SMARTCARD
  permission:com.google.android.gms.permission.CAR_VENDOR_EXTENSION
```

### 全部权限
* adb shell pm list permissions -g
```
C:\Users\asus>adb shell pm list permissions -g
All Permissions:

group:android.permission-group.STATUS_BAR
  permission:android.permission.EXPAND_STATUS_BAR

group:android.permission-group.USER_DICTIONARY
  permission:android.permission.READ_USER_DICTIONARY

group:android.permission-group.SYSTEM_TOOLS
  permission:android.permission.GET_PACKAGE_SIZE
  permission:android.permission.NET_TUNNELING
  permission:android.permission.SUBSCRIBED_FEEDS_READ
  permission:android.permission.CHANGE_BACKGROUND_DATA_SETTING
  permission:com.android.launcher.permission.UNINSTALL_SHORTCUT
  permission:android.permission.BROADCAST_PACKAGE_REMOVED
  permission:android.permission.RECOVERY
  permission:com.huawei.android.launcher.permission.CHANGE_VLIFE_WALLPAPER
  permission:android.permission.SET_SCREEN_COMPATIBILITY
  permission:android.permission.READ_DREAM_STATE
  permission:com.huawei.android.launcher.permission.CHANGE_STK_NAME
  permission:android.permission.SET_ANIMATION_SCALE
  permission:android.permission.ASEC_DESTROY
  permission:android.permission.ASEC_MOUNT_UNMOUNT
  permission:android.permission.BATTERY_STATS
  permission:android.permission.ASEC_RENAME
  permission:com.huawei.android.launcher.permission.RANDOM_CHANGE_WALLPAPER
  permission:android.permission.GLOBAL_SEARCH
  permission:android.permission.INTERACT_ACROSS_USERS
  permission:android.permission.MOUNT_UNMOUNT_FILESYSTEMS
  permission:android.permission.CLEAR_APP_CACHE
  permission:android.permission.READ_SEARCH_INDEXABLES
  permission:android.permission.GET_APP_OPS_STATS
  permission:android.permission.REMOTE_AUDIO_PLAYBACK
  permission:android.permission.START_ANY_ACTIVITY
  permission:android.permission.BLUETOOTH_STACK
  permission:com.huawei.android.launcher.permission.SEND_MATCH_CARD
  permission:com.huawei.android.launcher.permission.READ_SETTINGS
  permission:android.permission.ASEC_ACCESS
  permission:com.huawei.android.launcher.permission.WRITE_SETTINGS
  permission:android.permission.ACCESS_LOCATION_EXTRA_COMMANDS
  permission:com.android.launcher.permission.INSTALL_SHORTCUT
  permission:android.permission.SET_WALLPAPER_COMPONENT
  permission:android.permission.START_TASKS_FROM_RECENTS
  permission:android.permission.ASEC_CREATE
  permission:android.permission.GLOBAL_SEARCH_CONTROL
  permission:com.huawei.android.launcher.permission.CHANGE_POWERMODE
  permission:android.permission.BROADCAST_STICKY
  permission:android.permission.MOUNT_FORMAT_FILESYSTEMS
  permission:android.permission.GET_DETAILED_TASKS
  permission:android.permission.DIAGNOSTIC
  permission:android.permission.ACCESS_MOCK_LOCATION
  permission:android.permission.WRITE_DREAM_STATE
  permission:android.permission.FORCE_STOP_PACKAGES
  permission:android.permission.SUBSCRIBED_FEEDS_WRITE
  permission:com.huawei.android.launcher.permission.SEND_DOWNLOAD_CANCEL
  permission:android.permission.OEM_UNLOCK_STATE
  permission:android.permission.INTERACT_ACROSS_USERS_FULL
  permission:android.permission.MODIFY_APPWIDGET_BIND_PERMISSIONS
  permission:com.tencent.msf.permission.account.sync
  permission:android.permission.NET_ADMIN
  permission:android.permission.WRITE_SETTINGS
  permission:android.permission.WRITE_APN_SETTINGS
  permission:android.permission.SET_PREFERRED_APPLICATIONS
  permission:com.huawei.android.launcher.permission.PIFLOW_NEWS_RECEIVE
  permission:android.permission.MANAGE_USERS

group:android.permission-group.WRITE_USER_DICTIONARY
  permission:android.permission.WRITE_USER_DICTIONARY

group:android.permission-group.MICROPHONE
  permission:android.permission.RECORD_AUDIO

group:android.permission-group.AFFECTS_BATTERY
  permission:android.permission.CHANGE_WIFI_MULTICAST_STATE
  permission:android.permission.FLASHLIGHT
  permission:android.permission.VIBRATE
  permission:android.permission.TRANSMIT_IR
  permission:android.permission.WAKE_LOCK

group:android.permission-group.BOOKMARKS
  permission:com.android.browser.permission.WRITE_HISTORY_BOOKMARKS
  permission:com.android.browser.permission.READ_HISTORY_BOOKMARKS

group:android.permission-group.STORAGE
  permission:android.permission.WRITE_EXTERNAL_STORAGE
  permission:android.permission.READ_EXTERNAL_STORAGE
  permission:android.permission.MANAGE_DOCUMENTS
  permission:android.permission.WRITE_MEDIA_STORAGE

group:android.permission-group.ACCOUNTS
  permission:android.permission.GET_ACCOUNTS
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.mobile
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.speechpersonalization
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.OTHER_SERVICES
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.sierraqa
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.notebook
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.writely
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.speech
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.mail
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.local
  permission:android.permission.AUTHENTICATE_ACCOUNTS
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.print
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.wifi
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.knol
  permission:com.google.android.providers.gsf.permission.READ_GSERVICES
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.ah
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.blogger
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.orkut
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.lh2
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.news
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.sierrasandbox
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.groups2
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.adwords
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.cp
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.YouTubeUser
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.ig
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.android
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.gbase
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.dodgeball
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.finance
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.grandcentral
  permission:android.permission.ACCOUNT_MANAGER
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.sierra
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.jotspot
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.youtube
  permission:android.permission.MANAGE_ACCOUNTS
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.ALL_SERVICES
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.sitemaps
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.health
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.androidsecure
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.cl
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.talk
  permission:android.permission.USE_CREDENTIALS
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.wise
  permission:com.google.android.googleapps.permission.GOOGLE_AUTH.adsense

group:android.permission-group.AUDIO_SETTINGS
  permission:android.permission.MODIFY_AUDIO_SETTINGS

group:android.permission-group.WALLPAPER
  permission:android.permission.SET_WALLPAPER
  permission:android.permission.SET_WALLPAPER_HINTS

group:android.permission-group.ACCESSIBILITY_FEATURES

group:android.permission-group.COST_MONEY

group:android.permission-group.SYSTEM_CLOCK
  permission:android.permission.SET_TIME_ZONE

group:android.permission-group.SOCIAL_INFO
  permission:android.permission.WRITE_CONTACTS
  permission:android.permission.WRITE_SOCIAL_STREAM
  permission:android.permission.READ_CALL_LOG
  permission:android.permission.READ_CONTACTS
  permission:android.permission.READ_SOCIAL_STREAM
  permission:android.permission.WRITE_CALL_LOG

group:android.permission-group.PERSONAL_INFO
  permission:android.permission.WRITE_CALENDAR
  permission:android.permission.BIND_KEYGUARD_APPWIDGET
  permission:com.android.voicemail.permission.READ_WRITE_ALL_VOICEMAIL
  permission:com.google.android.gms.permission.ACTIVITY_RECOGNITION
  permission:android.permission.READ_PROFILE
  permission:android.permission.BIND_APPWIDGET
  permission:android.permission.BODY_SENSORS
  permission:android.permission.READ_CALENDAR
  permission:android.permission.RETRIEVE_WINDOW_CONTENT
  permission:android.permission.BIND_DIRECTORY_SEARCH
  permission:android.permission.WRITE_PROFILE

group:android.permission-group.BLUETOOTH_NETWORK
  permission:android.permission.BLUETOOTH_ADMIN
  permission:android.permission.BLUETOOTH_MAP
  permission:android.permission.BLUETOOTH
  permission:android.permission.BLUETOOTH_PRIVILEGED

group:android.permission-group.SCREENLOCK
  permission:android.permission.DISABLE_KEYGUARD

group:android.permission-group.DEVELOPMENT_TOOLS
  permission:android.permission.SET_PROCESS_LIMIT
  permission:android.permission.SIGNAL_PERSISTENT_PROCESSES
  permission:android.permission.SET_ALWAYS_FINISH
  permission:android.permission.SET_DEBUG_APP
  permission:android.permission.READ_LOGS
  permission:android.permission.WRITE_SECURE_SETTINGS
  permission:android.permission.DUMP
  permission:android.permission.ACCESS_ALL_EXTERNAL_STORAGE
  permission:android.permission.CHANGE_CONFIGURATION

group:android.permission-group.PHONE_CALLS
  permission:android.permission.READ_PRECISE_PHONE_STATE
  permission:android.permission.BIND_INCALL_SERVICE
  permission:android.permission.CALL_PHONE
  permission:android.permission.PROCESS_OUTGOING_CALLS
  permission:android.permission.CONTROL_INCALL_EXPERIENCE
  permission:android.permission.BIND_CONNECTION_SERVICE
  permission:android.permission.READ_PRIVILEGED_PHONE_STATE
  permission:android.permission.READ_PHONE_STATE
  permission:android.permission.MODIFY_PHONE_STATE
  permission:android.permission.USE_SIP

group:android.permission-group.LOCATION
  permission:android.permission.LOCATION_HARDWARE
  permission:android.permission.ACCESS_COARSE_LOCATION
  permission:android.permission.ACCESS_FINE_LOCATION

group:android.permission-group.VOICEMAIL
  permission:com.android.voicemail.permission.READ_VOICEMAIL
  permission:com.android.voicemail.permission.ADD_VOICEMAIL
  permission:com.android.voicemail.permission.WRITE_VOICEMAIL

group:android.permission-group.DISPLAY
  permission:android.permission.SYSTEM_ALERT_WINDOW

group:android.permission-group.CAMERA
  permission:android.permission.CAMERA
  permission:android.permission.CAMERA_DISABLE_TRANSMIT_LED

group:android.permission-group.SYNC_SETTINGS
  permission:android.permission.READ_SYNC_SETTINGS
  permission:android.permission.WRITE_SYNC_SETTINGS
  permission:android.permission.READ_SYNC_STATS

group:android.permission-group.HARDWARE_CONTROLS
  permission:android.permission.MANAGE_USB
  permission:android.permission.HARDWARE_TEST
  permission:android.permission.ACCESS_MTP

group:android.permission-group.CALENDAR

group:android.permission-group.APP_INFO
  permission:android.permission.REMOVE_TASKS
  permission:android.permission.REORDER_TASKS
  permission:android.permission.PERSISTENT_ACTIVITY
  permission:android.permission.RESTART_PACKAGES
  permission:android.permission.GET_TASKS
  permission:android.permission.MANAGE_ACTIVITY_STACKS
  permission:android.permission.KILL_BACKGROUND_PROCESSES
  permission:android.permission.REAL_GET_TASKS
  permission:android.permission.RECEIVE_BOOT_COMPLETED

group:android.permission-group.NETWORK
  permission:android.permission.SCORE_NETWORKS
  permission:android.permission.NFC
  permission:android.permission.DOWNLOAD_WITHOUT_NOTIFICATION
  permission:com.google.android.permission.BROADCAST_DATA_MESSAGE
  permission:android.permission.LOOP_RADIO
  permission:android.permission.CHANGE_WIFI_STATE
  permission:android.permission.INTERNET
  permission:android.permission.ACCESS_WIMAX_STATE
  permission:com.google.android.c2dm.permission.RECEIVE
  permission:android.permission.CHANGE_NETWORK_STATE
  permission:android.permission.CHANGE_WIMAX_STATE
  permission:com.google.android.xmpp.permission.USE_XMPP_ENDPOINT
  permission:android.permission.READ_WIFI_CREDENTIAL
  permission:android.permission.CONNECTIVITY_INTERNAL
  permission:com.google.android.xmpp.permission.SEND_RECEIVE
  permission:com.google.android.c2dm.permission.SEND
  permission:com.google.android.gtalkservice.permission.SEND_HEARTBEAT
  permission:com.google.android.xmpp.permission.BROADCAST
  permission:android.permission.ACCESS_WIFI_STATE
  permission:android.permission.ACCESS_NETWORK_STATE
  permission:android.permission.RECEIVE_DATA_ACTIVITY_CHANGE
  permission:com.google.android.xmpp.permission.XMPP_ENDPOINT_BROADCAST

group:android.permission-group.DEVICE_ALARMS
  permission:com.android.alarm.permission.SET_ALARM

group:android.permission-group.MESSAGES
  permission:com.google.android.gtalkservice.permission.GTALK_SERVICE
  permission:android.permission.RECEIVE_EMERGENCY_BROADCAST
  permission:android.permission.SEND_SMS
  permission:com.android.email.permission.READ_ATTACHMENT
  permission:com.google.android.providers.talk.permission.WRITE_ONLY
  permission:android.permission.BROADCAST_SMS
  permission:android.permission.READ_SMS
  permission:android.permission.BROADCAST_WAP_PUSH
  permission:android.permission.RECEIVE_MMS
  permission:android.permission.RECEIVE_BLUETOOTH_MAP
  permission:android.permission.RECEIVE_SMS
  permission:android.permission.READ_CELL_BROADCASTS
  permission:com.google.android.providers.talk.permission.READ_ONLY
  permission:android.permission.WRITE_SMS
  permission:android.permission.RECEIVE_WAP_PUSH
  permission:android.permission.SEND_RESPOND_VIA_MESSAGE

ungrouped:
  permission:android.permission.ACCESS_INPUT_FLINGER
  permission:android.permission.BIND_TEXT_SERVICE
  permission:com.huawei.hidisk.FingerPrintProvider.permission.ACCESS
  permission:android.permission.MANAGE_MEDIA_PROJECTION
  permission:com.google.android.projection.gearhead.receivertest.DIALOG_PERMISSION
  permission:android.permission.BIND_DREAM_SERVICE
  permission:com.android.contacts.permission.WRITE_CONTACTS_PRIVATE_INFO
  permission:com.huawei.contacts.permission.HW_CONTACTS_ALL
  permission:com.android.huawei.permission.REPORT_FM_STATUS
  permission:android.permission.ACCESS_BLUETOOTH_SHARE
  permission:android.permission.SEND_DOWNLOAD_COMPLETED_INTENTS
  permission:com.google.android.gms.permission.CAR_SPEED
  permission:com.huawei.motion.permission.START_MOTION_SETTINGS
  permission:android.Manifest.permission.AUTHENTICATE_ACCOUNTS
  permission:android.permission.MODIFY_AUDIO_ROUTING
  permission:android.permission.ACCESS_KEYGUARD_SECURE_STORAGE
  permission:android.permission.FILTER_EVENTS
  permission:com.huawei.hicloud.permission.CONTACT_RESTORE_FINISHED
  permission:com.google.android.gms.permission.C2D_MESSAGE
  permission:com.alipay.android.permission.PATTERNLOCK
  permission:android.permission.READ_PRE_INSTALLED
  permission:android.permission.CAPTURE_TV_INPUT
  permission:android.permission.MODIFY_NETWORK_ACCOUNTING
  permission:android.permission.TV_INPUT_HARDWARE
  permission:android.permission.SET_POINTER_SPEED
  permission:com.tencent.applink.sdk.permission.APPLINK_WRITE_PERMISSION
  permission:android.permission.CALL_PRIVILEGED
  permission:android.permission.BRICK
  permission:com.android.email.permission.READ_PRE_INSTALLED
  permission:android.permission.HSM_SMCS
  permission:com.huawei.motion.permission.START_MOTION_SERVICE
  permission:com.google.android.gms.permission.CAR_FUEL
  permission:com.huawei.remoteassistant.permission.USE_ACCESS
  permission:com.qq.AppService.permission.out.IPC_SERVICE
  permission:com.huawei.phoneservice.permission.CENTER_SERVICE_ACCESS
  permission:huawei.permmisons.mms.SEND_REQUEST
  permission:android.permission.BIND_DEVICE_ADMIN
  permission:com.android.huawei.magazineunlock.permission.WRITE
  permission:com.tencent.tms.broadcast
  permission:android.permission.PERFORM_CDMA_PROVISIONING
  permission:huawei.android.permission.CHANGE_SCREEN_LOCK_AFTER_TIMEOUT
  permission:android.permission.DELETE_CACHE_FILES
  permission:com.tencent.photos.permission.DATA
  permission:com.google.android.gsf.permission.C2D_MESSAGE
  permission:android.permission.START_PRINT_SERVICE_CONFIG_ACTIVITY
  permission:com.google.android.providers.settings.permission.WRITE_GSETTINGS
  permission:huawei.permmisons.floatmms.RECEIVE_REQUEST
  permission:android.permission.CAPTURE_AUDIO_HOTWORD
  permission:com.android.huawei.permission.OUTSIDE_STOP_SOUND_RECORDER
  permission:android.permission.WRITE_GSERVICES
  permission:com.huawei.motion.permission.WRITE_DATA
  permission:android.permission.CLEAR_APP_USER_DATA
  permission:com.huawei.hwid.permission.ACCESS
  permission:android.permission.CONTROL_LOCATION_UPDATES
  permission:android.permission.MANAGE_APP_TOKENS
  permission:com.android.contacts.huawei.permission.REFRESH_DRAFT
  permission:android.Manifest.permission.MANAGE_ACCOUNTS
  permission:com.huawei.android.thememanager.permission.ACCESS_CHANGE_WALLPAPAER
  permission:com.huawei.android.FloatTasks.writePermission
  permission:android.permission.FREEZE_SCREEN
  permission:android.permission.READ_INSTALL_SESSIONS
  permission:com.huawei.vassistant.permission.USE_MODEL_SERVICE
  permission:android.permission.USER_ACTIVITY
  permission:com.android.calendar.huawei.permission.DOWNLOADSUBSCRIPTION
  permission:com.android.email.permission.GLOBAL_SEARCH
  permission:com.android.permission.airsharing_screensharing_interface
  permission:com.android.deskclock.huawei.permission.UPDATE_ALARM
  permission:android.permission.INJECT_EVENTS
  permission:com.huawei.appmarket.SEND_THIRD_COMMON_MSG
  permission:com.huawei.hwresolver.provider.writePermission
  permission:android.permission.UPDATE_APP_OPS_STATS
  permission:com.huawei.privacymode.permission.STARTUP
  permission:com.huawei.android.thememanager.permission.THEMEMANAGER_INTERFACE
  permission:android.permission.READ_NETWORK_USAGE_HISTORY
  permission:imcs.permission.MUSIC_CONTROL
  permission:android.permission.BIND_PRINT_SERVICE
  permission:com.huawei.skytone.BROADCAST
  permission:android.permission.BACKUP
  permission:com.google.android.providers.settings.permission.READ_GSETTINGS
  permission:com.android.permission.RECV_HUAWEI
  permission:com.android.stk.permission.READ_STK_PROVIDER
  permission:com.android.systemui.permission.SCREEN_SHOT
  permission:com.huawei.systemmanager.permission.ACCESS_INTERFACE
  permission:com.android.vending.INTENT_VENDING_ONLY
  permission:com.android.packageinstaller.permission.HUAWEI_CHECK_APP_RISK_ACCESS
  permission:huawei.android.permission.MANAGER_PRIVACY_FINGER
  permission:android.permission.BIND_VOICE_INTERACTION
  permission:com.qq.AppService.permission.out.CACHE_READ_PERMISSION
  permission:android.permission.ACCESS_CHECKIN_PROPERTIES
  permission:android.permission.ACCESS_AP_INFORMATION
  permission:com.manyou.youlaohu.permission.MIPUSH_RECEIVE
  permission:android.permission.PROCESS_CALLLOG_INFO
  permission:com.huawei.powergenie.receiverPermission
  permission:com.android.permission.ENABLE_HWQRCODEDISPATCHER
  permission:com.vlife.wallpaper.permission.IPC
  permission:com.huawei.appmarket.permission.imageservice
  permission:com.huawei.alarm.provider.readPermission
  permission:com.huawei.appmarket.permission.THIRD_PROVIDER_SERVICE
  permission:com.huawei.appmarket.RECV_THIRD_COMMON_MSG
  permission:com.huawei.camera.permission.QRCODE_SCAN
  permission:android.permission.ACCESS_DOWNLOAD_MANAGER_ADVANCED
  permission:com.tencent.qqhead.permission.getheadresp
  permission:android.permission.MANAGE_DEVICE_ADMINS
  permission:com.android.contacts.permission.PRIVELEGED_ACCESS_ALLOWED
  permission:android.permission.NFC_HANDOVER_STATUS
  permission:android.permission.CONTROL_WIFI_DISPLAY
  permission:android.permission.MANAGE_CA_CERTIFICATES
  permission:com.google.android.gsf.permission.CONNECTION
  permission:android.permission.UPDATE_DEVICE_STATS
  permission:android.server.checkin.CHECKIN.permission.C2D_MESSAGE
  permission:android.permission.READ_FRAME_BUFFER
  permission:com.google.android.googleapps.permission.ACCESS_GOOGLE_PASSWORD
  permission:com.android.keyguard.FINGERPRINT_UNLOCK
  permission:com.android.permission.system_manager_interface
  permission:com.huawei.android.wfdft.permission.ACCESS_WIFIDIRECTIMPORT_SHARE
  permission:android.permission.INVOKE_CARRIER_SETUP
  permission:com.huawei.KoBackup.permission.ACCESS
  permission:com.tencent.qav.permission.broadcast
  permission:com.google.android.gms.permission.CAR
  permission:android.permission.SECURITY_PACKAGE
  permission:com.huawei.hwid.permission.CONTENT_PROVIDER
  permission:com.tencent.msf.service.permission
  permission:com.huawei.permission.INTELLIGENT_NOTIFICATION_MSG_BRACELET
  permission:com.xiaomi.gamecenter.sdk.service.permission.MIPUSH_RECEIVE
  permission:com.vlife.huawei.wallpaper.permission.INSTALL_APIRESPONSE
  permission:android.permission.BIND_TV_INPUT
  permission:android.permission.MANAGE_VOICE_KEYPHRASES
  permission:com.android.email.permission.OMACP_CONFIGURE
  permission:com.huawei.phone.permission.NUMBERLOCATION
  permission:com.android.huawei.magazineunlock.permission.READ
  permission:android.permission.BIND_REMOTEVIEWS
  permission:getui.permission.GetuiService.cn.swiftpass.enterprise.wft.v4.appstore
  permission:android.permission.HW_CAMCFG_SERVICE
  permission:android.permission.LAUNCH_TRUST_AGENT_SETTINGS
  permission:com.tencent.music.data.permission2
  permission:android.permission.SET_KEYBOARD_LAYOUT
  permission:com.huawei.skytone.permission.VSIM_UI
  permission:com.huawei.permission.BIG_DATA
  permission:android.permission.ACCESS_SURFACE_FLINGER
  permission:huawei.android.permission.SELFBUILD_IR_SERVICE
  permission:com.tencent.applink.sdk.permission.APPLINK_READ_PERMISSION
  permission:com.huawei.gamebox.provider.readPermission
  permission:com.android.email.permission.WRITE_PRE_INSTALLED
  permission:android.Manifest.permission.GET_ACCOUNTS
  permission:com.huawei.vassistant.providers.settings.permission.READ_ONLY
  permission:com.android.permission.airsharing_play_interface
  permission:com.tencent.android.qqdownloader.theme.permission
  permission:com.android.mediacenter.permission.INTERACTION
  permission:com.android.hwmirror.permission.SECURE_MIRROR
  permission:android.permission.SHUTDOWN
  permission:com.huawei.motion.permission.MOTION_ACTION_RECOGNITION
  permission:android.permission.FACTORY_TEST
  permission:android.permission.ACCESS_DOWNLOAD_MANAGER
  permission:android.permission.SET_INPUT_CALIBRATION
  permission:android.permission.SET_TIME
  permission:android.permission.SEND_PRIVACY_MODE_CHANGED
  permission:android.permission.ACCESS_CACHE_FILESYSTEM
  permission:android.permission.ACCESS_NOTIFICATIONS
  permission:com.huawei.alarm.provider.writePermission
  permission:com.android.bluetooth.permission.TEST_STATUS
  permission:android.permission.UPDATE_LOCK
  permission:com.huawei.appmarket.provider.readPermission
  permission:com.huawei.privacymode.permission.CHANGE_PASSWORD
  permission:com.huawei.totemweather.permission.THIRD_REQUEST_WEATHER
  permission:android.permission.BIND_NOTIFICATION_LISTENER_SERVICE
  permission:com.huawei.camera.permission.PRIVATE
  permission:com.huawei.android.thememanager.permission.THEME_PROVIDER_ACCESS
  permission:com.huawei.phoneservice.permission.USES_LOG_UPLOAD_SERVICE
  permission:android.permission.BIND_ACCESSIBILITY_SERVICE
  permission:com.huawei.permission.CARDS_SETTINGS
  permission:com.huawei.phoneservice.permission.SMART_FAQS_ACCESS
  permission:com.huawei.hwvplayer.permission.protected.broadcast
  permission:com.google.android.gms.permission.GAMES_DEBUG_SETTINGS
  permission:com.google.android.gms.permission.INTERNAL_BROADCAST
  permission:android.permission.CRYPT_KEEPER
  permission:huawei.android.permission.RESET_NEW_PASSWORD
  permission:com.huawei.android.hwaps.writePermission
  permission:android.permission.BIND_VPN_SERVICE
  permission:com.android.certinstaller.INSTALL_AS_USER
  permission:android.permission.BIND_WALLPAPER
  permission:android.permission.IBINDER_NOTIFICATION_SERVICE
  permission:com.huawei.powergenie.stateServicePermission
  permission:android.permission.DELETE_PACKAGES
  permission:android.permission.ACCESS_NETWORK_CONDITIONS
  permission:android.permission.REBOOT
  permission:android.permission.ALLOW_ANY_CODEC_FOR_PLAYBACK
  permission:android.permission.SECURITY_ACTIVITY
  permission:android.permission.BIND_CONDITION_PROVIDER_SERVICE
  permission:android.permission.BIND_JOB_SERVICE
  permission:huawei.permission.HWINTELLIGENT_RECEIVER
  permission:android.permission.CONFIRM_FULL_BACKUP
  permission:com.huawei.appmarket.permission.downloadmanager
  permission:com.huawei.deskclock.broadcast.permission
  permission:com.android.printspooler.permission.ACCESS_ALL_PRINT_JOBS
  permission:android.intent.category.MASTER_CLEAR.permission.C2D_MESSAGE
  permission:com.android.phone.permission.AUTOIP_STATUS_CHANGED
  permission:android.permission.BIND_PRINT_SPOOLER_SERVICE
  permission:com.android.stk.permission.WRITE_STK_PROVIDER
  permission:android.permission.CAPTURE_SECURE_VIDEO_OUTPUT
  permission:android.permission.BIND_REMOTE_DISPLAY
  permission:com.huawei.notepad.provider.readPermission
  permission:com.huawei.android.permission.gallerysupportphotoshare
  permission:android.permission.SET_ORIENTATION
  permission:com.google.android.googleapps.permission.GOOGLE_MAIL_SWITCH
  permission:com.huawei.skytone.HW_WIFI_ICON_ENTER
  permission:cn.ninegame.gamemanager.permission.MIPUSH_RECEIVE
  permission:android.permission.REMOVE_DRM_CERTIFICATES
  permission:android.permission.MOVE_PACKAGE
  permission:android.permission.CONFIGURE_WIFI_DISPLAY
  permission:com.android.contacts.permission.READ_CONTACTS_PRIVACY_DATA
  permission:com.tencent.msg.permission.pushnotify
  permission:com.huawei.contacts.permission.hicloudLogin
  permission:com.android.huawei.permission.OUTSIDE_SECURE_RECORD
  permission:android.permission.ACCESS_CALLERID
  permission:com.huawei.cust.android.phone.permission.HW_LTEONLY
  permission:com.huawei.notepad.provider.writePermission
  permission:android.permission.ACCESS_CONTENT_PROVIDERS_EXTERNALLY
  permission:android.permission.PACKAGE_USAGE_STATS
  permission:com.tencent.wifisdk.permission.disconnect
  permission:com.android.phone.AUTOIP_SETTING_RECEIVER_PERMISSION
  permission:com.google.android.gsf.subscribedfeeds.permission.C2D_MESSAGE
  permission:com.huawei.contacts.permission.PRIVATE_CONTACTS
  permission:android.permission.RETRIEVE_WINDOW_TOKEN
  permission:android.permission.MEDIA_CONTENT_CONTROL
  permission:com.huawei.appmarket.wlanapp
  permission:android.permission.COPY_PROTECTED_DATA
  permission:com.huawei.hwresolver.provider.readPermission
  permission:com.alipay.android.app.gphone.SHARE
  permission:com.android.systemui.permission.BackgrounCallingLayout
  permission:android.permission.DEVICE_POWER
  permission:android.permission.PROVIDE_TRUST_AGENT
  permission:com.android.keyguard.permission.SEND_STEP_INFO
  permission:android.permission.RECEIVE_STK_COMMANDS
  permission:com.android.contacts.permission.READ_CONTACTS_PRIVATE_INFO
  permission:android.permission.BAIDU_LOCATION_SERVICE
  permission:android.permission.BIND_PACKAGE_VERIFIER
  permission:android.permission.HDMI_CEC
  permission:com.android.calendar.huawei.permission.CALENDAR_RECESS
  permission:com.huawei.camera.permission.PREFERENCE_PROVIDER
  permission:com.android.exchange.permission.ACCESS_CANCEL_DOWNLOAD_ATTACHMENT
  permission:com.google.android.gms.permission.CAR_MILEAGE
  permission:android.permission.BIND_INPUT_METHOD
  permission:android.permission.GET_TOP_ACTIVITY_INFO
  permission:com.android.providers.media.permission.SCAN_FOLDER
  permission:huawei.permission.MMI_TEST
  permission:android.permission.FRAME_STATS
  permission:com.huawei.motion.permission.MOTION_ACTION_OPERATE
  permission:com.android.contacts.huawei.permission.NOTIFICATION_UPDATE_ACTION
  permission:android.permission.CREATE_USERS
  permission:com.android.dreams.phototable.permission.HUAWEI_PHOTOTABLE_ACCESS
  permission:huawei.permission.BIRTHDAY_CALENDAR_CHANGED
  permission:android.permission.STATUS_BAR
  permission:com.huawei.bluetooth.permission.ACCESS_BLUETOOTHIMPORT_SHARE
  permission:android.permission.SET_ACTIVITY_WATCHER
  permission:com.android.huawei.permission.OUTSIDE_SECURE_CALCULATOR
  permission:com.huawei.gallery.permission.ACCESS_PHOTO_MANAGER
  permission:huawei.permission.CASERVICE
  permission:com.wandoujia.phoenix2.permission.MIPUSH_RECEIVE
  permission:android.permission.ACCESS_ALL_DOWNLOADS
  permission:com.android.server.telecom.permission.REGISTER_CONNECTION_MANAGER
  permission:com.google.android.gms.permission.CHECKIN_NOW
  permission:com.huawei.android.wfdft.permission.ACCESS_INTERFACE
  permission:com.ut.permission.DEVICE_STATE
  permission:android.permission.STOP_APP_SWITCHES
  permission:com.huawei.vdrive.permission.HANDSFREE_STATE_CHANGED
  permission:com.android.calendar.huawei.permission.CALENDAR_ACCESS
  permission:com.google.android.gms.DRIVE
  permission:com.android.permission.airsharing_group_interface
  permission:android.permission.TEMPORARY_ENABLE_ACCESSIBILITY
  permission:com.android.exchange.permission.GENERAL_ACCESS
  permission:huawei.android.permission.HW_SIGNATURE_OR_SYSTEM
  permission:android.permission.USES_HW_LOG_SERVICE
  permission:com.google.android.providers.gsf.permission.WRITE_GSERVICES
  permission:com.huawei.gallery.permission.PRIVATE_GALLERY
  permission:com.google.android.gms.auth.permission.GOOGLE_ACCOUNT_CHANGE
  permission:com.huawei.intelligent.permission.WRITE_INTELLIGENT_PROVIDER
  permission:com.qq.AppService.permission.out.CACHE_WRITE_PERMISSION
  permission:android.permission.CONTROL_KEYGUARD
  permission:com.android.server.telecom.permission.REGISTER_PROVIDER_OR_SUBSCRIPTION
  permission:com.android.email.permission.ACCESS_PROVIDER
  permission:com.huawei.hwid.ACTION_MAIN_SETTING_ACCESS
  permission:android.permission.INTERNAL_SYSTEM_WINDOW
  permission:com.android.huawei.permission.OUTSIDE_STOP_FM
  permission:android.permission.DOWNLOAD_CACHE_NON_PURGEABLE
  permission:org.simalliance.openmobileapi.SMARTCARD
  permission:android.permission.MASTER_CLEAR
  permission:android.permission.FORCE_BACK
  permission:android.permission.BIND_TRUST_AGENT
  permission:android.permission.RECV_PRIVACY_MODE_CHANGED
  permission:com.huawei.gallery.permission.GALLERY_PROVIDER
  permission:com.huawei.android.launcher.permission.CHANGE_BADGE
  permission:android.permission.CHANGE_COMPONENT_ENABLED_STATE
  permission:com.google.android.marvin.talkback.permission.LABELING
  permission:com.huawei.android.totemweather.permission.ACCESS_WEATHERCLOCK_PROVIDER
  permission:com.android.huawei.permission.OUTSIDE_LAUNCH_RECORD_LIST
  permission:com.huawei.motion.permission.READ_DATA
  permission:com.android.bluetooth.permission.ACCESS_RECEIVE_HISTORY
  permission:com.huawei.vassistant.providers.settings.permission.WRITE_ONLY
  permission:com.huawei.skytone.permission.VSIM_BUSSINESS
  permission:android.permission.TRUST_LISTENER
  permission:android.permission.BROADCAST_CALLLOG_INFO
  permission:com.huawei.gallery.permission.START_APP
  permission:com.android.huawei.permission.SOUNDRECORDER_PLAY_ACTION
  permission:com.huawei.permission.INTELLIGENT_NOTIFICATION_MSG
  permission:com.huawei.KoBackup.permission.EMERGENCY
  permission:android.permission.STATUS_BAR_SERVICE
  permission:android.permission.SERIAL_PORT
  permission:android.permission.READ_INPUT_STATE
  permission:android.permission.BIND_NFC_SERVICE
  permission:android.permission.PACKAGE_VERIFICATION_AGENT
  permission:com.eg.android.AlipayGphone.permission.MIPUSH_RECEIVE
  permission:com.huawei.android.FloatTasks.readPermission
  permission:com.huawei.camera.permission.RAPID_CAPTURE
  permission:com.android.huawei.permission.OUTSIDE_RECORD
  permission:com.android.permission.SEND_HUAWEI
  permission:com.android.smspush.WAPPUSH_MANAGER_BIND
  permission:com.google.android.gms.permission.CAR_VENDOR_EXTENSION
  permission:com.huawei.android.wfdft.permission.ACCESS_RECEIVE_HISTORY
  permission:com.android.contacts.permission.WRITE_CONTACTS_PRIVACY_DATA
  permission:com.google.android.gms.permission.BIND_NETWORK_TASK_SERVICE
  permission:android.permission.GRANT_REVOKE_PERMISSIONS
  permission:android.permission.WRITE_PRE_INSTALLED
  permission:com.android.permission.WHITELIST_BLUETOOTH_DEVICE
  permission:com.huawei.bluetooth.permission.ACCESS_INTERFACE
  permission:com.huawei.gamebox.permission.downloadmanager
  permission:com.android.gallery3d.permission.GALLERY_PROVIDER
  permission:android.permission.CAPTURE_VIDEO_OUTPUT
  permission:android.permission.BROADCAST_SCORE_NETWORKS
  permission:com.huawei.powergenie.writePermission
  permission:com.huawei.powergenie.readPermission
  permission:com.google.android.gms.cloudsave.BIND_EVENT_BROADCAST
  permission:com.huawei.skytone.HW_WIFI_ICON_EXIT
  permission:com.huawei.android.totemweather.permission.home_city_weather
  permission:com.android.packageinstaller.permission.HUAWEI_PACKAGEINSTALLER_ACCESS
  permission:com.google.android.gms.auth.trustagent.permission.TRUSTAGENT_STATE
  permission:android.permission.MODIFY_PARENTAL_CONTROLS
  permission:com.huawei.phone.permission.SUPP_SERVICE_FAILURE
  permission:android.permission.MMS_SEND_OUTBOX_MSG
  permission:android.permission.IBINDER_APP_WIDGET_SERVICE
  permission:com.android.permission.airsharing_sensor_interface
  permission:android.permission.MANAGE_NETWORK_POLICY
  permission:android.permission.CAPTURE_AUDIO_OUTPUT
  permission:android.permission.INSTALL_PACKAGES
  permission:android.permission.HUAWEI_SYSTEM_NODE_ACCESS
  permission:android.permission.INSTALL_LOCATION_PROVIDER
  permission:com.android.keyguard.permission.RECEIVE_COVER_STATE
  permission:com.huawei.intelligent.permission.READ_INTELLIGENT_PROVIDER
  permission:android.permission.ACCESS_DRM_CERTIFICATES
  permission:com.google.android.marvin.feedback.permission.TALKBACK
```

---
### 参考文章
* [权限概述][topics_permissions]
---
[topics_permissions]: https://developer.android.com/guide/topics/permissions/overview