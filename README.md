# pypi_acknowledged_example

This is an example repository that represents .pypi_acknowledged feature

## Why it's essential to validate python packages?

Finished browsing

"Starjacking" is a term used to describe a tactic where an adversary spoofs software popularity metadata to deceive
users into believing that a maliciously provided package is widely used and originates from a trusted source.
This term is particularly relevant in the context of the Python Package Index (PyPI), where many open-source software
packages are hosted via third-party package managers.

A package manager typically includes various metadata about the software and often includes a link to the package's
source code repository to assist developers in determining the trustworthiness of the software. One common statistic
used in this decision-making process is the popularity of the package, indicated by the amount of "Stars" the package
has received. However, many package managers do not validate the connection between the package and source code
repository being provided. As a result, adversaries can spoof the popularity statistic of a malicious package by
associating a popular source code repository URL with the package. This deception can trick developers into
unintentionally incorporating the malicious package into their development environment.

[StarJacking on Mitre](https://capec.mitre.org/data/definitions/693.html)

[Positive Technologies Research](https://www.ptsecurity.com/ww-en/analytics/pt-esc-threat-intelligence/unsecure-dev-p2/)

[Checkmarx Research](https://checkmarx.com/blog/starjacking-making-your-new-open-source-package-popular-in-a-snap/)

## Harmful potential of StarJacking

Starjacking poses several significant risks to both software developers and users:

1. Security Risks: The primary reason to combat starjacking is to mitigate security threats. Starjacked packages may
contain malicious code that can cause significant harm, such as data theft, unauthorized system access, or
cryptocurrency theft as seen in some examples.

2. Trust Erosion: If developers cannot trust the popularity metrics provided by package repositories, they may hesitate
to use open-source software. This could slow down development processes and limit the sharing code.

3. Damage to Reputations: Developers and organizations could suffer reputational damage if they inadvertently use and
distribute malicious code. This can lead to loss of clients or users and potential legal implications.
 
4. Potential for Widespread Harm: Given the interconnected nature of software dependencies, a single starjacked package
can impact many applications and systems. If the malicious package becomes a dependency of other widely used
packages, the potential for harm is significantly amplified.


## What does this repository represent

This repository suggests to use `.pypi_acknowledged` file to declare the list of packages on PyPI with which the
repository can be associated and, accordingly, with which it shares statistics: stars, forks, PR, etc.

This feature will prevent a lot of StarJacking causes, that often happens unintentionally.

Sometimes StarJacking is a part of malicious killchain, connected with TypoSquatting.