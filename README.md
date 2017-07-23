## Description

Official Kibana image + removed xpack, tested on Openshift origin.

To upgrade/downgrade version change the version.txt file

## Running on Openshift
```
make
docker tag docker.elastic.co/kibana/kibana:5.5.0 172.30.1.1:5000/myproject/kibana:5.5.0
docker push 172.30.1.1:5000/myproject/kibana:5.5.0
oc new-app --image-stream=kibana:5.5.0
```
Documentation can be found on the [Elastic website](https://www.elastic.co/guide/en/kibana/current/docker.html).
