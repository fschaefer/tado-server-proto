tado-server-proto
=================

Protocol for JSON-based communication via HTTP GET between Android App and tado server:

Homepage: http://www.tado.com/de/

Current endpoint for communication: https://my.tado.com/mobile/1.3


    POST: /updateLocation
    request:
    {
        "mode": "APP_TRIGGERED",
        "username": "",
        "password":"",
        "latitude:"xx.xxxx",
        "longitude:"xx.xxxx"
        "accuracy": "60.0",
        "batteryLevel":" 53",
        "debugString": "attempt-1-unsentFixes-0-"
    }
    response:
    {
        "homeFence": "",
        "homeGeolocationLatitude": "",
        "homeGeolocationLongitude": "",
        "minDistance": "",
        "minTime": 120000
        "regionDistances": Array[20],
        "success": true|false,
        "triggerInterval": "",
        "wakeupInterval": ""
    }


    GET: /getAppUsers
    request:
    {
        "username": "",
        "password": ""
    }
    response:
    {
        "currentUser": "",
        "appUsers": ""
    }


    GET: /createAppUser
    request:
    {
        "username": "",
        "password": "",
        "nickname": "",
        "geoTrackingEnabled": true|false,
        "deviceName": "",
        "devicePlatform": "",
        "deviceUuid": "",
        "deviceOsVer": "",
        "appVersion": ""
    }
    response:
    {
        "username": "",
        "password": "",
        "nickname": "",
        "geoTrackingEnabled": true|false,
        "privacyEnabled": true|false
    }


    GET: /claimAppUser
    request:
    {
        "username": "",
        "password": "",
        "nickname": "",
        "geoTrackingEnabled": true|false,
        "deviceName": "",
        "devicePlatform": "",
        "deviceUuid": "",
        "deviceOsVer": "",
        "appVersion": ""
    }
    response:
    {
        "username": "",
        "password": "",
        "nickname": "",
        "geoTrackingEnabled": true|false,
        "privacyEnabled": true|false
    }


    GET: /getCurrentState
    request:
    {
        "username": "",
        "password": ""
    }
    response:
    {
        "operation": "",
        "insideTemp": "",
        "setPointTemp": "",
        "controlPhase": "",
        "currentUserPrivacyEnabled": true|false
    }


    GET: /getThermostatSettings
    request:
    {
        "username": "",
        "password": ""
    }
    response:
    {
        "setMode": "",
        "manualTemp": "",
        "homeTemp": "",
        "sleepTemp": "",
        "comfortLevel": "",
        "deactivateHomeButton": ""
    }


    GET: /updateThermostatSettings
    request:
    {
        "username": "",
        "password": "",
        "comfortLevel": "",
        "setMode": "",
        "deactivateHomeButton", "",
        "manualTemp": "",
        "homeTemp": "",
        "sleepTemp": ""
    }
    response:
    {
        "setMode": "",
        "manualTemp": "",
        "homeTemp": "",
        "sleepTemp": "",
        "comfortLevel": "",
        "deactivateHomeButton", ""
    }


    GET: /getAppUserSettings
    request:
    {
        "username": "",
        "password": ""
    }
    response:
    {
        "stateChangeNotifications": true|false,
        "settingsChangeNotifications": true|false,
        "systemInfoNotifications": true|false,
        "rewardNotifications": true|false,
        "geoTrackingEnabled": true|false,
        "privacyEnabled", true|false
    }


    GET: /updateAppUserSettings
    request:
    {
        "username": "",
        "password": "",
        "stateChangeNotifications": true|false,
        "settingsChangeNotifications": true|false,
        "systemInfoNotifications": true|false,
        "rewardNotifications": true|false,
        "geoTrackingEnabled": true|false,
        "privacyEnabled", true|false
    }
    response:
    {
        "stateChangeNotifications": true|false,
        "settingsChangeNotifications": true|false,
        "systemInfoNotifications": true|false,
        "rewardNotifications": true|false,
        "geoTrackingEnabled": true|false,
        "privacyEnabled", true|false
    }


    GET: /getNotifications
    request:
    {
        "username": "",
        "password": "",
        "fromDate": "",
        "toDate": "",
        "locale": "",
        "max": "",
        "lastMessageId": ""
    }
    response:
    {
        "notifications": {},
        "messages", {}
    }


    GET: /getScheduleContainer
    request:
    {
        "username": "",
        "password": ""
    }
    response:
    {
        "scheduleContainer": {
            "residentsWithoutCellphone": true|false,
            "currentScheduleType": "ONEDAY|ANYDAY|THREEDAY|SEVENDAY|WORKDAY|SATURDAY|SUNDAY|MONDAY|TUESDAY|WEDNESDAY|..."
            "oneDaySchedule": {},
            "threeDaySchedule": {},
            "sevenDaySchedule": {}
    }


    GET: /updateScheduleContainer
    request:
    {
        "username": "",
        "password": ""
    }
    response:
    {
        "scheduleContainer": {
            "residentsWithoutCellphone": true|false,
            "currentScheduleType": "ONEDAY|ANYDAY|THREEDAY|SEVENDAY|WORKDAY|SATURDAY|SUNDAY|MONDAY|TUESDAY|WEDNESDAY|..."
            "scheduleDayType": "ONEDAY|ANYDAY|THREEDAY|SEVENDAY|WORKDAY|SATURDAY|SUNDAY|MONDAY|TUESDAY|WEDNESDAY|...",
            "getup": "",
            "leaving": "",
            "arrival": "",
            "sleep": ""
    }
