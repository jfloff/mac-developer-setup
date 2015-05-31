# General Settings

![](https://33.media.tumblr.com/51e823c71b55ccbda3b83501ec7bc78a/tumblr_nojspeQLd81uqyj6qo1_500.gif)

Is that a bunch a screenshots? Yup! There's a screenshot for each main OSX Yosemite *Systems Settings* panel, so next time I know exactly my settings.

#### General

![](general.png)


#### Dock

![](dock.png)


#### Mission Control

![](mission control.png)


#### Hot Corners

![](hot corners.png)

#### Security & Privacy

![](security.png)

I changed my password to use a one different from my iCloud account. I also turned on Firewall. Better safe than sorry.


#### Spotlight

![](spotlight.png)

As you can notice, I disable Spotlight shortcut. And that's because I use an even better app: [Alfred](http://www.alfredapp.com/). Hence, I disable the Spotlight shortcut and use that one for Alfred. 

Furthermore, I disable spotlight shortcut from the menubar with the following terminal command (reboot after):

```shell
sudo chmod 600 /System/Library/CoreServices/Search.bundle/Contents/MacOS/Search
```

This does not completely disable Spotlight, it only removes its GUI. To re-enable it, just do (reboot after):

```shell
sudo chmod 755 /System/Library/CoreServices/Search.bundle/Contents/MacOS/Search
```
#### Notifications

First of all I removed the apps I don't use: Mail and Safari.


#### iCloud

On iCloud I removed the apps that I don't use: Mail and Safari. Then, I setup iCloud Drive, Photos sharing with iOS, Keychain and Back to my Mac.


