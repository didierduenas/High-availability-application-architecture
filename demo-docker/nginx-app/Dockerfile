FROM nginx

COPY nginx.conf /etc/nginx/nginx.conf
COPY hello-siteflowland.conf /etc/nginx/conf.d/hello-siteflowworld.conf
RUN mkdir -p /usr/share/nginx/public/hello
COPY index.html /usr/share/nginx/html/hello/index.html
EXPOSE 80
