**Selenium:-**
    Selenium is a software-testing framework for web applications.Selenium provides a playback tool for authoring tests without the need to learn a test scripting language.

1. Install selenium using pip
	```
    pip3 install -U selenium
    ```

2. Download chromedriver from https://sites.google.com/a/chromium.org/chromedriver/downloads. This will enable Selenium to run all the test cases with browser. The following code demonstrates the usage :

```
from selenium import webdriver
from selenium.webdriver.common.keys import Keys
browser = webdriver.Chrome()
browser.get('http://www.google.com')
print(browser.title)
browser.quit()
```
3. Suppose we do not want the browser to be displayed, but we still want the tests to occur in the background, we can modify the above code slightly. Add a `"headless"` argument to `ChromeOptions()` instead of just using `Chrome()`. The below code executes the same functionality as the one above, without displaying the browser :
```
from selenium import webdriver
from selenium.webdriver.common.keys import Keys
options = webdriver.ChromeOptions()
options.add_argument('headless')
browser = webdriver.Chrome(options = options)
browser.get("http://www.google.com")
print(browser.title)
browser.close()
```
