### artifacts:expire_in

`expire_in` allows you to specify how long artifacts should live before they expire and therefore deleted, counting from the time they are uploaded and stored on GitLab.
 If the expiry time is not defined, it defaults to the instance wide setting (30 days by default, forever on GitLab.com

 ```yaml
 job:
   artifacts:
     expire_in: 1 week
```