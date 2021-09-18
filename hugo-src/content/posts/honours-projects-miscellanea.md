+++
title = "Some Notes on Getting Started with Your Honours Project"
date = 2021-09-17T16:10:13+01:00
tags = ["teaching", "dissertation"]
draft = false
+++

Between when I started lecturing back in 2006/07, and now, I've supervised upwards of a hundred undergraduate dissertations and upwards of fifty masters dissertations. So I think that I might have done this job for long enough to learn a thing or two. I am still determing exactly what that learning might include, but here are a bunch of important things to consider when doing your dissertation with me. It's currently more of a brain dump than a considered set of guidance, and represents a bunch of things that we usually cover early in the supervision process, so it should be of some use:

* Your dissertation doesn't have to be about a unique idea or a novel piece of research. For example, a CompSci dissertation can comprise a replication study of existing work, perhaps a paper that you've found. A software engineering project can involve building a new version of something that already exists. This can make things easier in the long run because one important aspect of your dissertation is the evaluation, and replication or rebuilding give your project a built in competitor against which to compare your own work.
* You can also do the same project as another person - by this I mean that you can start with the same research goal, question, or objective. Working individually, your projects will then most likely deviate strongly from each other as you make design decisions and focus on aspects that are interesting and important to you.
* Work out early on how you will evaluate what you do. Evaluation is a learning outcome that many students fail to gain marks on because their evaluation was less accomplished than the rest of their work.
* The first challenge is to determine what you want to do for your project. A mistake that many students make is to try to do too much in their project. You actually have much less time in the honours project than you expect and so clearly articulated problem statement is key to getting started. This should be expanded into a set of either research questions or objectives depending upon whether you are doing a CompSci or a Software Engineering project. In either case it is ideal to have a single main question or objective that is broken down into several smaller and more specific questions or objectives. Your project, and dissertation, is then doing and documenting the process of either establishing answers to the questions or else satisfying the objectives.
* Evaluation can focus on a range of aspects, e.g. you, the project and it's management, your project artefacts, as well as comparative evaluation, to competitors, published work, datasets. A nice approach is to run your work, and a third party's work against the same dataset and then compare the results. You can also evaluate your work by using other people, experts, focus-groups, questionnaires, interviews, user feedback, etc. are all good ways to evaluate your work. A good evaluation will cover multiple aspects of your project and use multiple techniques.
* Be honest in your self appraisal, but don't sell yourself short, talk your project down, or focus on negative aspects or things that don't quite work the way you wanted them to. It's fine to mention these things but don't dwell on them. A focus on the things that do work is often preferable.
* Make a project plan. This doesn't have to be detailed initially. You'll start off with a very coarse grained plan and overtime you will add more and more tasks until, by the end of your project, you have a fine-grained record of all of your activities. Your plan doesn't have to be correct, you can replan and change things as your project progresses. You can then reflect on the difference between your initial and final plan as part of your evaluation of your project management. There are no specific tools that need to be used, a simple spreadsheet based gantt chart is perfectly fine (possibly supplemented with a simple issue tracker, like the GitHub issue tracker, to help emphasise links between plan, analysis, implementation, and testing)
* Set up project infrastructure early so that you don't have to do it later when you will have lots of more interesting tasks to complete.
* Use Git & optionally Github for code
* Create a shared folder for artefacts that don't fit into Git. Google drive is very good for this.
* Decide if you will use a word processor or LaTeX and then create your empty dissertation file using the appropriate style/template. If you're using LaTeX then consider using Overleaf. Overleaf has a Napier dissertation template in it's template library and it is convenient for sharing drafts of writing and getting feedback because I can make notes directly into the interface and we don't have to mess with emailing versions backwards and forwards
* If you are sharing a draft of writing and I don't need to edit it (which is always) then give me a PDF version rather than a word doc or LaTeX source. This is because a PDF is likely to be closer to the presentation you wanted me to see than the version rendered by whichever word processing app I happen to open that day. Also, PDF generally renders faster on my system than using either a word processor or building your file from source. Note that your final dissertation file must be a PDF. Don't submit a word proceesor file.
* Share your git repo, shared folder, and overleaf project with me. I won't look at anything unless you ask me to, so I won't be looking over your shoulder whilst you work. I don't have time for that. But I will be able to rapidly look at something when you need me to.
* Once you've created your dissertation document file. Put an outline into it. The easiest approach is to consider the chapter headings and create them. Now.
* A typical Software Engineering outline has the following structure:
    * Abstract
    * Introduction
    * Background (including literature and technical review, possibly as separate sub-sections)
    * Analysis
    * Design
    * Implementation
    * Testing
    * Evaluation
    * Conclusion (including future work)
    * References
    * Appendices (any work that doesn't fit into the narrative of the main body of the dissertation can go here. You can then reference individual appendices from appropriate places in the dissertation)
* Note that there is usually a bit of mirroring and alignment within the content of the Software Engineering dissertation:
    * The intro mirrors the conclusion -- questions asked in the introduction should be addressed in the conclusion
    * The analysis gives rise to a set of requirements, these are refined, prioritised (MoSCoW), and allocated tostages/prototypes of the project. Each stage/prototype is then designed, following an iterative process, and implemented, then tested.
    * For each requirement there should be a corresponding git commit (implementation) and a corresponding test - it is helpful to use Github issues, or something similar, to track these. This approach give cohesions to the project that cuts across the various chapters.
* Alternatively a Software Engineering outline can have this structure -- instead of analysis, design, implementation, and testing as separate chapters, organise by prototype for as many prototypes as you plan, with the software engineering stages as sub-sections of each prototype chapter, e.g.:
    * Abstract
    * Introduction
    * Background
    * Prototype #1
        * Analysis
        * Design
        * Implementation
        * Testing
    * Prototype #2
        * Analysis
        * Design
        * Implementation
        * Testing
    * Evaluation
    * Conclusion (including future work)
    * References
    * Appendices
* A typical CompSci outline has the following structure:
    * Abstract
    * Introduction
    * Background/Literature/Technical review
    * Implementation (covers the entire software engineering process: analysis, design, implementation, testing)
    * Experiments
    * Results
    * Evaluation
    * Conclusion
    * References
    * Appendices
* The difference in structures for the two types of dissertation reflects the different foci of each discipline. In Software Engineering we focus on the different stages of the software development process and devote a chapter to each. We expect the software artefact to be substantial and mature, the production of which gives plenty of material to write about in each chapter. The CompSci dissertation is more focussed on experimentation and so we want to build our software system more rapidly, ideally during the first trimester, so that we can perform experiments on or with it, and then report the results. We don't spend as much time developing the software so the software engineering process can usually fit into a single "implementation" chapter.
* Once you have a dissertation file, start writing into it. Regularly. Put your notes in there. Use bullet points if necessary. Over time, expand these bullets into sentences and paragraphs. If you do this over the entire duration of the project then you will find that, come the end, much of the dissertation is actually already written and merely needs editing ready for the final submission.
* Every project is different so there can be some variations to this structure, but don't spend time worrying about that. Get started, use a standard structure, and alter it if necessary.
* Your appendices should include versions of your IPO, interim report, diary sheets, and project plan, as well as any other work you've done that doesn't fit in the main body of the report.
* The main body of the report should be tightly written and follow a narrative. This means that we don't necessarily need to adopt an "academic style" for the writing, we just need to write clearly, concisely, and accurately. We also want to lead the reader through the project, so we need to decide what the point of the dissertation is (your research questions and project objectives will guide you in this) and then explain it throughout the writing without getting side-tracked.
* Testing and evaluation are not the same. From the perspective of your project, testing is about establishing that the system functions correctly according to it's design. Evaluation is about determing whether it does a good job of that, regardless of whether it functions correctly.
* Your IPO is your first project artefact. You will get a little, but likely not much, feedback about it because it is early in the project and you haven't yet done much. So get it done and squared away as soon as possible so you can focus on the rest of your project. The IPO doesn't carry any mark but is an early sanity check on your ideas that your supervisor and second marker can comment on.
* Your interim report, which is also often called the week nine report, is due towards the end of the first trimester of your project. Don't fixate on getting this done for exactly week nine, but anytime around that period of the trimester will do. It is mostly a record of your progress so far. Again it doesn't carry a mark but is the first opportunity to get useful feedback on your project. If you haven't done enough yet then it is an opportunity for your markers to deliver a kick up the arse. This is not to be mean but to reorient you whilst there is still time to do so. The interim report usually comprises an Introduction, a draft of the background chapter, a project plan, and anything else that you want to include that is evidence of the work done so far. A good idea is to put all of this into your dissertation file rather than creating a separate report.
* You should see a progression in the development of your ideas and project, from IPO, through the interim report, to the final dissertation report. 
* As you progress you will gain more knowledge, from your reading and thinking, and your ideas will be clarified. This is part of the process and takes time.
* The only secret to a good dissertation is to work consistently throughout the two trimesters. It is more of a marathon than a sprint. You will occasionally have to complete tasks that feel like you are grinding through stuff you don't want to do, and at other times you will get to do fun stuff. Which is which is different for every person, but it is all necessary in order to maximise your marks across all learning outcomes.

Along with a thorough read of the Moodle pages for the dissertation, these notes should be enough to help you get started.
