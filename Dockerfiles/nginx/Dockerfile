FROM public.ecr.aws/amazonlinux/amazonlinux:2.0.20230404.0-arm64v8
RUN yum update -y \
    && yum install net-tools -y \
    && yum install procps -y \
    && amazon-linux-extras install nginx1 -y \
    && yum install install nginx-mod-stream -y \
    && mv /etc/nginx/nginx.conf /etc/nginx/nginx.conf.orig
COPY nginx.conf /etc/nginx/
CMD ["nginx", "-g", "daemon off;"]