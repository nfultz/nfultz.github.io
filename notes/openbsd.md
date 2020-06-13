A few days ago an email was posted to tech@ asking to refactor one of the headers in mg. I must confess that I was annoyed by this email: it's doubly wrong. First, sysdef.h was not redundant in its header declaration. Second, the author did not include a diff with the email. Of course, had the author sent a diff he would have realized that the first point was false.



But I was already intrigued. And indeed there were plenty of redundant includes so I proposed a diff that eliminated the redundancy. Theo replied off list that my suggestion was backwards: instead of moving everything slowly into def.h I should instead turn to declaring headers in the individual .c files so that each file only includes exactly what it needs. As a bonus this would bring mg in line with the coding style the rest of OpenBSD --- [Musings of an OpenBSD developer](http://blog.anthrobsd.net/043.html)

[Pruning and Polishing: Keeping OpenBSD Modern](http://www.openbsd.org/papers/pruning.html)

