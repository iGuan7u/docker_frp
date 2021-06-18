FROM alpine:latest

CMD ["/bin/sh"]

MAINTAINER iguan7u@gmail.com

ENV FRPC_VERSION=0.37.0

RUN apk add --no-cache wget tar

RUN mkdir /frpc

WORKDIR /frpc

RUN wget https://image-1251248522.cos.ap-guangzhou.myqcloud.com/other/frp_${FRPS_VERSION}_linux_amd64.tar.gz

RUN tar -zxvf frp_${FRPC_VERSION}_linux_amd64.tar.gz

WORKDIR /frpc/frp_${FRPC_VERSION}_linux_amd64

RUN chmod +x frpc

CMD ["./frpc", "-c", "/data/frpc.ini"]
