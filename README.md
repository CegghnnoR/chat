# dev-ops

docker container cp Nginx:/etc/nginx/nginx.conf D:\code\dev-ops\nginx\conf
docker container cp Nginx:/etc/nginx/conf.d/default.conf D:\code\dev-ops\nginx\conf\conf.d
docker container cp Nginx:/usr/share/nginx/html/index.html D:\code\dev-ops\nginx\html

docker run --name Nginx -p 80:80 -v D:\code\dev-ops\nginx\html:/usr/share/nginx/html -v D:\code\dev-ops\nginx\logs:/var/log/nginx -v D:\code\dev-ops\nginx\conf\nginx.conf:/etc/nginx/nginx.conf -v D:\code\dev-ops\nginx\conf\conf.d:/etc/nginx/conf.d -v D:\code\dev-ops\nginx\ssl:/etc/nginx/ssl -d --restart always --privileged=true nginx