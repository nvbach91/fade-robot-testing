# Fade.cz Robot Framework Selenium Testing

### Prerequisites
* Install [Mozilla Firefox](https://www.mozilla.org/en-US/firefox/new/)
* Install [Google Chrome](https://www.google.com/chrome/)
* Download [Chrome Driver](https://sites.google.com/a/chromium.org/chromedriver/downloads), unzip to a folder and set the folder's path in system Path
* Download [Gecko Driver](https://github.com/mozilla/geckodriver/releases), unzip to a folder and set the folder's path in system Path
* Install [Python 2.7.13](https://www.python.org/downloads/), remember to choose the option to set it's path in system Path
* Install [Robot Framework](https://github.com/robotframework/robotframework#installation)
* Install [Selenium 2 library](https://github.com/robotframework/Selenium2Library#user-content-installation)

### Project
* Clone git repo
```{r, engine='sh'}
git clone https://github.com/nvbach91/fade-robot-testing.git
```

* Run a test
```{r, engine='sh'}
robot .\Tests\TC01.txt
```

* Run all tests
```{r, engine='sh'}
robot .\Tests
```

### Code convention
* Please use 4 spaces instead of tab when writing code


### Ignore images for faster testing
* modify file ```~\Python27\Lib\site-packages\selenium\webdriver\chrome\options.py``` on line 31
```
self._experimental_options = {
    "prefs" : {
        "profile.managed_default_content_settings.images": 2
    }
}
```