<!-- njnmdoc:  title="docker"  -->


Docker is a container that packages <i>everything</i> (Application, server,
dependencies, OS) into a VM with an easy to run interface.

*add yourself to the docker group.*

run it as a daemon (-d),
map the ports it needs (-p)
and the storage volume (-v) for the repos.

To run a shell, specify -t for TTY and -i for interactive:

Dockerfiles contain the recipe for creating a container, consisting of a base
image, and then commands to install and configure specific services.

Instead, you can use [[Fig]].

[https://blog.jtlebi.fr/2015/04/25/how-i-shrunk-a-docker-image-by-98-8-featuring-fanotify/ How I shrunk a Docker image by 98.8% – featuring fanotify | Yet another enthusiast blog!]
[http://developerblog.redhat.com/2016/02/24/10-things-to-avoid-in-docker-containers/ 10 things to avoid in docker containers – Red Hat Developer Blog]

##Links

## Fig notes

fig is a Docker management tool; it takes care of setting the command line up
right for you.


