# safari-cookie
## A Tool for managing Safari cookies

### Info
Parse and write `.binaryCookies` format used by Safari and other iOS/OSX applications.
You can filter cookies by domain name using a blacklist or whitelist or dump the data and export in other formats.

### Usage
See python cookie.py -h for help on usage.

Default cookie storage for Safari is `~/Library/Cookies/Cookies.binarycookies`

### Automatically filter cookies
In `filter-cookie` directory there is an example script and launchd job that will filter the cookies using a whitelist.

To use this setup:
  * copy `cookie.py` in your PATH, rename it `cookie` and make it executable.
  * copy `filter-script` in `/usr/local/bin` and `rn.hmjoj.filter-cookie` in `~/Library/LaunchAgents`
  * run `launchctl load ~/Library/LaunchAgents/rn.hmjoj.filter-cookie`

Now everytime Safari writes his cookies they will be filtered.

### License
Dual licensed under the MIT and GPL licenses:  
http://www.opensource.org/licenses/mit-license.php  
http://www.gnu.org/licenses/gpl.html

Parsing is based on [this](http://www.securitylearn.net/2012/10/27/cookies-binarycookies-reader/) SecurityLean's article.
Thanks to Satishb3.

