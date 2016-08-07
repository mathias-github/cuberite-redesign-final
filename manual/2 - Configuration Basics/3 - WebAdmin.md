---
sitemap: false
---
The WebAdmin allows you to control various aspects of Cuberite, including player permissions. A typical ***webadmin.ini*** configuration looks like this:

<div class="code-box">
[User:john]<br/>
Password=cuberiteRocks<br/>
<br/>
[WebAdmin]<br/>
Ports=8080<br/>
Enabled=1
</div>

In the example above, you can login to the web admin using the username ***john*** and the password ***cuberiteRocks*** by pointing your browser to ***http://\<Server IP address\>:8080***. If you're running your server locally, point your browser to ***http://localhost:8080***.
