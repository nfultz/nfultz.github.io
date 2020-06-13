Ian Pylvainen [figured out](https://support.rstudio.com/hc/communities/public/questions/200653376-Rcpp-and-Roxygen) some problems with using roxygen with Rcpp:



<blockquote>I have just sorted this out myself. This may not be best practices but it works for me:

<ol><li> <code>@useDynLib MyPack</code> <br/>

You need to add the tag @useDynLib MyPack somewhere in you Roxygen documentation. I have decided to put it in my package documentation R file that is nothing but the Roxygen tags for the package documentation.

<p>

I call mine file MyPack-package.R and keep it in the R directory. The @useDynLib MyPack tag goes right before the NULL statement in my file. I am pretty sure it works anywhere in a Roxygen block though.

<li> <code>@export</code> <br/>

In each of the Rcpp scripts that you want to be an exported function you need to put an @export tag. This may not be necessary if you are exporting everything, but it looks like if you choose to be selective about exporting certain functions writen natively in R then you have to explicitly @export in the Rcpp file.

</ol>

Hope this helps.

</blockquote>

