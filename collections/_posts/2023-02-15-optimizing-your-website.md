---
layout: post
title: "Optimizing Your Website And Speed up"
date: 2023-02-15T10:20:00Z
categories: ["Development", "Web Design"]
description: "Making sure your website runs fast and loads quickly is a fundamental part of the web design and seo process."
thumbnail: "/assets/images/gen/blog/blog-2-thumbnail.webp"
image: "/assets/images/gen/blog/blog-2.webp"
---

[PSI](https://pagespeed.web.dev/) classifies the quality of user experiences into three buckets: Good, Needs Improvement, or Poor. PSI sets the following thresholds in alignment with the Web Vitals initiative:

<table>

<tbody>

<tr>

<th></th>

<th>Good</th>

<th>Needs Improvement</th>

<th>Poor</th>

</tr>

<tr>

<td>FCP</td>

<td>[0, 1800ms]</td>

<td>(1800ms, 3000ms]</td>

<td>over 3000ms</td>

</tr>

<tr>

<td>FID</td>

<td>[0, 100ms]</td>

<td>(100ms, 300ms]</td>

<td>over 300ms</td>

</tr>

<tr>

<td>LCP</td>

<td>[0, 2500ms]</td>

<td>(2500ms, 4000ms]</td>

<td>over 4000ms</td>

</tr>

<tr>

<td>CLS</td>

<td>[0, 0.1]</td>

<td>(0.1, 0.25]</td>

<td>over 0.25</td>

</tr>

<tr>

<td>INP (experimental)</td>

<td>[0, 200ms]</td>

<td>(200ms, 500ms]</td>

<td>over 500ms</td>

</tr>

<tr>

<td>TTFB (experimental)</td>

<td>[0, 800ms]</td>

<td>(800ms, 1800ms]</td>

<td>over 1800ms</td>

</tr>

</tbody>

</table>

## Properly size images

Serve images that are appropriately-sized to save cellular data and improve load time.

Ideally, your page should never serve images that are larger than the version that's rendered on the user's screen. Anything larger than that just results in wasted bytes and slows down page load time.

## Reduce unused JavaScript

Reduce unused JavaScript and defer loading scripts until they are required to decrease bytes consumed by network activity.

*Detect unused JavaScript*
[The Coverage tab in Chrome DevTools](https://developer.chrome.com/docs/devtools/css/reference/#coverage) can give you a line-by-line breakdown of unused code.

The Coverage class in Puppeteer can help you automate the process of detecting unused code and extracting used code.

## Reduce unused CSS

These suggestions can help your page load faster. They don't [directly affect](https://developer.chrome.com/docs/lighthouse/performance/performance-scoring/?utm_source=lighthouse&utm_medium=lr) the Performance score.

## First Contentful Paint

First Contentful Paint 3G marks the time at which the first text or image is painted while on a 3G network.

First Contentful Paint (FCP) is one of six metrics tracked in the Performance section of the Lighthouse report. Each metric captures some aspect of page load speed.

### improve the accessibility of your web app

These checks highlight opportunities to improve the accessibility of your web app. Only a subset of accessibility issues can be automatically detected so manual testing is also encouraged.

> [See here](https://web.dev/accessible/)
