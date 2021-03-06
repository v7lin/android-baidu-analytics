# android-baidu-analytics

[![Build Status](https://cloud.drone.io/api/badges/v7lin/android-baidu-analytics/status.svg)](https://cloud.drone.io/v7lin/android-baidu-analytics)
[![GitHub tag](https://img.shields.io/github/tag/v7lin/android-baidu-analytics.svg)](https://github.com/v7lin/android-baidu-analytics/releases)
[![API](https://img.shields.io/badge/API-14%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=14)

### snapshot

````
ext {
    latestVersion = '3.9.1.1-SNAPSHOT'
}

allprojects {
    repositories {
        ...
        maven {
            url 'https://oss.jfrog.org/artifactory/oss-snapshot-local'
        }
        ...
    }
}
````

### release

````
ext {
    latestVersion = '3.9.1.1'
}

allprojects {
    repositories {
        ...
        jcenter()
        ...
    }
}
````

### usage

android
````
...
android {
    ...
    defaultConfig{
        ...
        manifestPlaceholders = [TENCENT_APP_ID: "${appId}"]
        ...
    }
    ...
}
...
dependencies {
    ...
    implementation "io.github.v7lin:baidu-analytics-android:${latestVersion}"
    ...
}
...
````
