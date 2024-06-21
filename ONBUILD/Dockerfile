FROM almalinux:9
RUN dnf install nginx -y
RUN rm -rf /usr/share/nginx/html/index.html
# here we did not provide any index.html in this directory but since we used ONBUILD instruction, it will not give any error.. Error will be thrown only when this image is used by any other like in test folder
ONBUILD COPY index.html /usr/share/nginx/html/index.html
CMD [ "nginx","-g","daemon off;" ]