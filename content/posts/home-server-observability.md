+++
title = "Home server observability 101"
date = "2025-12-09T21:18:09+13:00"
#dateFormat = "2006-01-02" # This value can be configured for per-post date formatting
description = "In my [previous post](/posts/beyla) I wrote a bit about how I monitor my home server, and how I use Grafana Beyla to get traces and metrics from services with no existing telemetry.\n\nThis time, I'm going to go through how to set up your own observability stack for home server scale, and how to start collecting metrics, logs, and traces."
showFullContent = false
readingTime = false
hideComments = false
+++
In my [previous post](/posts/beyla) I wrote a bit about how I monitor my home server, and how I use Grafana Beyla to get traces and metrics from services with no existing telemetry.

This time, I'm going to go through how to set up your own observability stack for home server scale, and how to start collecting metrics, logs, and traces.
## Why bother?
If you're running a homelab, you're probably somewhat interested in monitoring already - it's an important part of operating actual systems, and the whole point of homelabbing is to ~~burn money~~ learn new things.

For home server folks, you might sit in the same category as above, but it can still be pretty useful in practice. It's pretty annoying to sit down to watch a movie only to find out your server has fallen over (ask me how I know), so having robust monitoring can alert you before issues happen, and help you diagnose them when they do.

The last reason is because graphs are cool. More graphs is more good.
## Telemetry signals and standards
