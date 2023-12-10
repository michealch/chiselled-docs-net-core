# Chiselled Ubuntu for .Net
**Project by Canonical and Microsoft**
## Introduction
This document provides an overview of the chiselled / chiseled Ubuntu image for .Net
## Literature Review
Before we learn about chiselled Ubuntu, we need to about Distroless Ubuntu and Chisel.

**Distroless Ubuntu**, inspired by Google's Distroless concept, is a minimalistic version of Ubuntu. Like Google's Distroless, it has no non-essential elements such as the package manager, bash, and non-essential packages.

[**Chisel**](https://github.com/canonical/chisel) is a software tool for carving and cutting Debian packages![^1]
It is built on the idea of **package slices** - minimal, complimentary and loosely coupled sets of files, based on the package’s metadata and content. Slices are basically subsets of the Debian packages, with their own content and set of dependencies to other internal and external slices.[^1]

[![pkg-slices](https://github.com/canonical/chisel/raw/main/docs/_static/package-slices.svg)](https://github.com/canonical/chisel/blob/main/docs/_static/package-slices.svg)



**Chiselled Ubuntu for .NET** is a afford from canonical and Microsoft to build small, safe distroless image based on Ubuntu for .NET. It is similar to conventional [distroless](https://hackernoon.com/distroless-containers-hype-or-true-value-2rfl3wat), but based on Ubuntu and `.deb` packages sliced with chisel to optimize.
Pros: [^2]
1. No Shell.
2. No package manager.
3. Small in size (~100 MB Base image).
4. Non-root (app) User by default. (See following screenshot)
![nonroot User by default](/user-screenshot.png?raw=true "nonroot User by default")

Useful Links:
1. [Announcing .NET Chiseled Containers](https://devblogs.microsoft.com/dotnet/announcing-dotnet-chiseled-containers/)
2. [Canonical announces the general availability of chiselled Ubuntu containers](https://canonical.com/blog/chiselled-ubuntu-ga)
3. [Github.com: chisel](https://github.com/canonical/chisel)
4. [Github.com: dotnet-docker # ubuntu-chiseled.md](https://github.com/dotnet/dotnet-docker/blob/main/documentation/ubuntu-chiseled.md)

[^1]: Github: Chisel
	2023, https://github.com/canonical/chisel

[^2]: Github: dotnet-docker # ubuntu-chiseled.md
	2023, https://github.com/dotnet/dotnet-docker/blob/main/documentation/ubuntu-chiseled.md