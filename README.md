
Generated with command:
```docker run -it -v $(pwd):/app -e HTTRACK_URI=http://schema.geolink.org/index.html ralfbs/httrack:latest```

Hosted with:
```
<VirtualHost *:80>
	ServerName	schema.geolink.org

        CustomLog       "/var/log/httpd/access.log" combined
        ErrorLog        "/var/log/httpd/error.log"

        DocumentRoot    /schema.geolink.org/mirror/schema.geolink.org
        <Directory /schema.geolink.org/mirror/schema.geolink.org>
                Options Indexes ExecCGI FollowSymLinks
                Require all granted
                AllowOverride all
        </Directory>
</VirtualHost>
```
