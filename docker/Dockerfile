FROM nginx

COPY ./nginx.conf /etc/nginx/nginx.conf
RUN rm -rf /etc/nginx/conf.d
ADD ./conf.d /etc/nginx/conf.d

RUN apt update
RUN apt install -y git

RUN git clone https://github.com/yuqiangcn/galery 

WORKDIR /galery

EXPOSE 8080

CMD ["nginx", "-g", "daemon off;"]

