# NAME

matrix-bridges

# SYNOPSYS

A Docker-Compose set-up for a Matrix server (Synapse) with a client
(Element), and selected bridges to other platforms.

# PROVENANCE

It is adapted from the blog posts here, which is offline at the time
of writing, hence the use of archive.org copies. The original is
somewhat old, so some things needed to be updated. For instance Riot
is now Element. It also has a reverse-proxy container added, in order
to avoid needing an external one as in the post.

- https://web.archive.org/web/20210514183915/https://zblesk.net/blog/setting-up-a-matrix-chat-server/
- https://web.archive.org/web/20210301170955/https://zblesk.net/blog/setting-up-matrix-bridges/

The bridge configs are also missing in the original post.

# USAGE

To start, you need docker and docker-compose installed, obvs.

Check out this repository, e.g.

    cd /opt
    git clone $REPO_URL matrix-bridge

Run docker-compose there:

    cd /opt/matrix-bridge
    docker compose up -d

For a more permanent and robust solution, you should create a systemd
service which starts docker compose. For instance, see this thread:

https://askubuntu.com/questions/1459175/how-to-run-a-docker-compose-as-a-systemd-service

# CAVEATS

Work in progress! This is not yet finished nor really tested to work as advertised.