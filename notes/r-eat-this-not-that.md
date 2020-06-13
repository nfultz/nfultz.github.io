Here are some simple substitutions to make your [[R]] leaner and meaner.

#Instead of

paste('path/to/', 'subdir/', 'myfile.txt', sep='')



#do

file.path('path', 'to', 'subdir', 'myfile.txt')



#Reason: file.path is more semantic, and will work correctly on multiple platforms.



#Instead of 

cat("Debug message\n")



#Do this 

message("Debug message")



#Reason: messages() can be disabled/ignored.

#Instead of

c(0, cumsum(x))



#Do this

diffinv(x)

#Instead of

apply(X, 1, which.max)



#Do this

max.col(X)

#Instead of

max(x) - min(x)



#Do this

diff(range(x))

