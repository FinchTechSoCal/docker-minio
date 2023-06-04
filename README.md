# docker-minio
MinIO S3

Use this on the proxy:

# Use these on proxy for each
## Allow special characters in headers
#ignore_invalid_headers off;
## Allow any size file to be uploaded.
## Set to a value such as 1000m; to restrict file size to a specific value
#client_max_body_size 0;
## Disable buffering
#proxy_buffering off;
#proxy_request_buffering off;
#proxy_set_header Host $http_host;
#proxy_set_header X-Real-IP $remote_addr;
#proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
#proxy_set_header X-Forwarded-Proto $scheme;
#proxy_connect_timeout 300;
## Default is HTTP/1, keepalive is only enabled in HTTP/1.1
##proxy_http_version 1.1;
#proxy_set_header Connection "";
#chunked_transfer_encoding off;



Notes: https://wiki.alex.lol/books/justsysadminthings/page/minio-server-docker-compose-nginx-reverse-proxy
