# cors-poc
Dockerized version of https://github.com/trustedsec/cors-poc.

See https://www.trustedsec.com/2018/04/cors-findings/ to understand situations where this could be useful.

## Usage

* Edit **corstest.html** to update [target-site/target-page] and [our-server].
* Start [our-server] and host corstest.html in container 
$`docker run -p 8000:8000 -v /log madkasper/cors-poc`
* Browse to **http://[our-server]:8000/corstest.html** from a "victim" browser.

This will start a web server hosting **corstest.html** on port 8000 to capture cross-origin responses
from the victim browser. Responses will be displayed and stored in **/log/captured-post-data.txt**.

