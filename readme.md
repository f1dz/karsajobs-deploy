Karsajobs Deploy
================

Before you go
-------------
We should deploy `mongodb` and the `backend` first then get the IP address and port which the backend run on. 

Run this command to deploy `mongodb` and the `backend`:
```sh
make apply-mongo
make apply-backend
```
After we got the IP and port, update `karsajobs-ui-deployment.yml` line number `30` with the given IP and port.

To deploy the frontend service simply execute command as follows:
```sh
make apply-frontend
```