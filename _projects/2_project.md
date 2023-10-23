---
layout: page
title: cosmic microwave background
description: data pipeline development for the Cosmology Large Angular Scale Surveyor (CLASS)
img: assets/img/cut.png
importance: 2
category: undergraduate
giscus_comments: true
---

During my time working with the [Cosmology Large Angular Scale Surveyor (CLASS)](https://sites.krieger.jhu.edu/class/) team at Johns Hopkins University, I worked with Dr. Joseph Eimer to develop the data processing pipeline. The scientific goal of CLASS is to detect B-Mode polarization from the cosmic microwave background. A detection of this form of polarization at these wavelengths would most likely be explained by gravitational waves formed by inflationary expansion shortly after the Big Bang.

The detectors on the CLASS telescopes, located in the High Altacama Desert of Chile, take time to receive signals. As a result, the same data may be received at different times for different detectors. Among the issues this can cause is difficulty locating and cutting calibration activities (called relocs) from the dataset.

I developed an algorithm to group the detectors based on when they observe the reloc, pinpoint the time that the reloc occurs for each group, then cut out the period right before and after the reloc.

I wrote the following documentation explaining the design of my algorithm (Note: this was intended to be shared with other team members, so there is a lot of jargon).

{::nomarkdown}
{% assign jupyter_path = "assets/jupyter/refine_relock_outline.ipynb" | relative_url %}
{% capture notebook_exists %}{% file_exists assets/jupyter/blog.ipynb %}{% endcapture %}
{% if notebook_exists == "true" %}
    {% jupyter_notebook jupyter_path %}
{% else %}
    <p>Sorry, the notebook you are looking for does not exist.</p>
{% endif %}
{:/nomarkdown}
