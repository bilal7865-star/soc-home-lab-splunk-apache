# Detection Queries & Alert Configuration

## Main Detection Search

spl
index=main sourcetype=apache:access 
("/etc/passwd" OR "phpmyadmin" OR ".env" OR "wp-login" OR "admin'" OR "../../../")
| table _time, clientip, request, status, useragent
| sort -_time
