luvi-docker-builder
====================

Builds luvi for supported distros with docker scripts + makefiles.

Usage
-----

```bash
# required: linux install with internet and recent-ish docker installed
git clone https://github.com/luvi/luvi-docker-builder
cd luvi-docker-builder/$distro
make
```

TODO
----
* All generated RPMs are untested right now.
* Fedora 16-19 do not have official docker images. TBD how to build those.
