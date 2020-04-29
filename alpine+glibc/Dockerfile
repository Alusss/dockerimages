	FROM alpine
	MAINTAINER Alusss alusss@163.com
	ENV REFRESHED_AT 2020-05
	ENV GLIBC  glibc-2.31-r0
	RUN echo "http://mirrors.aliyun.com/alpine/latest-stable/main/" > /etc/apk/repositories && \
	    echo "http://mirrors.aliyun.com/alpine/latest-stable/community/" >> /etc/apk/repositories
	
	RUN apk update && \
      apk add --no-cache ca-certificates && \
	    apk add --no-cache bash tzdata && \
	    cp -rf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
	    wget -q -O /etc/apk/keys/sgerrand.rsa.pub https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub && \
	    wget https://github.com/sgerrand/alpine-pkg-glibc/releases/download/2.31-r0/$GLIBC.apk && \
	    apk add $GLIBC.apk && \
	    rm -rf $GLIBC.apk
