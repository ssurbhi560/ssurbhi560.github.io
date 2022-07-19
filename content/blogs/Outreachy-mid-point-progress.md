---
title: "Outreachy mid-point project progress."
date: 2022-07-10
type: post
---

This week marked the mid-point of my internship at conda-forge as an Outreachy intern. I am working on documenting the conda-forge ecosystem. In this blog, I will go through the work progress I have been able to make so far, goals for the coming weeks, and some of the (many) things I have learned so far.

The first issue I started working on when the internship began was [Better anchoring of announcements](https://github.com/conda-forge/conda-forge.github.io/issues/1611). The goal of this issue was to fix the anchor for each year and also specific announcements in the Announcements section of conda-forge docs. This was also the time when I was feeling quite overwhelmed and anxious since I was just starting and was unsure if I would be able to give my best. But thanks to my awesome mentors [@Katherine](https://github.com/kathatherine) and [@Matt](https://github.com/beckermr), who have always been so helpful, I was able to have a good start. We solved this issue in two parts. The first part was to add anchors to each year which is solved [here](https://github.com/conda-forge/conda-forge.github.io/pull/1766), and the second part was adding anchors to each announcement and fixing the RSS feed. 

The part of the documentation I focused on after completing the first issue was Maintainers’ Documentation.

Many open issues needed to be taken care of to make the Maintainers’ documentation more useful and accessible for new maintainers. So far, the open tickets that we have worked on/are working on are:

1. [Document extras feedstock-name](https://github.com/conda-forge/conda-forge.github.io/issues/1769) and [Explain how to become a maintainer](https://github.com/conda-forge/conda-forge.github.io/issues/1331). Closed with [add extra section-recipe maintainer and feedstock-name](https://github.com/conda-forge/conda-forge.github.io/pull/1772)

    As we started with improving the Maintainer documentation, these were the issues we picked first to work on. The first issue was towards documenting how maintainers can use the ``feedstock-name`` directive for naming feedstocks differently than their package names in staged recipes. The second issue was for documenting how one should become a maintainer of a package.

2. [Add more steps in Improve the documentation section.](https://github.com/conda-forge/conda-forge.github.io/issues/1651). Solved [here](https://github.com/conda-forge/conda-forge.github.io/pull/1776)

    In this issue we added some additional steps for people who would like to start contributing to conda-forge, especially to documentation.

3. [Add more information about Grayskull in the documentation itself](https://github.com/conda-forge/conda-forge.github.io/issues/1655). Solved [here](https://github.com/conda-forge/conda-forge.github.io/pull/1777)

    The documentation on Grayskull in docs was lacking the answers to questions like what exactly is Grayskull and how should one use Grayskull to generate a recipe? With this issue we added more documentation on Grayskull for users.

4. [Clarify feedstock LICENSE.txt](https://github.com/conda-forge/conda-forge.github.io/issues/803). Solved [here](https://github.com/conda-forge/conda-forge.github.io/pull/1786)

    The docs for contributing and maintaining conda recipes discuss when and how to distribute the license for a particular package. The auto-generated feedstock repositories also include a license in the root, which is different from the related package license. With this issue we added documentation on the differences between those two licenses and also explained the feedstock repository structure briefly. 

5. [DOC: New maintainer](https://github.com/conda-forge/conda-forge.github.io/issues/1117). Solved [here](https://github.com/conda-forge/conda-forge.github.io/pull/1788)

    With this issue we improved docs for the new maintainers and the working of the bot. A “How does regro-cf-autotick-bot create automatic version updates?” section was added to the docs, which explains the whole process of creating an automated version update PRs by bot. 

6. [Add Perl package hints to documentation](https://github.com/conda-forge/conda-forge.github.io/issues/1536). Working on this [here](https://github.com/conda-forge/conda-forge.github.io/pull/1790)

    With this issue we added ​​packaging instructions for Perl packages with different build systems in the documentation.

7. [DOC: Update documentation about tokens](https://github.com/conda-forge/conda-forge.github.io/issues/1532). Working on this [here](https://github.com/conda-forge/conda-forge.github.io/pull/1793)

    Feedstocks have stopped storing encrypted tokens to upload packages, but outdated information on tokens was still present in the documentation. With this issue we removed the outdated information and also added a new section “How to update your feedstock token?” for maintainers.  

8. [Improve the documentation on arch_rebuild.txt](https://github.com/conda-forge/conda-forge.github.io/issues/1668). Working on this [here](https://github.com/conda-forge/conda-forge.github.io/pull/1794)

    With this issue we improved the documentation on ``arch_rebuild.txt`` and  how maintainers can add a feedstock to ``arch-rebuild.txt`` if it requires rebuilding with different architectures/platforms (such as ppc64le or aarch64).

Currently, I am working on [Document migrators](https://github.com/conda-forge/conda-forge.github.io/issues/1355) and [Add more relevant information in the 'compilers' section](https://github.com/conda-forge/conda-forge.github.io/issues/1357). 

For the coming weeks, I plan to add documentation covering all the security aspects of conda-forge builds and work towards making User documentation beginner-friendly by adding more relevant information.  
