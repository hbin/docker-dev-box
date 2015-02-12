FROM nginx:latest

# Apply Nginx configuration
COPY conf/nginx.conf /etc/nginx/nginx.conf

RUN mkdir -p /etc/nginx/sites-available /etc/nginx/sites-enabled /data/logs
COPY conf/web /etc/nginx/sites-available/web
RUN ln -s /etc/nginx/sites-available/web /etc/nginx/sites-enabled/web && \
    rm /etc/nginx/conf.d/default.conf

EXPOSE 80
CMD ["nginx"]
