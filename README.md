# feature

- acceptance.suite.yml is ready for testing on firefox and chrome
- use .env file
- http proxy can be set in .env ( used for http_proxy and ssl_proxy, the latter is for https)


Env
===========


1. `composer install`
2. Copy `.env.example` to `.env` then edit `.env`
3. To use WebDriver module, follow https://codeception.com/docs/modules/WebDriver
  - java
  - chrome
  - firefox
  - 
        


Start
===========

Selenium
```
SET driver_dir=D:\Dropbox\little_softwares\webdrive
SET selenium_server="%driver_dir%\selenium-server-standalone-3.141.59.jar
SET chromedriver="%driver_dir%\chromedriver_for_chrome_81.0.4044.69.exe"
SET geckodriver="%driver_dir%\geckodriver.exe"
java -Dwebdriver.chrome.driver=%chromedriver% -Dwebdriver.gecko.driver=%geckodriver% -jar %selenium_server% -port 44445
```


Test
```
vendor\bin\codecept.bat run --steps --env chrome
```