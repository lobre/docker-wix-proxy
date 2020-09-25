# docker-wix-proxy

Docker image for a Nginx based reverse proxy for Wix websites.

## How to use

Saying your Wix site is https://myuser.wixsite.com/mysite.

    docker run -d --name wix-proxy \
        -p 80:80 \
        -e HOST=example.com \
        -e PROTO=http \ 
        -e WIX_USER=myuser \
        -e WIX_SITE=mysite \
        lobre/wix-proxy

You domain name `example.com` should resolve to the server where this container is started.

Then try to browser `http://example.com`.
