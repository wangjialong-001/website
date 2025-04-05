#my website
"""
超级用户里的一个配置文件mywebsite.conf，自启动服务端web程序端口绑定

nginx的配置文件mywebsite.nginx

软连接建一个
ln -s /home/mywebsite/mywebsite.conf /etc/supervisor/conf.d/mywebsite.conf
ln -s /home/mywebsite/mywebsite.nginx /etc/nginx/sites-enabled/mywebsite


mywebsite.conf

[program:mywebsite]
command=/usr/local/bin/gunicorn wsgi -c gunicorn.config.py
directory=/home/mywebsite
autostart=true
autorestart=true


gunicorn.config.py

--bind 0.0.0.0:2001
--pid /tmp/mywebsite.pid

"""