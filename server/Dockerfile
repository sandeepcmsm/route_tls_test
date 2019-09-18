# Docker file builds an image with a tinode chat server.
# The server exposes port 18080.
# In order to run the image you have to link it to a running RethinkDB container
# (assuming it's named 'rethinkdb') and map the port where the tinode server accepts connections:
#
# $ docker run -p 6060:18080 -d --link rethinkdb \
#	--env UID_ENCRYPTION_KEY=base64+encoded+16+bytes= \
#	--env API_KEY_SALT=base64+encoded+32+bytes \
#	--env AUTH_TOKEN_KEY=base64+encoded+32+bytes \
#	tinode-server

FROM envoyproxy/envoy-dev:d159697667435ebdb5ca3e612960453f9b94f7a6
COPY envoy.yaml /etc/envoy/envoy.yaml
