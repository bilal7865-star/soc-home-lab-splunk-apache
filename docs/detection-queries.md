# Detection Queries & Alert Configuration

## Main Detection Search

spl
index=main sourcetype=apache:access 
("/etc/passwd" OR "phpmyadmin" OR ".env" OR "wp-login" OR "admin'" OR "../../../")
| table _time, clientip, request, status, useragent
| sort -_time

## Alert Configuration
Alert Name: Suspicious Web Attack Detected

Trigger: Number of results > 0

Action: Webhook

Webhook URL: Configured to send to Shuffle SOAR

## Attack Patterns Detected

Directory Traversal

Common Admin Panel Scanning

Environment File Access Attempts

SQL Injection-like patterns
