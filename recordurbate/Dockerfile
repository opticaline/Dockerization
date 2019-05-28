FROM python:alpine
MAINTAINER Opticaline <opticaline.z@gmail.com>

WORKDIR /app

RUN apk add ffmpeg curl && \
    curl https://codeload.github.com/oliverjrose99/Recordurbate/zip/master --output master.zip && \
    unzip master.zip ; mv Recordurbate-master/src/* .;rm -r Recordurbate-master && \
    rm master.zip && \
    curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl && \
    chmod a+rx /usr/local/bin/youtube-dl && \
    pip install requests && \
    apk del curl

VOLUME /app/videos

ENTRYPOINT ["sh","-c","python Recordurbate.py run" ]
