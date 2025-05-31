Authenticated Login
``curl -u http://user:pass@<SERVER_IP>:<PORT>/

```curl -u user:pass http://<SERVER_IP>:<PORT>/```

Setting Authorization via Header
```curl -H 'Authorization: Basic YWRtaW46YWRtaW4=' http://<SERVER_IP>:<PORT>/```

Using Param to search php file
```curl -iv -H 'Authorization: Basic YWRtaW46YWRtaW4=' 'http://94.237.60.52:53663/search.php?search=flag'```

Sending a Post Request:
```
curl -X POST -d 'username=admin&password=admin' http://<SERVER_IP>:<PORT>/
```


Setting the cookie to prevent re-authentication
``curl -b 'PHPSESSID=c1nsa6op7vtk7kdis7bcnbadf1' http://<SERVER_IP>:<PORT>/

Setting the cookie via Header
`curl -H 'Cookie: PHPSESSID=c1nsa6op7vtk7kdis7bcnbadf1' http://<SERVER_IP>:<PORT>/


Setting the body using json content type
`curl -X POST -d '{"search":"london"}' -b 'PHPSESSID=c1nsa6op7vtk7kdis7bcnbadf1' -H 'Content-Type: application/json' http://<SERVER_IP>:<PORT>/search.php


Updating the database table city with london
`curl -X PUT http://<SERVER_IP>:<PORT>/api.php/city/london

curling the database table city to get the information on london
`curl http://<SERVER_IP>:<PORT>/api.php/city/london

silently curling the database table city for information while jquery makes it pretty
`curl -s http://<SERVER_IP>:<PORT>/api.php/city/london | jq

silently curling the database table city while searching via string
`curl -s http://<SERVER_IP>:<PORT>/api.php/city/le | jq

silently curling database table city while searching with empty string
`curl -s http://<SERVER_IP>:<PORT>/api.php/city/ | jq

adding entry to table
`curl -X POST http://<SERVER_IP>:<PORT>/api.php/city/ -d '{"city_name":"HTB_City", "country_name":"HTB"}' -H 'Content-Type: application/json'

-X can be used with POST, PUT DELETE, PATCH, OPTIONS