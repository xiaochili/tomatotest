FROM nginx
LABEL "Project"="Tomato"
LABEL "Author"="Imran"

RUN rm -rf /etc/nginx/conf.d/default.conf
COPY ngintomato.conf /etc/nginx/conf.d/tomatoapp.conf