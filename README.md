# hacky-reverse-proxy
a bit of a hack to allow traefik to redirect to external hosts using nginx as a relay container

## Disclaimer : 

There are now better ways to do that but I think they only work with static changes to traefik.toml

## Basic usage :

### Configure :
Edit the proxy-pass IP in nginx/default.conf

Edit proxy.yaml and change settings to expose your nginx container on the URL you want you external IP to respond.

### build the nginx-external container : 
 
```docker build . -t nginx-external```

```docker stack deploy proxy -c proxy.yaml```




