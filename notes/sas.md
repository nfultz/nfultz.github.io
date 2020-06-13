SAS doesn't behave properly on unix. I would expect it to read to stdin, write output to stdout and log errors to stderr. Nope.

* To read data from stdin;

infile stdin;

