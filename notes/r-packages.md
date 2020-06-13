[High Performance Machine Learning in R with H2O](http://www.stat.berkeley.edu/~ledell/docs/h2o_hpccon_oct2015.pdf)

[Colout by nojhan](http://nojhan.github.io/colout/)

[Blag's bag of rants: R - My journey so far](http://blagrants.blogspot.com/2015/09/r-my-journey-so-far.html)

Wrappers for fork()/waitpid() meant to allow R users to quickly and easily fork child processes and wait for them to finish.



 --- [CRAN - Package bfork](https://cran.r-project.org/web/packages/bfork/)

The material is based on the online courses I have been teaching with Mike Love. As we created the course, Mike and I wrote R markdown documents for the students and put them on GitHub. We then used jekyll to create a webpage with html versions of the markdown documents. Jeff then convinced us to publish it on LeanbupLeanpub. So we wrote a shell script that compiled the entire book into a Leanpub directory, and after countless hours of editing and tinkering we have a 450  page book with over 200 exercises. The entire book compiles from scratch in about 20 minutes. We hope you like it. --- [Data Analysis for the Life Sciences – a book completely written in R markdown | Simply Statistics](http://simplystatistics.org/2015/09/23/data-analysis-for-the-life-sciences-a-book-completely-written-in-r-markdown/)

[aRrgh: a newcomer's (angry) guide to R](http://arrgh.tim-smith.us/)

[R package xkcd](http://xkcd.r-forge.r-project.org/)

The R package ecosystem is one of the cornerstones of the success seen by R. As of this writing, over 6200 are on CRAN, several hundred more at BioConductor and at OmegaHat.



Support for multiple repositories is built deeply into R; mostly via the (default) package utils. The update.packages function (along with several others from the utils package) can used for these three default repositories as well as many others with ease. But it seemed that support for simple creation and use of local repositories was however missing.



Drat tries to help here.



 --- [drat: drat R Archive Template](http://dirk.eddelbuettel.com/code/drat.html)

tidyr is new package that makes it easy to tidy your data. Tidy data is data that’s easy to work with: it’s easy to munge (with dplyr), visualise (with ggplot2 or ggvis) and model (with R’s hundreds of modelling packages). The two most important properties of tidy data are:

 <ul>

   <li> Each column is a variable.

   <li>  Each row is an observation.

 </ul>

Arranging your data in this way makes it easier to work with because you have a consistent way of referring to variables (as column names) and observations (as row indices). When use tidy data and tidy tools, you spend less time worrying about how to feed the output from one function into the input of another, and more time answering your questions about the data. --- [Introducing tidyr | RStudio Blog](http://blog.rstudio.org/2014/07/22/introducing-tidyr/)

The goal of checkpoint is to solve the problem of package reproducibility in R. Specifically, checkpoint allows you to install packages as they existed on CRAN on a specific snapshot date as if you had a CRAN time machine. To achieve reproducibility, the checkpoint() function installs the packages required or called by your project and scripts to a local library exactly as they existed at the specified point in time. Only those packages are available to your project, thereby avoiding any package updates that came later and may have altered your results. In this way, anyone using checkpoint's checkpoint() can ensure the reproducibility of your scripts or projects at any time. To create the snapshot archives, once a day (at midnight UTC) we refresh the Austria CRAN mirror, on the "Managed R...   More»

 --- [MRAN - Managed R Archive Network · Package Info](http://mran.revolutionanalytics.com/packages/info/?checkpoint)

This package provides support for randomized software testing for R. Inspired by its influential Haskell namesake, it promotes a style of writing tests where assertions about functions are verified on random inputs. The package provides default generators for most common types but allows users to modify their behavior or even to create new ones based on the needs of a each application. The main advantages over traditional testing are



 --- [RevolutionAnalytics/quickcheck · GitHub](https://github.com/RevolutionAnalytics/quickcheck)

The template contains the four usual components of any scientific manuscript:



equations (using LaTeX syntax)

table with caption (done by kable package, but you can also use xtable)

figure with caption

citations and references (done by knitcitations package)

 --- [» Simple template for scientific manuscripts in R markdown](http://www.petrkeil.com/?p=2401)

[The Hitchhiker's Guide to the Hadleyverse – Adolfo Álvarez](http://adolfoalvarez.cl/the-hitchhikers-guide-to-the-hadleyverse/)

opying source code of another student completely makes no sense, as student does not learn, and what is more, he/she gets points for something he/she didn’t make.



When there are only few homeworks to check, it is easy to do it manually. But what if there is a large number of submissions? Then we need some application to automate the process. There are some known tools for standard programming languages, such as MOSS or JPLAG for e.g. C, C  , C#, Java, Scheme or Javascript.



But what if we want to automate the process of checking similarity of R source code? Till now there were no such a tool available. But things have changed.



SimilaR --- [SimilaR | Rexamine](http://www.rexamine.com/2015/03/similar/)

[Adding estimability checking to a modeling package](https://journal.r-project.org/archive/2015-1/lenth.pdf)

[Minimal R Package Check List | Simply Statistics](http://simplystatistics.org/2015/10/14/minimal-r-package-check-list/)

[Roll Your Own Stats and Geoms in ggplot2 (Part 1: Splines!) | rud.is](http://rud.is/b/2015/09/08/roll-your-own-stats-and-geoms-in-ggplot2-part-1-splines/)

[rpca · MRAN](https://mran.revolutionanalytics.com/package/rpca/)

[Introducing cricketr! : A R package to analyze performances of cricketers | Giga thoughts …](https://gigadom.wordpress.com/2015/07/04/introducing-cricketr-a-r-package-to-analyze-performances-of-cricketers/)

[Package Info · MRAN](https://mran.revolutionanalytics.com/packages/info/?switchr)

[Using S3 buckets in R with RS3 library](https://www.gastrograph.com/blogs/dev/using-s3-in-r.html)

