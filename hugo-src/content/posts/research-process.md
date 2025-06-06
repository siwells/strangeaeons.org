+++
title = "My Research & Writing Process"
date = 2025-06-06T17:45:00+01:00
tags = ["research","writing"]
+++

A recent conversation with a student led me to reflect on my approach to research and writing. These notes might prove useful to someone, somewhere, perhaps, as an example of one research flow. I daresay others have their own working methods, but this is one I've refined over a long period into something that works consistently for me.

Nearly all of my work involves either thinking and writing. As an academic, these two practices, thinking and reading, revolve around both my own ideas and the published ideas of others. So the majority of my work starts with published papers and books. I keep everything organised in a single bibtex database that I hand edit in Vim. I've done this for more than twenty years now and don't see a reason to change. It works for me but your mileage may vary. I chose bibtex because my preferred typesetting tool is LaTex, which also works for me. There are other bibliographic and typesetting tools out there, if you find one you like then use it.

It is important though to collect bibliograpgic information as you go along because it is a pain to track down the details later, when a deadline is looking and you just want to cite something. I tend to add the bibliographic entry to my bibtex file as I go along, usually when I come to read the paper. Every paper is kept digitally as a PDF in a set of organised folders organised alphabetically. Files are named consistently using the following schema:

    first-authors-last-name_YEAR-of-publication_title-of-paper

So my own 2012 paper, "A Domain Specific Language for Describing Diverse Systems of Dialogue" has the following filename:

    wells_2012_a.domain.specific.language.for.describing.diverse.systems.of.dialogue.pdf

This approach means that every reference has a single, consistent identifier. Yes it can be a little unwieldy at times, but I find that this nicely self sorts by author, then by year, and finally I can usually remember enough about the papers from part of the title to orient myself. 

This bibtex database becomes the starting place for nearly everything that follows. Firstly I have a simple LaTeX document called bibliography that contains the following:

    \documentclass{article}
    \begin{document}
    \hfill\today
    \nocite{*}
    \bibliographystyle{plain}
    \bibliography{../resources/bib/master}
    \end{document}

This yields a date-stamped, typeset, bibliography document of everything in my bibtex database rendered to PDF. I periodically print this out as it is really useful to page through to find things I might have forgotten about. Whilst digital is useful for many things, like searching within documents, paper can still have it's role for some of us, especially those of us who grew up in a pre-digital age perhaps.

I then have two additional regular LaTeX documents, a topics document and a notebook document. Within both of these documents I make extensive use of the LaTeX hyperref package (see this useful [Overleaf documentation page](https://www.overleaf.com/learn/latex/Hyperlinks) for additional info) to provide internal links so that as I read I can jump around from topic to topic as if I was in a Wiki, just without running an actual Wiki.


The topics document is where I create bibliographies specific to particular research questions or problems that I am working on. Within it I basically write a paragraph summarising how the given paper is relevant to the specific topic, and then cite the resource in by bibtex database. Again this is rendered to PDF to give me a nicely typeset document

The notebook document is my equivalent of a lab notebook. It is structured into two parts. The first part is organised by research topic, and is basically my own writing and thinking on the topics that I am working on. It is well structured according to my own understanding and prioritisation within my reseach domain. The content is a synthesis of all I know and think on the given subject. By keeping this notebook, extending it regularly, and periodically reviewing the writing within, I develop my thoughts and ideas that form that basis for my research papers. This way I am not working in multiple places, but instead, I have a single workspace in which I assemble my thoughts. This is supplemented by a paper notebook for on the fly ideas and scribbles, and my whiteboard. The contents of the paper notebook and whiteboard are generally reviewed and synthesised into my LaTeX notebook on a periodic basis. Part 2 of the notebook is just as important and has two sections. The first is titled "Ideas & Questions" and is where I record any arbitrary question that crossed my mind but which is not yet ready for the next section. The second section is "Project Ideas" and is where I start to develop the aforementioned questions, either individually or in groups, into specific research projects, targetted torwards either grants, or UG/PG students.

When a piece of writing is sufficiently developed then I will branch it off into a separate LaTex document for writing up as a paper for a specific venue or deadline. Similarly for project ideas that might be developed into either proposals for research grants or into briefs for student projects.

To summarise, I have:

* A consistently named collection of papers and books.
* A master bibtex database that indexes the papers and books.
* A bibliography generated from the bibtex database.
* A topics document that indexes my bibliography by topic of interest.
* A notebook of my own notes and ideas.

