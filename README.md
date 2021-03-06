# crDroid OTA repo
OTA configuration for crDroidOTA (push OTA info when new build is ready for device users)

## Introduction ##
In order for a device to be OTA compliant, there are a few things to know. 

## XML structure ##
```
      <manufacturer id="Manufacturer">
            <DeviceCode>
                  <maintainer>MaintainerName</maintainer>
                  <devicename>DeviceName</devicename>
                  <filename>FileName</filename>
                  <buildtype>BuildType</buildtype>
                  <download>DownloadLink</download>
                  <changelog>ChangelogLink</changelog>
                  <gapps>GappsLink</gapps>
                  <forum>ForumLink</forum>
                  <paypal>PaypalLink</paypal>
                  <telegram>TelegramLink</telegram>
            </DeviceCode>
      </manufacturer>
```

### Mandatory XML tags ###
* **Manufacturer** - Add under existing manufacturer (create manufacturer if required)
* **DeviceCode** - Device code name
* **MaintainerName** - Maintainer name followed by prefered name in parenthesis
* **DeviceName** - Device name (not code name)
* **FileName** - Latest crdroid build name (OTA code parses date to check for new version - don't include file extension .zip)
* **BuildType** - Nightly/Weekly/Final
* **DownloadLink** - Official download folder url (from AFH) masked by bit.ly shortlinks
* **ChangelogLink** - Changelog url (GitHub)
* **GappsLink** - Google apps url (preferred: opengapps url)
* **ForumLink** - Forum url for discussions and support (preferred: xda url)

*All mandatory XML tags need to be there. Please leave blank in case some do not apply to you.*

### Optional XML tags ###
* **PaypalLink** - paypal url (for donations)
* **TelegramLink** - telegram url (if you offer support via telegram - can be a group link or telegram.me link)

## Guidelines ##
* Check if manufacturer is already existing
* Check if published link is official
* Check if XML is intact
* Check if no extra / missing spaces  

## Notice: ##  
Due to the fact the XML does not accept "&" in tags, there is a need to shortlink your download links  
Please note that **goo.gl** is going down starting **April 13 2018** ([source](https://developers.googleblog.com/2018/03/transitioning-google-url-shortener.html)) it's advised to use **[bitly](https://bitly.com)** as alternative
