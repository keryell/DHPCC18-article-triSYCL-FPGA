==============================================================
 Distributed & Heterogeneous Programming in C/C++ (DHPCC++18)
==============================================================

https://www.iwocl.org/iwocl-2018/dhpcc/

http://sycl.tech/distributed-heterogeneous-programming-in-c-cpp-dhpccpp18.html

https://easychair.org/cfp/DHPCC18

Submission: ttps://easychair.org/conferences/?conf=dhpcc18


The master template is now available in the following formats*: (last update February. 9, 2018)

    LaTeX (Version 1.49)

Actually TeXLive comes with the ACM formats, but a little bit older.


Getting started with this article
=================================

You can get a ``DHPCC-2018-triSYCL-FPGA.pdf`` file for this article
on a Linux machine with::

  cd src
  make

Reviews
=======

https://easychair.org/conferences/submission.cgi?submission=3693790;a=17588257

Review 1
Overall evaluation: 	
1: (weak accept)
The paper gives a broad overview on the SYCL programming model and its implementation in the triSYCL system. It introduces the advantages of those for the heterogeneous architectures we see emerging today and even more so in the future. Presenting this overview to the attendees of the DHPCC workshop will add an interesting facet to its program.
Review 2
Overall evaluation: 	
2: (accept)
This paper presents the authors experiences and results using SYCL to target Xlinx FPGA devices. They show how using standard SYCL with some specific extensions they are able to write natural looking code that can efficiently execute on FPGA devices. The paper provides a clear motivation for the work, describing the growing heterogeneity in HPC resources, and also provides a thorough introduction to the SYCL programming model. The descriptions are augmented with clear code snippets which make the paper easy to follow. The authors introduce concepts to help express pipelining, dataflow and array partitioning and use these to write an array transfer benchmark, for which they present results. The results could be presented with some more detailed analysis, as some of the surprising points on the graph lack explanation. E.g. why does execution time increase for some of the tools and languages increase when switching to a newer SDK? This is an interesting paper that is a good choice for inclusion in DHPCC++, and should be an interesting presentation.
Review 3
Overall evaluation: 	
2: (accept)
This paper discusses an on-going open-source project called triSYCL used to experiment with the SYCL standard. This framework has been extended to target Xilinx SDx tool to compile SYCL programs to run on a CPU host connected to FPGA cards.

The authors instead of using #pragma or attributes or extensions prefer to have some pure C++ function based or class based extensions, compatible with CPU emulation and that aligns with SYCL DSeL philosophy.

Readability can be improved! Line 360, optimizations such as a bunch of reference paper numbers does not particularly help.

I didn’t quite follow the significance of using 2017.2 and 2017.4 with different clang and llvm versions, for figure 6 experiments. Axes should be labeled, always! It seems clang/llvm 3.9 using 2017.2 takes a longer time than 2017.4 . It would help to add more explanation if you are trying to recommend one version over the other for particular runs. The turquoise bar for single-source (SYCL) is lower than the rest but the red bar seems to be as tall as for 3.1 and 3.9 OpenCL d+p. Why so?
Or group d+p and no opt bars together for say HLS C++ set. There should be a better way to represent Fig.6 and tell a story- you have tools, w/ and w/o optimizations, Xilinx SDx versions and Clang/LLVM versions.

I would have loved to see what the task graph looks like or some sort of representation of this task graph in a pen & paper sort of a way.

I like how you have concluded your paper! “With modern C++, there are less reasons to choose between “slow and convenient” and “fast and hard-to-use” programming models and we are seeing more an evolution from “fast and hard-to-use” towards a “fast and easy-to-use” paradigm”

I would like to see evaluations on real applications before I would conclude that triSYCL is competitive to other conventional programming tools and languages. More specifically an application evaluated against OpenCL and Verilog/VHDL and triSYCL. This will give us a taste of reality.

Having said that, FPGAs are very hard to program, so to that end, I like this triSYCL tool from Xilinx Research Labs. This effort is targeting on some of the real challenges with FPGAs. Thanks for including code snippets and thanks for making these code snippets available on GitHub


ACM copyright
=============

 ACM License Text, Bibstrip, and Form - International Workshop on OpenCL (IWOCL '18) 18 103
rightsreview@acm.org
Today, 11:12 AMRonan Keryell
Label: Delete email after 90 days (3 months) Expires: 7/13/2018 11:12 AM
Your ACM License for paper "Early experiments using SYCL single-source modern C++ on Xilinx FPGA" in International Workshop on OpenCL (IWOCL '18) has been accepted and is attached for your records.
If there are errors in either the title or author listing, please contact the proceedings coordinator for this publication, to receive a blank form to be completed for your accepted paper.

When preparing your paper for submission using the ACM TeX templates, the rights and permissions information and the bibliographic strip must appear on the lower left hand portion of the first page.

The new ACM Consolidated TeX template Version 1.3 and above automatically creates and positions these text blocks for you based on the code snippet which is system-generated based on your rights management choice and this particular conference.


Please copy and paste the following code snippet into your TeX file between \begin{document} and \maketitle, either after or before CCS codes.

\copyrightyear{2018}
\acmYear{2018}
\setcopyright{acmlicensed}
\acmConference[IWOCL '18]{International Workshop on OpenCL (IWOCL '18)}{May 14--16, 2018}{Oxford, United Kingdom}
\acmBooktitle{IWOCL '18: International Workshop on OpenCL (IWOCL '18), May 14--16, 2018, Oxford, United Kingdom}
\acmPrice{15.00}
\acmDOI{10.1145/3204919.3204937}
\acmISBN{978-1-4503-6439-3/18/05}


ACM TeX template .cls version 2.8, automatically creates and positions these text blocks for you based on the code snippet which is system-generated based on your rights management choice and this particular conference.

Please copy and paste the following code snippet into your TeX file between \begin{document} and \maketitle, either after or before CCS codes.

\CopyrightYear{2018}
\setcopyright{acmlicensed}
\conferenceinfo{IWOCL '18,}{May 14--16, 2018, Oxford, United Kingdom}
\isbn{978-1-4503-6439-3/18/05}\acmPrice{$15.00}
\doi{https://doi.org/10.1145/3204919.3204937}

If you are using the ACM Microsoft Word template, or still using an older version of the ACM TeX template, or the current versions of the ACM SIGCHI, SIGGRAPH, or SIGPLAN TeX templates, you must copy and paste the following text block into your document as per the instructions provided with the templates you are using:

Permission to make digital or hard copies of all or part of this work for personal or classroom use is granted without fee provided that copies are not made or distributed for profit or commercial advantage and that copies bear this notice and the full citation on the first page. Copyrights for components of this work owned by others than the author(s) must be honored. Abstracting with credit is permitted. To copy otherwise, or republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee. Request permissions from Permissions@acm.org.

IWOCL '18, May 14–16, 2018, Oxford, United Kingdom
© 2018 Copyright is held by the owner/author(s). Publication rights licensed to ACM.
ACM ISBN 978-1-4503-6439-3/18/05…$15.00
https://doi.org/10.1145/3204919.3204937

NOTE: Make sure to include your article's DOI as part of the bibstrip data; DOIs will be registered and become active shortly after publication in the ACM Digital Library

..
    # Some Emacs stuff:
    ### Local Variables:
    ### mode: rst
    ### minor-mode: flyspell
    ### ispell-local-dictionary: "american"
    ### End:
