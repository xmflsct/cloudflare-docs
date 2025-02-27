---
pcx_content_type: how-to
title: Enhanced HTTP/2 Prioritization
weight: 4
---

# Enhanced HTTP/2 Prioritization

With Enhanced HTTP/2 Prioritization, Cloudflare delivers resources in the optimal order for the fastest experience across all browsers. It also supports control of content delivery when used in conjunction with [Workers](/workers/).

## How it works

The speed of loading web content, from the user’s perspective, is dependent on the order in which the resources load. With HTTP/2, by default, Cloudflare will follow the order requested by the browser. This ordering varies from browser to browser, causing a significant difference in performance.

With Enhanced HTTP/2 Prioritization, Cloudflare overrides the default browser behavior to optimize the order of resource delivery, independent of the browser. The greatest improvements will be experienced by visitors using Safari and Edge browsers.

For more details, refer to [the introductory blog post](https://blog.cloudflare.com/better-http-2-prioritization-for-a-faster-web/).

## Enable Enhanced HTTP/2 Prioritization

{{<tabs labels="Dashboard | API">}}
{{<tab label="dashboard" no-code="true">}}

To enable **Enhanced HTTP/2 Prioritization** in the Cloudflare dashboard:

1. Log into the [Cloudflare dashboard](https://dash.cloudflare.com).
2. Select your account and zone.
3. Go to **Speed** > **Optimization**.
4. Go to **Protocol Optimization**.
5. For **Enhanced HTTP/2 Prioritization**, switch the toggle to **On**.

{{</tab>}}
{{<tab label="api" no-code="true">}}

To enable **Enhanced HTTP/2 Prioritization** using the Cloudflare API, send a [`PATCH` request](/api/operations/zone-settings-edit-single-setting) with `h2_prioritization` as the setting name in the URI path, and the `value` parameter set to `"on"`.

{{</tab>}}
{{</tabs>}}