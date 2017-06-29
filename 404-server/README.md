# 404-server (default backend)

404-server is a simple webserver that satisfies the ingress, which means it has to do two things:

 1. Serves a configurable 404 page at `/`
 2. Serves 200 on a `/healthz`

## How to define the 404 page

The 404 page's content can be passed to the Docker container in an Environment Variable called ``PAGE_CONTENT_404``

A simple text will be sent as the content of the 404 response in absence of this env var.

## How to release:

If you are releasing a new version, please bump the `TAG` value in the `Makefile` before building the images.

    make container
