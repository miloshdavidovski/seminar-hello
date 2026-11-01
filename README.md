# seminar-hello

Source for lab 3.1 of the OpenShift seminar ITSM-10145. The Dockerfile adds one
metadata layer on top of podinfo 6.8.0 (the image `hello` runs since Day 2):
the UI message. Port 9898, /readyz, /healthz and /metrics are unchanged.

The one-line change: edit the text behind `PODINFO_UI_MESSAGE` in `Dockerfile`,
commit, push (or fork this repo and point the pipeline parameter `git-url` at
your fork). The pipeline `hello-build-deploy` rebuilds and redeploys; nothing
else changes.
