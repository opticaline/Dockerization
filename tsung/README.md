# docker image for Tsung

```
docker run -it --rm -v ${TSUNG_XML}:/root/.tsung/tsung.xml -p 8091:8091 opticaline/tsung:latest
```

Visit [http://DOCKER_ADDRESS:8091](http://DOCKER_ADDRESS:8091) in your browser
