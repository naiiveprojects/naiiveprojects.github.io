---
title: "AISE"
type: docs
prev: projects/application
tags: ["Software", "Mobile"]
---

AISE is a software built using [gd.x](https://github.com/naiiveprojects/gd.x/), offering users a suite of tools for image creation and modification. designed as a mobile application, its inception aimed to integrate cutting-edge artificial intelligence technology.

## Motivation

AISE was initially constructed within a limited timeframe, with a maximum duration of one day. The primary objective was to swiftly incorporate state-of-the-art Artificial Intelligence technology for proof of concept and as a fundamental exercise in mobile device design.

Subsequently, as development progressed and further research was conducted, the decision was made to expand its functionality into a fully functional tool accessible for everyone.

### Problem

While Artificial Image Generators have become more accessible to the general public, it remains evident that using such programs can still be costly. Users typically need a powerful GPU or must invest financially to make the software truly "usable." Even when users can access it for free, there's often a trade-off, such as watching ads or providing their data for undisclosed purposes.

This practice is understandable because developers incur significant expenses in operating Artificial Intelligence systems. These costs include not only bandwidth and electricity but also infrastructure maintenance. Moreover, serving hundreds of thousands, if not millions, of requests daily further compounds the financial challenges.

{{< callout type="info" >}}
  Article work in progress.
{{< /callout >}}

AISE use [AI Horde](https://stablehorde.net/) a crowd sourced distributed cluster of Image generation workers and text generation workers. if you like consider joining the horde yourself!

## Detail

{{% details title="Features" closed="true" %}}

- [Stable Diffusion](https://github.com/Stability-AI/StableDiffusion) Served by [AI Horde](https://stablehorde.net/)
  - Models
  - Text to Image
  - Image to Image
  - ControlNet
  - Tiling
  - & More
- LoRA by [Civit AI](https://civitai.com/)
- Style Prompt injection using [CheatSheet](https://github.com/SupaGruen/StableDiffusion-CheatSheet/tree/main/src)
- image editing
- sketch
- Discovery
- gallery
- Reporting Tool
- Version Checking
- Text Translation [Google Translate API](https://cloud.google.com/translate/docs/reference/rest/)
- Image Optimization [Resmush API](https://resmush.it/)

{{% /details %}}

{{% details title="Resources" closed="true" %}}

| url | type | description |
|-----|------|-------------|
| [Itch.io](https://naiive.itch.io/aise) | `page`, `HTML5` | executable & more user friendly explanation |
| [Android](https://github.com/naiiveprojects/res/blob/main/AISE/AISE_prod_android.apk) | `installer` as `apk` | target platform |
| IOS | N/A | target platform |
| [Windows](https://github.com/naiiveprojects/res/blob/main/AISE/AISE_prod_windows.zip) | `portable` as `exe` in `zip` | for testing, main development operating system |
| [MacOS](https://github.com/naiiveprojects/res/blob/main/AISE/AISE_prod_mac.zip) | `unknown` as `zip` | for testing, untested / reported |
| [Linux](https://github.com/naiiveprojects/res/blob/main/AISE/AISE_prod_linux.zip) | `portable` as `x86_64` in `zip` | for testing, untested / reported |

{{% /details %}}

{{% details title="Report" closed="true" %}}

from developing AISE we create & introduce some new and refined component & class we can share and utilize in the future

| name | type | description |
|------|------|-------------|
| `stable_horde_api` | `resources` | stable horde APIs wrapper with helper class, it has `resume` method that will try to retrieve the last known `task` |
| `texture_showcase` | `.tscn` | iterate & animate part / position from atlas texture. |
| `texture_dock` | `HTTPRequest` | optimize, download, cached image from internet in batch and assign it to the requested node. |
| `google_translate_api` | `HTTPRequest` | google translate APIs Wrapper, contain necessary helper. |

| name | description |
|------|-------------|
| `file_panel` | cleaned up, & add touchscreen support |
| `theme` | cleaned up, add shadow, consistency adjustment |

{{% /details %}}