---
title: Neurosynth & Neurovault
tags: 
keywords:
last_updated: March 20, 2016
sidebar: mydoc_sidebar
permalink: /research/neurosynth-neurovault/
toc: false
---

![Neurovault]({{ "/images/research/neurovault.png" | prepend: site.baseurl }})

There are two open source websites, NeuroVault and Neurosynth, that are widely used by neuroscience researchers. NeuroVault is a public repository for brain images supported by International Neuroinformatics Coordinating Facility, Max Planck Institute for Human Cognitive and Brain Sciences and Stanford University. Neurosynth is a platform that automate the process of producing functional magnetic resonance imaging (fMRI) data. Neurosynth process the data collected from numerous neuroimaging studies and does a meta-analysis on the coordinates in each study. The result is a images with a list of Terms that it is highly associated with.

As our client has developed a new study on capturing brain data while a person watch a movie, he want to build a public database that is similar to NeuroVault and Neurosynth. The database is a combination of both sites as it should allow users to interact with the brain image and view the list of Terms that it is highly associated with and at the same time allow other neuroscience researchers to upload their data for similar study

## Neurosynth Viewer (Open Source)
Neurosynth Viewer is a CoffeeScript/JS library for visualization of functional MRI data. It provides us with a simple tools to display the brain scan image and navigation sliders to surf through a single plane. The documentation of the library is extensive and easy to implement.

* Demo: <http://pilab.psy.utexas.edu/demos/nsviewer/index.html>
* Source: <https://github.com/neurosynth/nsviewer>
