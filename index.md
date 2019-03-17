---
redirect_from: "/results"
layout: home
title: FCDroid
---
## Abstract
**Frame Confusion** is a vulnerability affecting hybrid applications which allows circumventing the isolation granted by the **Same-Origin Policy**. The detection of such vulnerability is still carried out manually by application developers, but the process is error-prone and often underestimated. In this article, we propose a sound and complete methodology to detect the Frame Confusion on Android as well as a publicly-released tool (i.e., **FCDroid**) which implements such methodology and allows to detect the Frame Confusion in hybrid applications, automatically. We also make public the results obtained by analyzing 50K apps using FCDroid, which have revealed that many hybrid applications suffer from Frame Confusion.



## The Tool

The detection of Frame Confusion  poses several challenges in terms of implementation. Indeed, an automatic detection tool needs to:
* achieve maximum coverage, i.e., by detecting all possible app execution paths that may lead to the vulnerability;
* recognize the actual configuration of WebView components, which may *dynamically* enable JavaScript or define new interfaces;
* analyze all the web pages loaded inside some potentially vulnerable WebViews, by also considering those loaded according to i) the user's input, and ii) the value of runtime variables.

To address such challenges, an automatic tool can rely on static and dynamic analysis techniques.
Static analysis techniques can examine all possible execution paths and variable values, not just those invoked during execution.
However, static approaches can *i*) introduce false positives and *ii*) be unable to detect complex scenario, like, e.g., values provided by the user or resources loaded at runtime.
On the other hand, dynamic analysis techniques allow to detect the actual behavior of the app, but it is limited by *i*) the coverage of the analysis and *ii*) the time required for the analysis, thus producing potential false negatives.
To this aim, **FCDroid** combines static and dynamic analysis techniques to overcome the limitations of both techniques and achieve more accurate detection results.
The FCDroid is composed by five main building blocks: the *Static Analysis Module (SAM)*, the *Dynamic Analysis Module (DAM)*, the *WebSite Dumper (WD)*, the *Frame Confusion Detector (FCD)* and the *Exploitation Checker (EC)*.

## Demo
*Coming soon*

## Results
*Coming soon*

## Team
* [Davide Caputo](https://csec.it/people/davide_caputo), University of Genova, Italy
* [Luca Verderame](https://www.talos-sec.com), University of Genova, Italy
* [Simone Aonzo](https://csec.it/people/simone_aonzo), University of Genova, Italy
* [Alessio Merlo](https://csec.it/people/alessio_merlo), University of Genova, Italy

## Acknowledgment
