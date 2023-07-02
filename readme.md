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

Images Used in this deployment
-------------------------
1. [MongoDB](https://hub.docker.com/_/mongo) _(*We are using MongoDB V3)_
2. [Backend](https://github.com/f1dz/karsajobs-backend/pkgs/container/karsajobs), get the source [here](https://github.com/f1dz/karsajobs-backend).
3. [Frontend](https://github.com/f1dz/karsajobs-frontend/pkgs/container/karsajobs-ui), get the source [here](https://github.com/f1dz/karsajobs-frontend).

Grafana
-------
In this project I'm using [Node Exporter Full](https://grafana.com/grafana/dashboards/1860-node-exporter-full/) dashboard, the dashboard's screenshot will looks like this
![Grafana Dashboard](/img/grafana-dashboard.png "Grafana Dashboard")

CI Configuration
----------------
As we are using Github Action as CI, the workflows can be found in each repositories of the sources.
1. [Backend CI](https://github.com/f1dz/karsajobs-backend/blob/master/.github/workflows/publish.yaml)
2. [Frontend CI](https://github.com/f1dz/karsajobs-frontend/blob/master/.github/workflows/publish.yaml)