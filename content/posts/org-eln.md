+++
title = "Emacs and Org-Mode for scientific research"
author = ["Sean Johnsen"]
date = 2022-03-18
tags = ["science", "emacs"]
draft = false
+++

[Org mode](https://orgmode.org/) is a popular package for the Emacs text editor. It specifies a document structure and syntax, then provides a wealth of tools to work with those files. This has allowed for the creation of an entire ecosystem of plain-text-oriented tooling around Org documents. In fact, I am writing this post in org mode right now. This whole site is created using Org mode and emacs!

I recently started a PhD, and have adopted Org mode for taking notes on the scientific literature, and for use as an [electronic lab notebook](https://en.wikipedia.org/wiki/Electronic_lab_notebook) (ELN). In this post, I'll first briefly explain some fundamental ideas behind org-mode. Next, I'll describe how I use these tools in my daily practice. Finally, I'll describe my particular configuration which aids in scientific documentation and note-taking.


## Emacs and Org mode - What they are and what they do {#emacs-and-org-mode-what-they-are-and-what-they-do}


## How I use Org mode for Note-taking {#how-i-use-org-mode-for-note-taking}

My note-taking strategy is based on Nicholas Luhmann's _Zettelkasten_[^fn:1] method. I learned about this method from Sonkë Ahrens' book, _How to Take Smart Notes_. The central idea behind the method is that knowledge is synthesized during the writing process by integrating information one has gathered from multiple primary sources.


## How I use Org mode as an Electronic Lab Notebook {#how-i-use-org-mode-as-an-electronic-lab-notebook}


### The problem {#the-problem}

My thesis work involves both "wet-lab" (molecular biology, transferring small amounts of clear liquid between various tubes) and "dry-lab" components (in my case, bioinformatic genomic analysis).

In biological research, one often has multiple interdependent projects each of which may take a week to a couple of months. A laboratory notebook should be a complete record of the relevant details and results of the experiments performed over the course of these projects. For example, I would like to determine the genomic distribution of a particular [histone post-translational modification](https://en.wikipedia.org/wiki/Histone#Modification) (PTM) in wild-type and mutant animals. To do this, I need to:

1.  Create a set of fly strains with a specific set of genetic mutations
2.  Verify that the antibodies I have for that PTM are specific, and work in the genomic assay I will use
3.  Actually perform the genomic assay on each different strain of fly

Just creating the required strains of flies will require months of work to engineer bacteria containing the DNA I wish to insert into the flies, inject the flies with this DNA, and verify that they contain the novel DNA. Of course of those steps will require tasks, sub-tasks, and sub-sub-tasks, each requiring molecular verification. These verification experiments produce data in different forms: sometimes confocal micrographs, sometimes pictures of a gel electrophoresis run, sometimes manual counts of living versus dead larvae. Sometimes I just take a picture of a petri dish growing bacteria with my phone. My genomics experiments generate large amounts of raw data formatted as [FASTQ](https://en.wikipedia.org/wiki/FASTQ_format) files, which are subsequently processed by bioinformatic piplines that we write in the lab, generating "processed" data files. These processed files are further used in downstream statistical analyses in R markdown notebooks.

These different data need to be organized and indexed. Crucially, I need to be able to look at a piece of data, and _go back to the entry in my notebook where I recorded the relevant details of the process that generated that data_. This is where Emacs and Org mode come in...


### The solution {#the-solution}

Emacs' Org mode provides a perfect environment for maintaining an electronic lab notebook.

First, **Org files are plain text**. The first edition of ASCII was published 59 years ago[^fn:2]. My guess is that plain text files will be readable for at least another 100 years. I don't expect that anyone will care about my thesis 100 years from now, but it still feels good that no one will need a proprietary piece of software to read my notebook (I'm looking at you Microsoft OneNote).


## My configuration {#my-configuration}

You can download my entire setup from my `dots` repository in GitHub.

[^fn:1]: meaning "slipbox" in German
[^fn:2]: at time of writing; <https://en.wikipedia.org/wiki/ASCII#Overview>
